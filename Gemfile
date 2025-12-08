source "https://rubygems.org"

# --- Core Dependencies ---
gem "jekyll", "~> 4.4.1"
gem "faraday-retry"

# --- Theme ---
# The Minimal Mistakes theme gem
gem "minimal-mistakes-jekyll"

# --- Plugins ---
# These plugins are automatically loaded by Jekyll
group :jekyll_plugins do
  gem "jekyll-feed"           # RSS/Atom feed generator
  gem "jekyll-seo-tag"        # SEO meta tags
  gem "jekyll-sitemap"        # XML sitemap for search engines
  gem "jekyll-gist"           # Embed GitHub Gists
  gem "jekyll-include-cache"  # Performance booster for the theme
end

# --- Local Development Utilities ---
# Required for running 'jekyll serve' on Ruby 3.0+ (Ubuntu 24.04)
gem "webrick"

# --- Cross-Platform Compatibility ---
# Performance booster for file watching on native Windows (ignored on WSL2)
gem "wdm", "~> 0.1", platforms: [:windows]

# Timezone data (Prevents errors on Windows/WSL)
gem "tzinfo-data", platforms: [:windows, :jruby]