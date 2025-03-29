## Jekyll Site structure

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



## Site design
All sites built from this template should be clean, minimal modern but beautiful. Where colour is used, we like pastels.


