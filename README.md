# Ashraful Islam - Personal Academic Website

This is the source repository for my personal academic website hosted at [asrafulashiq.github.io](https://asrafulashiq.github.io/).

Built with [Hugo](https://gohugo.io/) and the [Wowchemy Academic](https://wowchemy.com/) theme.

## Prerequisites

- **Hugo Extended v0.89.4** (required for compatibility with the Wowchemy theme)
- **Go** (for Hugo modules)

### Installing Hugo

This project requires Hugo v0.89.4 (extended) specifically. Newer versions have breaking changes with the Wowchemy theme.

**Option 1: Download directly (recommended)**
```bash
# macOS ARM64 (Apple Silicon)
curl -L https://github.com/gohugoio/hugo/releases/download/v0.89.4/hugo_extended_0.89.4_macOS-ARM64.tar.gz -o hugo.tar.gz
tar -xzf hugo.tar.gz hugo
mv hugo bin/hugo  # or /usr/local/bin/hugo

# macOS Intel
curl -L https://github.com/gohugoio/hugo/releases/download/v0.89.4/hugo_extended_0.89.4_macOS-64bit.tar.gz -o hugo.tar.gz
tar -xzf hugo.tar.gz hugo
mv hugo bin/hugo
```

**Option 2: Use the local binary (if already set up)**
```bash
./bin/hugo version
```

### Installing Go

```bash
brew install go
```

## Project Structure

```
my-academic-site/
├── config/_default/     # Site configuration
│   ├── config.yaml      # Main Hugo config
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
└── bin/                 # Local Hugo binary (gitignored)
```

## Development Workflow

### 1. Clone the repository

```bash
git clone https://github.com/asrafulashiq/my-academic-site.git
cd my-academic-site
git submodule update --init --recursive
```

### 2. Preview locally

```bash
./bin/hugo server
# Or if Hugo is in PATH: hugo server
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
./bin/hugo
# Or: hugo
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
   publication_types: ["1"]  # 1=Conference, 2=Journal
   publication: "Conference Name"
   abstract: "Abstract text..."
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

### Hugo version mismatch

If you see errors about `getenv` or `security.funcs`, you're using a newer Hugo version. This project requires Hugo v0.89.4.

### Module download fails

Ensure Go is installed:
```bash
go version
```

### Submodule issues

```bash
git submodule update --init --recursive
```

## License

Content is copyright Ashraful Islam. The Wowchemy theme is licensed under MIT.
