## Jekyll Site structure

This file is to provide context to your AI code assistant of choice, to explain how to build out the site.

This Jekyll template is structured to separate content, layout, and assets for maintainability. The _config.yml file controls global settings, _includes and _layouts manage reusable components and page structure, _posts handles blog content, and _site is the generated output ready for deployment. The use of SCSS and Bootstrap indicates a focus on responsive and customizable design.

The custom folder contains a _variables.sass file and an includes/ subfolder. The includes/ folder contains additional SASS files: _banner.sass, _footer.sass, and _nav.sass.

How SASS Files Are Imported
In SASS, partials (files prefixed with an underscore, like _variables.sass) are typically imported into a main SASS file using the @import directive. For example:

```
@import 'custom/variables';
@import 'custom/includes/banner';
@import 'custom/includes/footer';
@import 'custom/includes/nav';
```

This approach allows modular organization of styles, where each file handles a specific aspect of the design (e.g., variables, banners, footers, navigation).

SASS Indentation Syntax
The .sass files in this folder use the SASS indentation syntax, which is an alternative to SCSS. Key differences include:

No Curly Braces: Instead of {}, indentation is used to define nested rules.
No Semicolons: Statements do not end with ;.
No Colons for Properties: Property-value pairs are written without colons.
Example:

```
$primary-color: #333
body
  font-family: Arial, sans-serif
  color: $primary-color
```

We use a data-driven approach, separating content from presentation for easy maintenance and updates.

This template uses a `_data/settings.yml` file to centralize all site content, making it easy to update information without touching HTML or CSS files. This approach offers several advantages:

### Key Benefits

1. **Separation of Content and Presentation**: All content lives in the YAML data file, completely separate from HTML templates
2. **Single Source of Truth**: Update your information in one place and see changes reflected throughout the site
3. **Easy Maintenance**: Non-technical users can update content without understanding HTML or Jekyll templates
4. **Consistent Structure**: Content follows a well-defined schema, ensuring consistency across sections

### Structure of settings.yml

The `settings.yml` file is organized into logical sections that correspond to the site's components. For example for a resume site we might see in our settings.yml

```
about:
  title: "About Me"
  content: [...]
  highlights: [...]

experience:
  title: "Work Experience"
  jobs: [...]

# and so on...
```

Each HTML template in the `_includes` directory uses Liquid template tags to access data from `settings.yml`. For example:

```html
<h1>{{ site.data.settings.banner.title }}</h1>
<p>{{ site.data.settings.banner.tagline }}</p>

{% for job in site.data.settings.experience.jobs %}
  <div class="job-item">
    <h3>{{ job.position }}</h3>
    <!-- More job details -->
  </div>
{% endfor %}
```


