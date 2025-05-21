# Twitter Images for pgflow

This directory contains code snippet images used in pgflow Twitter/X posts.

## Image Naming Convention

Images are named after their corresponding markdown files:

- `tweet-filename.png` - Generated from `tweet-filename.md`

## Usage in Tweets

These images are referenced in tweet markdown files using the `image_url` frontmatter field:

```yaml
---
link: "https://pgflow.dev/example/"
source_code_for_image: |
  // Code snippet here
language_for_image: "js"
image_url: "https://pgflow-dev.github.io/twitter-images/tweet-filename.png"
---
```

## Image Generation

Images are automatically generated using the Silicon tool via:

```bash
bin/gen-image-from-tweet-md path/to/tweet.md
```

This script:
1. Extracts code from the tweet's frontmatter
2. Generates a PNG image with syntax highlighting
3. Saves a copy in this directory
4. Updates the tweet's frontmatter with the correct GitHub Pages URL

## Workflow

After generating new images:
1. Commit and push this repository
2. Images will be available at `https://pgflow-dev.github.io/twitter-images/filename.png`

## Image Format

All images are generated with:
- Dracula theme for syntax highlighting
- No window controls
- Language-specific syntax highlighting based on the `language_for_image` field