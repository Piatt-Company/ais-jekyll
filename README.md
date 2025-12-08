# AI Infrastructure Services (AIS)

This is the public-facing corporate website for **AI Infrastructure Services**, built with Jekyll and the Minimal Mistakes theme.

## Project Overview
* **Theme:** [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) (Gem-based installation)
* **Status:** Production-ready
* **Node:** Clean build policy (Zero Warnings)

## Prerequisites
* Ruby 3.0+
* Bundler
* GCC/Make (build essentials)

## Quick Start

1. **Clone the repository:**
   ```bash
   git clone <repo-url>
   cd ais-jekyll
   ```

2. **Install Dependencies:**
   ```bash
   bundle install
   ```

3. **Run Local Server:**
   ```bash
   bundle exec jekyll serve --livereload
   ```
   The site will be available at: `http://localhost:4000`

## Development Notes

### Styling
* **Branding:** Brand colors (Navy/Copper) are defined in `assets/css/main.scss`.
* **Linting:** VS Code settings (`.vscode/settings.json`) are configured to suppress false positives for Jekyll Front Matter and project-specific terminology (e.g., "Infraservices").

### Deprecation Policy
This project uses `quiet_deps: true` and `silence_deprecations: ["import"]` in `_config.yml` to suppress upstream warnings from the Minimal Mistakes theme regarding Dart Sass 3.0 compatibility. Do not remove these settings.