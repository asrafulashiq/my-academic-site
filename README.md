# Ashraful Islam - Personal Academic Website

This is the source repository for my personal academic website hosted at [asrafulashiq.github.io](https://asrafulashiq.github.io/).

Built with [Hugo](https://gohugo.io/) and [HugoBlox](https://hugoblox.com/) Resume theme.

## Prerequisites

- **Hugo Extended** (latest version)
- **Go** (for Hugo modules)
- **Node.js 18+** (for TailwindCSS)

### Install Dependencies

**macOS (using Homebrew):**
```bash
brew install hugo go node
```

**Install TailwindCSS (in project directory):**
```bash
cd my-academic-site
npm install
```

## Project Structure

```
my-academic-site/
├── config/_default/     # Site configuration
│   ├── hugo.yaml        # Main Hugo config
│   ├── params.yaml      # Theme parameters (identity, theme, layout)
│   └── menus.yaml       # Navigation menus
├── content/             # Website content (Markdown)
│   ├── _index.md        # Homepage with section blocks
│   └── publication/     # Publications
├── data/
│   └── authors/
│       └── admin.yaml   # Author profile (bio, experience, skills, education)
├── assets/media/        # Images (avatar, etc.)
├── static/              # Static files (copied as-is)
│   └── .nojekyll        # Disables Jekyll on GitHub Pages
├── public/              # Generated site (git submodule → asrafulashiq.github.io)
├── package.json         # Node.js dependencies (TailwindCSS)
└── go.mod               # Hugo module dependencies
```

## Development Workflow

### 1. Clone the repository

```bash
git clone https://github.com/asrafulashiq/my-academic-site.git
cd my-academic-site
git submodule update --init --recursive
npm install
```

### 2. Preview locally

```bash
hugo server
```

Open [http://localhost:1313](http://localhost:1313) in your browser.

### 3. Make changes

- **Profile/Bio**: `data/authors/admin.yaml`
- **Homepage sections**: `content/_index.md` (blocks: biography, experience, skills, publications, awards)
- **Publications**: `content/publication/`
- **Site config**: `config/_default/params.yaml`
- **Navigation**: `config/_default/menus.yaml`

### 4. Build the site

```bash
hugo --minify
```

### 5. Deploy to GitHub Pages

```bash
cd public
git add .
git commit -m "Update site"
git push origin main
cd ..
```

Or use the helper script:
```bash
./run_public.sh
```

## Common Tasks

### Update profile information

Edit `data/authors/admin.yaml`:
- `bio` - About me text
- `experience` - Work history
- `education` - Academic background
- `skills` - Technical skills
- `links` - Social/contact links

### Add a new publication

1. Create a new folder in `content/publication/`:
   ```bash
   mkdir content/publication/my-new-paper
   ```

2. Create `index.md` with front matter:
   ```yaml
   ---
   title: "Paper Title"
   authors: [A Author, B Author]
   date: "2024-01-01"
   publication_types: ["1"]  # 1=Conference, 2=Journal, 3=Preprint
   publication: "Conference/Journal Name"
   publication_short: "CONF"
   summary: "Brief description..."
   url_pdf: "https://arxiv.org/..."
   url_code: "https://github.com/..."
   ---
   ```

### Modify homepage sections

Edit `content/_index.md` to add/remove/reorder blocks:
- `biography` - Profile with avatar
- `experience` - Work history timeline
- `skills` - Technical skills
- `collection` - Publications list
- `awards` - Awards section

## Troubleshooting

### CSS not loading on GitHub Pages

Ensure `static/.nojekyll` exists. This file tells GitHub Pages to skip Jekyll processing (which ignores files starting with `_`).

### TailwindCSS not found

```bash
npm install
```

### Module download fails

```bash
hugo mod get -u
```

### Submodule issues

```bash
git submodule update --init --recursive
```

### Deprecated warnings

The content uses some deprecated front matter keys. These are warnings only and don't affect the build. To fix:
- Replace `url_pdf`, `url_code`, etc. with `links: [{type: pdf, url: ...}]` format

## License

Content is copyright Ashraful Islam. The HugoBlox theme is licensed under MIT.
