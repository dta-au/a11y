# GitHub Pages Jekyll Site with GitHub Actions

This repository contains a template for creating a GitHub Pages site using Jekyll and GitHub Actions. It uses the Just the Docs theme and includes a basic structure for a documentation site with a blog.

## Setup Instructions

1. **Create a new repository**
   - Go to GitHub and create a new repository.
   - You can name it anything you like, but `<username>.github.io` will create a user or organization site.

2. **Clone the repository**
   ```bash
   git clone https://github.com/<username>/<repository-name>.git
   cd <repository-name>
   ```

3. **Add template files**
   - Copy the following files into your repository:
     - `_config.yml`
     - `index.md`
     - `about.md`
     - `blog.md`
     - `.github/workflows/github-pages.yml`
     - `Gemfile`

4. **Create necessary directories**
   ```bash
   mkdir _posts _docs
   ```

5. **Configure GitHub Pages**
   - Go to your repository on GitHub
   - Navigate to Settings > Pages
   - For "Source", select "GitHub Actions"

6. **Create gh-pages branch**
   ```bash
   git checkout -b gh-pages
   git push origin gh-pages
   ```

7. **Commit and push your changes**
   ```bash
   git add .
   git commit -m "Initial commit with Jekyll structure and GitHub Actions"
   git push origin main
   ```

8. **Wait for GitHub Actions to build and deploy**
   - Go to the "Actions" tab in your repository to monitor the progress
   - Once complete, your site will be live at `https://<username>.github.io/<repository-name>`

## Customization

1. **Theme customization**
   - Create a `_sass` directory for custom SCSS files
   - Override theme variables or add your own styles

2. **Navigation**
   - Modify the `nav` section in `_config.yml` to update the site navigation

3. **Content**
   - Add new markdown files to the root directory or `_docs` for new pages
   - Add new blog posts as markdown files in the `_posts` directory, named `YYYY-MM-DD-title.md`

4. **Front Matter**
   - Use front matter in your markdown files to control page-specific settings
   - Example:
     ```yaml
     ---
     layout: page
     title: My New Page
     nav_order: 4
     ---
     ```

5. **Custom Plugins**
   - Add desired Jekyll plugins to your `Gemfile`
   - Update `_config.yml` to include new plugins

## File Structure

```
.
├── _config.yml
├── _posts/
│   └── YYYY-MM-DD-example-post.md
├── _docs/
│   └── example-doc.md
├── .github/
│   └── workflows/
│       └── github-pages.yml
├── Gemfile
├── index.md
├── about.md
└── blog.md
```

## Additional Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Just the Docs Theme](https://just-the-docs.github.io/just-the-docs/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## Support

If you encounter any issues or have questions, please open an issue in this repository.

Happy coding!