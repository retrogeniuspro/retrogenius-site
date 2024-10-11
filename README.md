# RETROGENius GitHub Pages Website

This repository contains the source code for RETROGENius website hosted on GitHub Pages.

## Getting Started

To set up and run this website locally, follow these steps:

1. Clone this repository:
   ```bash
   git clone https://github.com/retrogeniuspro/site.git
   ```

2. Navigate to the project directory:
   ```
   cd site
   ```

3. Install Jekyll and dependencies with docker:
   ```bash
   docker pull jekyll/jekyll:3.8
   ``` 

4. Create a new Jekyll site:
   ```bash
   docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:3.8 jekyll new .
   ```


5. Build the site locally:
   ```bash
   docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:3.5 jekyll build
   ```

6. Serve the site locally:
   ```bash
   docker run --rm name site --volume="$PWD:/srv/jekyll" -p 8081:4000 -it jekyll/jekyll:3.5 jekyll serve --watch --drafts
   ```


7. Open your browser and visit `http://localhost:8081` to view the site.

## Customization

- Edit the `_config.yml` file to update site-wide settings.
- Modify or add Markdown files in the root directory or in `_posts/` for blog posts.
- Update the `assets/` directory for images, CSS, and JavaScript files.

## Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the `main` branch.
