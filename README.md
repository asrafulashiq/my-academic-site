# Ashraful Islam - Personal Academic Website

This is the source repository for my personal academic website hosted at [asrafulashiq.github.io](https://asrafulashiq.github.io/).

Built with [Hugo](https://gohugo.io/) and [HugoBlox](https://hugoblox.com/) (formerly Wowchemy Academic).

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
│   ├── params.yaml      # Theme parameters
│   ├── menus.yaml       # Navigation menus
│   └── languages.yaml   # Language settings
├── content/             # Website content (Markdown)
│   ├── authors/         # Author profiles
│   ├── home/            # Homepage widgets
│   ├── publication/     # Publications
│   └── project/         # Projects
├── assets/              # Images and media
├── static/              # Static files (copied as-is)
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

Edit files in the `content/` directory:

- **Profile**: `content/authors/admin/_index.md`
- **Homepage widgets**: `content/home/`
- **Publications**: `content/publication/`
- **Projects**: `content/project/`

### 4. Build the site

```bash
hugo
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

### Add a new publication

1. Create a new folder in `content/publication/`:
   ```bash
   mkdir content/publication/my-new-paper
   ```

2. Create `index.md` with front matter:
   ```yaml
   ---
   title: "Paper Title"
   authors:
     - admin
     - Co-Author Name
   date: "2024-01-01"
   publication_types: ["article-journal"]  # or "paper-conference"
   publication: "Conference/Journal Name"
   abstract: "Abstract text..."
   links:
     - type: pdf
       url: "paper.pdf"
     - type: code
       url: "https://github.com/..."
   ---
   ```

3. Add `featured.jpg` for thumbnail (optional)

### Update profile information

Edit `content/authors/admin/_index.md`

### Modify homepage sections

Edit files in `content/home/`:
- `about.md` - Bio section
- `experience.md` - Work experience
- `publications.md` - Publications widget
- `contact.md` - Contact info

## Troubleshooting

### TailwindCSS not found

Make sure to run `npm install` in the project directory:
```bash
npm install tailwindcss @tailwindcss/typography
```

### Module download fails

Ensure Go is installed and run:
```bash
hugo mod get -u
```

### Submodule issues

```bash
git submodule update --init --recursive
```

### Deprecated warnings

The content uses some deprecated front matter keys. These are warnings only and don't affect the build. To fix them:
- Replace `url_pdf`, `url_code`, etc. with `links: [{type: pdf, url: ...}]` format
- Replace `_build` with `build` in front matter

## License

Content is copyright Ashraful Islam. The HugoBlox theme is licensed under MIT.
