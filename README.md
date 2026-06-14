# mk-mccann.github.io

Personal website and electronic CV.

## Local development

Prerequisites on Ubuntu/Debian:

1. Install Ruby toolchain packages:

	sudo apt update && sudo apt install -y ruby-full ruby-dev build-essential zlib1g-dev

1. Install dependencies:

	bundle config set --local path vendor/bundle
	bundle install

2. Run the site locally:

	bundle exec jekyll serve --livereload

3. Open the preview URL shown in the terminal (usually http://127.0.0.1:4000).

4. Build only (CI-equivalent check):

	bundle exec jekyll build

## GitHub Pages via Actions

This repository includes a workflow at .github/workflows/jekyll.yml that:

1. Builds the Jekyll site on push to main and on pull requests.
2. Deploys to GitHub Pages only on push to main.

Repository settings required:

1. In GitHub, go to Settings -> Pages.
2. Under Build and deployment, set Source to GitHub Actions.
