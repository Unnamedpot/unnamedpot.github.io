# Gemfile for local Jekyll development.
# Goal: match the GitHub Pages production build as closely as possible.

source "https://rubygems.org"

# The github-pages gem locks Jekyll and its plugins to the exact
# versions GitHub Pages runs in production, so local output matches
# the deployed site. This pulls in Jekyll transitively.
gem "github-pages", group: :jekyll_plugins

# Ruby 3.x removed webrick from the standard library, but
# `jekyll serve` still relies on it for the local dev server.
gem "webrick", "~> 1.8"

# Windows does not include zoneinfo; tzinfo-data provides it so
# timezone-dependent Liquid filters work correctly.
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]