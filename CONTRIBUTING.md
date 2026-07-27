# Contributing to Typeface Lab

Thank you for your interest in improving Typeface Lab. The project is intentionally static, dependency-free, and build-free. Contributions should preserve those constraints unless a change is discussed and approved in advance.

## Before starting

- Search existing issues and pull requests to avoid duplicate work.
- Open an issue before beginning a substantial feature or architectural change.
- Keep pull requests focused on one problem or improvement.

## Reporting a bug

Include the following information:

- A concise description of the problem and expected behavior.
- Exact steps to reproduce the issue.
- The selected font family, if the issue is font-specific.
- Browser name and version.
- Operating system and viewport size.
- Relevant console messages or screenshots.

Do not report security vulnerabilities in a public issue. Follow [SECURITY.md](SECURITY.md) instead.

## Suggesting an enhancement

Explain the user problem and expected outcome before proposing an implementation. Typeface Lab prioritizes a focused interface, progressive loading, accessibility, and a small static footprint.

## Development setup

Clone the repository and serve it with any static HTTP server:

```bash
git clone https://github.com/Ft2801/Typeface_Lab.git
cd Typeface_Lab
python3 -m http.server 8000
```

Open `http://localhost:8000`.

## Development guidelines

- Keep the application in `index.html` unless there is a compelling reason to change the architecture.
- Use semantic HTML, modern CSS, and vanilla JavaScript.
- Do not add frameworks, package managers, build systems, analytics, or tracking.
- Do not add runtime network requests other than those required to load Google Fonts.
- Preserve progressive font-preview loading and the existing cache limits.
- Match the existing indentation, naming, and section-comment style.
- Keep user-facing copy in English.
- Maintain keyboard support and appropriate ARIA state.

## Required testing

Before opening a pull request, verify:

- The page loads without console errors.
- Font search, presets, and the full A-Z browser work.
- Static and variable fonts load and apply correctly.
- Unsupported controls remain hidden.
- The live preview responds to all visible controls.
- Theme switching works and persists.
- Desktop and mobile layouts do not overflow.
- Keyboard navigation, Escape behavior, and focus restoration still work.
- Local asset references, the manifest, and metadata remain valid.

Test at least one static family, one variable family, one italic family, and one unusually wide display family.

## Pull requests

1. Fork the repository and create a branch from `main`.
2. Make the change and test it locally.
3. Update documentation or `CHANGELOG.md` when appropriate.
4. Use a clear title and explain both the problem and solution.
5. Confirm the checklist in the pull request template.

By contributing, you agree that your contribution is licensed under the project's [MIT License](LICENSE).
