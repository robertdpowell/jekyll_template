# Jekyll Template

This repository contains a Jekyll template designed for building clean, minimal, and modern websites. The template is structured to separate content, layout, and assets for maintainability, and it leverages SCSS and Bootstrap for responsive and customizable design.

## Features

- **Global Settings**: Managed through `_config.yml`.
- **Reusable Components**: Includes reusable components in `_includes` and `_layouts`.
- **Blog Content**: Blog posts are stored in the `_posts` directory.
- **Generated Output**: The `_site` directory contains the generated output ready for deployment.
- **SCSS and Bootstrap**: Focus on responsive and customizable design.
- **Custom SASS**: Modular SASS files for banners, footers, and navigation.

## Folder Structure

- `_config.yml`: Global configuration file.
- `_includes/`: Contains reusable HTML components (e.g., `banner.html`, `footer.html`).
- `_layouts/`: Defines page layouts (e.g., `default.html`).
- `_posts/`: Stores blog posts.
- `_site/`: Generated output for deployment.
- `css/`: Contains SCSS files and Bootstrap styles.
- `custom/`: Contains custom SASS files for variables and includes.
- `img/`: Stores images.
- `js/`: Stores JavaScript files.
- `vendor/`: Contains third-party dependencies.

## How to Use

1. **Install Dependencies**:
   ```bash
   bundle install
   ```

2. **Build the Site**:
   ```bash
   bundle exec jekyll build
   ```

3. **Serve the Site Locally**:
   ```bash
   bundle exec jekyll serve
   ```
   The site will be available at `http://localhost:4000`.

4. **Deploy**:
   The contents of the `_site` directory can be deployed to any web server or hosting platform.

## Customization

### SASS Files

The template uses SASS for styling. Partials (files prefixed with an underscore, like `_variables.sass`) are imported into a main SASS file using the `@import` directive. Example:

```sass
@import 'custom/variables';
@import 'custom/includes/banner';
@import 'custom/includes/footer';
@import 'custom/includes/nav';
```

### SASS Indentation Syntax

The `.sass` files use the SASS indentation syntax, which differs from SCSS:

- No curly braces (`{}`): Indentation is used to define nested rules.
- No semicolons (`;`): Statements do not end with semicolons.
- No colons for properties: Property-value pairs are written without colons.

Example:

```sass
$primary-color: #333
body
  font-family: Arial, sans-serif
  color: $primary-color
```

