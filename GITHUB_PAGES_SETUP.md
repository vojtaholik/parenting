# GitHub Pages Setup Instructions

This repository is configured to use Docsify for GitHub Pages deployment.

## Enabling GitHub Pages

To activate GitHub Pages for this repository:

1. Go to the repository settings on GitHub
2. Navigate to "Pages" in the left sidebar
3. Under "Source", select:
   - **Branch**: `main` (or your default branch)
   - **Folder**: `/docs`
4. Click "Save"

GitHub will automatically deploy the documentation site within a few minutes.

## Accessing the Site

Once enabled, the site will be available at:
- `https://vojtaholik.github.io/parenting/`

## How It Works

- **Docsify**: A lightweight documentation generator that renders markdown files on-the-fly
- **index.html**: The main entry point that loads Docsify
- **_sidebar.md**: Navigation sidebar with categorized links to all content
- **README.md**: The homepage/landing page
- **.nojekyll**: Tells GitHub Pages not to process files with Jekyll

## Local Development

To preview the site locally:

```bash
# Navigate to the docs folder
cd docs

# Start a simple HTTP server
python3 -m http.server 8080

# Or use Node.js
npx serve

# Or use docsify-cli
npm i docsify-cli -g
docsify serve docs
```

Then open `http://localhost:8080` in your browser.

## File Structure

```
docs/
├── index.html              # Docsify configuration
├── _sidebar.md             # Navigation menu
├── README.md               # Homepage
├── .nojekyll               # Disable Jekyll
├── practical-tips.md
├── developmental-theories/
│   ├── README.md
│   ├── piaget.md
│   ├── vygotsky.md
│   ├── attachment-theory.md
│   └── erikson.md
├── parenting-styles/
│   ├── README.md
│   ├── authoritative.md
│   ├── authoritarian.md
│   ├── permissive.md
│   └── comparison-matrix.md
├── practical-domains/
│   ├── README.md
│   ├── sleep.md
│   ├── nutrition.md
│   ├── language-development.md
│   ├── cognitive-stimulation.md
│   ├── emotional-regulation.md
│   ├── play.md
│   └── discipline.md
└── programs/
    ├── README.md
    ├── montessori.md
    ├── positive-discipline.md
    ├── rie.md
    └── circle-of-security.md
```

## Updating Content

All content is duplicated from the root directory to the `docs/` folder. To update content:

1. Edit the markdown files in the root directory (e.g., `developmental-theories/piaget.md`)
2. Copy the updated files to the `docs/` folder
3. Commit and push changes

Alternatively, you can maintain content only in the `docs/` folder and remove duplicates from the root.

## Customization

You can customize Docsify by editing `docs/index.html`:
- Change the theme
- Add plugins (search, zoom images, copy code, etc.)
- Modify navigation behavior
- Add custom styling

See [Docsify documentation](https://docsify.js.org/) for more options.
