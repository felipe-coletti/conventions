# Folder Structure

## Basic

For small, single-page projects with minimal CSS and JavaScript, where keeping files in the root directory is simpler than organizing them into separate folders.

```
main-folder/
├── assets/ # Banners, icons and logos
|   ├── icons/ # .ico
|   |   └── ...
|   ├── images/ # .jpg, .png...
|   |   └── ...
|   ├── svg/ # .svg
|   |   └── ...
|   └── ...
├── index.html # Single page
├── style.css
└── script.js
```

## Mid

For small to medium-sized projects with multiple HTML pages or enough CSS and JavaScript files to benefit from separating them into dedicated directories.

```
main-folder/
├── assets/ # Banners, icons and logos
|   ├── icons/ # .ico
|   |   └── ...
|   ├── images/ # .jpg, .png...
|   |   └── ...
|   ├── svg/ # .svg
|   |   └── ...
|   └── ...
├── css/ # CSS files
|   ├── style.css # or global.css, if there are other stylesh
|   └── ...
├── js/ # JavaScript files
|   ├── script.js # or main.js, if there are other scripts
|   └── ...
├── index.html # Main page
└── another-page.html
```

## Advanced

For larger projects with multiple components, pages, styles, and scripts, where grouping source files by responsibility improves organization and maintainability.

This structure is particularly suitable for projects that use a build process to bundle, transform, or optimize source files for production.

```
main-folder/
├── src/ # Source files
|   ├── assets/ # Banners, icons and logos
|   |   ├── icons/ # .ico
|   |   |   └── ...
|   |   ├── images/ # .jpg, .png...
|   |   |   └── ...
|   |   ├── svg/ # .svg
|   |   |   └── ...
|   |   └── ...
|   ├── components/
|   |   ├── component.js
|   |   ├── another-component.js
|   |   └── ...
|   ├── pages/
|   |   ├── another-page.html
|   |   └── ...
|   ├── styles/
|   |   ├── global.css
|   |   └── ...
|   └── scripts/
|       ├── main.js
|       └── ...
└── index.html # Main page
```