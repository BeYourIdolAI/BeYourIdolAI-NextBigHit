# 🤝 Contributing to DeejAI

First off, thank you for considering contributing to DeejAI! 💜

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Style Guidelines](#style-guidelines)
- [Pull Request Process](#pull-request-process)

---

## 📜 Code of Conduct

This project follows a simple rule: **Be kind.**

- Be respectful and inclusive
- Welcome newcomers warmly
- Focus on constructive feedback
- Remember: we're all here to create something beautiful

---

## 🎯 How Can I Contribute?

### 🐛 Reporting Bugs

Found a bug? Help us fix it!

1. Check if it's already reported in [Issues](../../issues)
2. If not, create a new issue with:
   - Clear title
   - Steps to reproduce
   - Expected vs actual behavior
   - Browser/device info
   - Screenshots if possible

### 💡 Suggesting Features

Have an idea? We'd love to hear it!

1. Check [existing feature requests](../../issues?q=is%3Aissue+label%3Aenhancement)
2. Create a new issue with:
   - Clear description of the feature
   - Why it would be useful
   - Possible implementation ideas

### 🎨 Design Contributions

- UI/UX improvements
- New color schemes
- Icon designs
- Animation ideas

### 📖 Documentation

- Fix typos
- Improve explanations
- Add examples
- Translate to other languages

### 💻 Code Contributions

See [Development Setup](#development-setup) below.

---

## 🛠️ Development Setup

### Prerequisites

- Any modern web browser
- A text editor (VS Code recommended)
- Basic knowledge of HTML, CSS, JavaScript

### Getting Started

```bash
# 1. Fork the repository on GitHub

# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/DeejAI.git
cd DeejAI

# 3. Open in browser
open app/index.html

# 4. Make changes and refresh browser to see them
```

### Project Structure

```
DeejAI/
├── app/
│   └── index.html      # Main application (all-in-one)
├── docs/
│   ├── LINEAR_FLOW.md  # Linear Flow documentation
│   └── ROADMAP.md      # Development roadmap
├── assets/
│   ├── images/         # Screenshots, logos
│   └── audio/          # Sound samples
└── README.md
```

### No Build Process

DeejAI is intentionally simple:
- No npm/yarn required
- No webpack/vite/bundler
- Just edit HTML/CSS/JS and refresh

This keeps contributions accessible to everyone.

---

## 🎨 Style Guidelines

### JavaScript

```javascript
// Use descriptive variable names
const beatVelocity = 0.8;  // ✅ Good
const bv = 0.8;            // ❌ Avoid

// Use const/let, never var
const MAX_BEATS = 100;     // ✅ Good
var maxBeats = 100;        // ❌ Avoid

// Comment complex logic
// Calculate velocity based on press duration (0.3 to 1.0)
const velocity = Math.min(1, 0.3 + (duration / 700) * 0.7);
```

### CSS

```css
/* Use CSS variables for colors */
.beat {
  background: var(--neon-pink);  /* ✅ Good */
  background: #ff00ff;           /* ❌ Avoid */
}

/* Mobile-first approach */
.container {
  width: 100%;
}

@media (min-width: 768px) {
  .container {
    width: 80%;
  }
}
```

### Commit Messages

```bash
# Format: type(scope): description

feat(linear): add velocity indicator
fix(audio): prevent clipping on overlap
docs(readme): update installation instructions
style(ui): improve button hover states
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

---

## 🔄 Pull Request Process

### 1. Create a Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/bug-description
```

### 2. Make Your Changes

- Keep changes focused and minimal
- Test in multiple browsers
- Update documentation if needed

### 3. Commit Your Changes

```bash
git add .
git commit -m "feat(scope): description of change"
```

### 4. Push to Your Fork

```bash
git push origin feature/your-feature-name
```

### 5. Open a Pull Request

1. Go to the original repository
2. Click "New Pull Request"
3. Select your branch
4. Fill in the PR template:
   - What does this PR do?
   - How has it been tested?
   - Screenshots (if UI changes)

### 6. Review Process

- A maintainer will review your PR
- They may request changes
- Once approved, it will be merged

---

## 🏷️ Issue Labels

| Label | Description |
|-------|-------------|
| `bug` | Something isn't working |
| `enhancement` | New feature request |
| `good first issue` | Good for newcomers |
| `help wanted` | Extra attention needed |
| `documentation` | Documentation improvements |
| `design` | UI/UX related |

---

## 🎖️ Recognition

Contributors will be:
- Listed in our README
- Thanked in release notes
- Part of the DeejAI community forever 💜

---

## ❓ Questions?

- Open an issue with the `question` label
- Join our discussions
- Reach out to the maintainers

---

## 💜 Thank You!

Every contribution, no matter how small, makes DeejAI better.

*"Flow Over Form — Together"*

— Jimmy & Frida
