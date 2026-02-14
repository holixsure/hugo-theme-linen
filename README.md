# Linen Hugo Theme

A minimalist Hugo theme with dark mode support, responsive design, and clean aesthetics.

## Features

- **Minimalist Design**: Follows the "less is more" principle, reducing visual noise and ensuring clear readability
- **Dark Mode**: Complete black/white/light/dark display mode switching functionality, including automatic system preference detection and manual toggle button
- **Responsive Design**: Ensures good display effect and user experience on desktop, tablet, and mobile devices
- **Customizable**: Provides reasonable configuration options, allowing users to customize basic colors, fonts, layouts, etc.
- **Performance Optimized**: Optimizes CSS/JS resource loading, ensures fast page loading speed, and meets modern web performance standards
- **Complete Components**: Includes necessary theme components (navigation bar, article list, content page, sidebar, footer, etc.)

## Installation

1. **Clone the theme into your Hugo site's themes directory**:
   ```bash
   git clone git@github.com:holixsure/hugo-theme-linen.git themes/linen
   ```

2. **Add the theme to your Hugo configuration file** (`config.toml`):
   ```toml
   theme = "linen"
   ```

## Configuration

Here's an example `config.toml` file with the theme's configuration options:

```toml
baseURL = "http://example.org/"
languageCode = "en-us"
title = "My Hugo Site"

[params]
  # Site settings
  description = "A minimalist Hugo site"
  author = "John Doe"
  
  # Theme customization
  [params.linen]
    # Color scheme (light or dark)
    defaultTheme = "light"
    
    # Navigation
    [params.linen.navigation]
      logo = ""
      logoText = "Linen"
      showMenu = true
      
    # Sidebar
    [params.linen.sidebar]
      enabled = true
      position = "right" # left or right
      
    # Footer
    [params.linen.footer]
      showCopyright = true
      copyrightText = "© 2024 All rights reserved"
      showSocial = false
      
      [params.linen.footer.social]
        twitter = ""
        github = ""
        linkedin = ""
```

## Usage

### Adding Menu Items

Add menu items to your `config.toml` file:

```toml
[[menu.main]]
  name = "Home"
  url = "/"
  weight = 1

[[menu.main]]
  name = "About"
  url = "/about/"
  weight = 2

[[menu.main]]
  name = "Posts"
  url = "/posts/"
  weight = 3
```

### Creating Content

Create content files in the `content` directory:

```markdown
---
title: "My First Post"
date: 2024-01-01T00:00:00Z
categories:
  - Blog
tags:
  - Hugo
  - Theme
---

This is my first post using the Linen theme.
```

## Customization

### Color Scheme

The theme uses CSS variables for color management. You can customize the colors in `static/css/main.css`:

```css
:root {
  /* Light mode variables */
  --bg-color: #ffffff;
  --text-color: #333333;
  --secondary-text: #666666;
  --border-color: #e5e5e5;
  --accent-color: #0066cc;
  --hover-color: #f5f5f5;
  --card-bg: #ffffff;
  --sidebar-bg: #f9f9f9;
}

/* Dark mode variables */
[data-theme="dark"] {
  --bg-color: #1a1a1a;
  --text-color: #e0e0e0;
  --secondary-text: #b0b0b0;
  --border-color: #333333;
  --accent-color: #4da6ff;
  --hover-color: #2a2a2a;
  --card-bg: #252525;
  --sidebar-bg: #2a2a2a;
}
```

### Fonts

You can customize the fonts in `static/css/main.css`:

```css
body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  /* Other styles */
}
```

## Performance Optimization

The theme includes several performance optimizations:

- **Minified CSS/JS**: The theme's CSS and JS files are minified for faster loading
- **Deferred JS Loading**: JavaScript is loaded with the `defer` attribute to avoid blocking page rendering
- **Responsive Images**: The theme automatically handles responsive images
- **System Font Stack**: Uses system fonts for faster loading and better performance

## Browser Compatibility

The theme is compatible with all modern browsers, including:

- Chrome
- Firefox
- Safari
- Edge

## License

MIT License

## Acknowledgements

The theme is inspired by several mainstream minimalist Hugo themes, including:

- PaperMod
- Even
- Congo

However, the code implementation is original and follows the "less is more" design principle.
