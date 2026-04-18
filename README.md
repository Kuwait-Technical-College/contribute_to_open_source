<p align="center">
  <img src="assets/ktech_logo_light.svg" alt="ktech logo" width="200">
</p>

# Contributing to Open Source — Tutorial & Slides

**Kuwait Technical College (ktech)**

A hands-on tutorial that teaches students how to make their first open-source contribution using VS Code, Git, GitHub, and GitHub Copilot.

## What's Inside

| File | Description |
|---|---|
| [tutorial-contribute-to-open-source.md](tutorial-contribute-to-open-source.md) | Full written tutorial with step-by-step instructions and instructor notes |
| [slides.md](slides.md) | Presentation slides powered by [Slidev](https://sli.dev) for classroom use |
| [slides.pdf](assets/slides.pdf) | PDF export of the slides for offline viewing or printing |
| [🎥 Video Walkthrough](https://www.youtube.com/watch?v=a8poI7DmBYs) | Full tutorial in video format on YouTube |

## Tutorial Overview

Students will fork a real open-source project, use GitHub Copilot to generate a cybersecurity zen koan, and submit a Pull Request — all within a ~2-hour guided session.

### Topics Covered

- Setting up VS Code, Git, and GitHub
- Basic terminal / command-line usage
- Git fundamentals (clone, add, commit, push)
- GitHub workflow (fork, pull request)
- AI-assisted development with GitHub Copilot

### Target Repository

Students contribute to: [Kuwait-Technical-College/cybersecurity_zen_koans_app](https://github.com/Kuwait-Technical-College/cybersecurity_zen_koans_app)

### About the App

**Cybersecurity Zen Koans** is a real mobile app built with Flutter, available on the App Store and Google Play Store. It displays short, zen-style cybersecurity sayings paired with technical explanations. All koans live in a single JSON file — meaning anyone can contribute via a Pull Request. Once a PR is merged, a new version of the app is published to both stores with the contribution included.

## Running the Slides

```bash
npm install
npm run dev
```

This starts a local Slidev server. Open the URL shown in the terminal to view the presentation.

### Other Slide Commands

```bash
npm run build    # Build static HTML for hosting
npm run export   # Export slides to PDF
```

## License

This tutorial is provided for educational use at Kuwait Technical College.
