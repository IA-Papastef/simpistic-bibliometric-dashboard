# Contributing to Bibliometric Research Dashboard

Thank you for your interest in contributing! This project is intentionally simple — a single HTML file with no build step — and we'd like to keep it that way.

## Guidelines

### Keep It Simple
- The entire app lives in `index.html`. This is a feature, not a limitation.
- No build tools, bundlers, or package managers.
- External libraries should be loaded via CDN with SRI hashes.

### Code Style
- Use semantic HTML5 with ARIA attributes for accessibility.
- CSS uses custom properties (variables) defined in `:root`.
- JavaScript uses vanilla ES6+ (no frameworks).
- Use clear comments to separate logical sections.
- Follow the existing naming conventions (BEM-like for CSS classes).

### How to Contribute

1. **Fork** the repository
2. **Create a branch** for your change (`git checkout -b feature/dark-mode`)
3. **Make your changes** to `index.html`
4. **Test** in at least two browsers (Chrome + Firefox recommended)
5. **Submit a Pull Request** with a clear description of what you changed and why

### What We're Looking For
- Bug fixes
- Accessibility improvements
- New chart types or visualization options
- Better mobile responsiveness
- Documentation improvements
- Translations (i18n)

### What We'd Prefer to Avoid
- Adding build tools or package managers
- Splitting the app into multiple files (unless there's a very strong reason)
- Adding heavy frameworks (React, Vue, etc.)
- Features that require a server

## Reporting Issues

Please use GitHub Issues and include:
- Browser and version
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if relevant

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
