# 🌊 LINEAR FLOW – Emotional Music Engine

> *"Musik ska inte skapas i boxar – den ska flöda fritt som tankar och känslor."*  
> — Frida Stålberg, Co-Creator

---

## 📖 Filosofi: Flow Over Form

Traditional music sequencers force creativity into rigid grids – 16 steps, 8 rows, perfect quantization. While this approach works for precise production, it fundamentally conflicts with how humans experience music emotionally.

**Linear Flow** challenges this paradigm by asking:

*What if beats were feelings, not boxes?*

Instead of clicking squares on a grid, users place glowing orbs anywhere on a flowing timeline. These orbs can be:
- **Moved freely** (drag & drop)
- **Stacked** (overlap for layered sounds)
- **Removed** (double-click)
- **Expressed** (velocity based on interaction)

This creates an instrument that responds to *emotion* rather than demanding *precision*.

---

## 🎯 Core Principles

| Principle | Traditional Sequencer | Linear Flow |
|-----------|----------------------|-------------|
| **Time** | Fixed grid steps | Continuous flow |
| **Placement** | Snap to grid | Free positioning |
| **Layering** | One sound per cell | Unlimited overlap |
| **Visual** | Squares/rectangles | Glowing orbs with energy |
| **Interaction** | Click to toggle | Drag, drop, stack, express |
| **Philosophy** | Mathematical | Emotional |

---

## ✨ Key Features

### 1. Free Placement
Click anywhere on the timeline to place a beat. No snapping, no restrictions.

```
Traditional: [■][■][□][□][■][□][□][■]
Linear Flow: ○    ○  ○      ○    ○○○
             ↑ beats float at any position
```

### 2. Drag & Drop
Every beat can be grabbed and moved. Cursor changes to indicate draggable state.

### 3. Overlap / Sound Stacking
Place beats close together to create layered sounds:
- Visual feedback: larger glow, white ring, multiplier (×2, ×3)
- Audio: all overlapping sounds play simultaneously
- Gain limiting prevents clipping

### 4. Velocity Sensitivity
How you interact affects the sound:
- Quick click = soft hit
- Long press = stronger hit
- Visual size reflects velocity

### 5. Multi-Track Layers
Separate tracks for different sound categories:
- 🥁 Drums
- 🎸 Bass
- 🎹 Melody
- ✨ Effects

### 6. Undo/Redo History
Full action history with Ctrl+Z / Ctrl+Y support.

---

## 🏗️ Technical Architecture

### Canvas-Based Rendering
```javascript
// Core render loop
function animateLinear() {
  ctx.fillStyle = 'rgba(10, 10, 26, 0.15)'; // Fade trail
  ctx.fillRect(0, 0, w, h);
  
  // Draw timeline glow
  // Draw track lanes
  // Draw beats as glowing orbs
  // Draw playhead
  
  requestAnimationFrame(animateLinear);
}
```

### Beat Data Structure
```javascript
{
  id: Number,        // Unique identifier
  x: 0-1,            // Position on timeline (0 = start, 1 = end)
  y: 0-1,            // Vertical position (track/pitch)
  sound: String,     // 'kick' | 'snare' | 'hihat' | 'bass'
  velocity: 0-1,     // Volume/intensity
  layer: Number,     // Track layer
  pulse: Number      // Animation phase
}
```

### Audio Engine
```javascript
// Web Audio API with gain limiting
const masterGain = audioCtx.createGain();
const limiter = audioCtx.createDynamicsCompressor();

limiter.threshold.value = -6;
limiter.knee.value = 3;
limiter.ratio.value = 12;

masterGain.connect(limiter);
limiter.connect(audioCtx.destination);
```

### Interaction Handling
```javascript
// Unified mouse/touch handling
function handleStart(x, y) {
  const hit = getBeatAtPosition(x, y);
  if (hit) startDrag(hit);
  else createBeat(x, y);
}
```

---

## 📱 Platform Support

| Platform | Status | Notes |
|----------|--------|-------|
| Desktop Chrome | ✅ Full | Primary development target |
| Desktop Firefox | ✅ Full | Tested |
| Desktop Safari | ✅ Full | Tested |
| iOS Safari | ✅ Full | Touch optimized |
| Android Chrome | ✅ Full | Touch optimized |
| PWA | ✅ Ready | Installable |

---

## 🎨 Visual Design Language

### Color Palette
```css
--neon-pink: #ff00ff    /* Melody, FX */
--neon-blue: #00ffff    /* Hi-hats, percussion */
--neon-green: #00ff88   /* Bass, low frequencies */
--neon-red: #ff0055     /* Kick, drums */
--neon-yellow: #ffff00  /* Snare, accents */
```

### Animation Principles
- **Pulse**: Beats breathe with a sine wave animation
- **Glow**: Radial gradients create depth
- **Trail**: Canvas fade creates motion blur
- **Energy**: Overlapping beats pulse faster and glow brighter

---

## 🚀 Roadmap

### v5.8 – Flow Depth (Current)
- [x] Gain limiter for overlap
- [x] Undo/Redo system
- [x] Multi-track layers
- [x] Velocity control

### v5.9 – Visual Pulse
- [ ] Real-time audio visualization
- [ ] Waveform pulses along timeline
- [ ] Beat energy particles
- [ ] Reactive background

### v6.0 – Emotional Mapping
- [ ] AI companion mood detection
- [ ] Music-to-emotion analysis
- [ ] Personalized feedback
- [ ] Mental wellness integration

---

## 💡 Why This Matters

Linear Flow isn't just a feature – it's a philosophy embedded in code.

For users with:
- **ADHD**: No rigid structure to follow
- **Anxiety**: Calming, flowing interface
- **Creative blocks**: Intuitive, playful interaction
- **Disabilities**: Touch-friendly, no precision required

Music creation should be *accessible* and *emotional*, not technical and exclusive.

---

## 👥 Credits

**Created by:**
- Jimmy Andersson – Lead Developer
- Frida Stålberg – Creative Vision & Design Philosophy

**Part of:**
- BeYourIdolAI – Making creativity accessible to everyone

---

## 📄 License

© 2025 BeYourIdolAI. All rights reserved.

For licensing inquiries: [contact@beyouridolai.com]

---

*"Every beat is a feeling. Every feeling deserves to be heard."*
