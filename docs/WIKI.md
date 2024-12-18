# Nemesis Blog Template - Technical Documentation

## Table of Contents
- [System Requirements](#system-requirements)
- [Development Environment](#development-environment)
- [Project Architecture](#project-architecture)
- [Technical Specifications](#technical-specifications)
- [Server Configuration](#server-configuration)
- [Performance Optimization](#performance-optimization)
- [Security Considerations](#security-considerations)
- [Troubleshooting](#troubleshooting)
- [API Documentation](#api-documentation)

## System Requirements

### Minimum Requirements
- **Server**: Any static file server (Apache, Nginx, etc.)
- **PHP Version**: Not required (static HTML)
- **Memory**: 512MB RAM (minimum)
- **Storage**: 100MB for base installation
- **Bandwidth**: Depends on traffic and asset optimization

### Recommended Requirements
- **Server**: Nginx with HTTP/2 support
- **Memory**: 1GB RAM or higher
- **Storage**: 500MB for full installation with sample content
- **CDN**: Recommended for production use
- **SSL**: Required for secure connections

## Development Environment

### Required Software
1. **Code Editor**
   - Visual Studio Code (recommended)
   - Sublime Text
   - Atom
   - WebStorm

2. **Development Tools**
   ```bash
   # Node.js (v14.0.0 or higher)
   node -v
   
   # npm (v6.0.0 or higher)
   npm -v
   
   # SASS Compiler
   npm install -g sass
   
   # Live Server
   npm install -g live-server
   ```

3. **Browser Developer Tools**
   - Chrome DevTools
   - Firefox Developer Tools
   - Safari Web Inspector

### Development Setup
1. **Local Server Configuration**
   ```apache
   # Apache .htaccess
   <IfModule mod_rewrite.c>
       RewriteEngine On
       RewriteCond %{HTTPS} off
       RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
   </IfModule>
   ```

2. **SASS Watch Configuration**
   ```bash
   # Watch SCSS files
   sass --watch css/scss:css --style compressed
   ```

## Project Architecture

### Directory Structure
```
nemesis/
├── css/
│   ├── scss/
│   │   ├── base/
│   │   ├── layout/
│   │   ├── magazine-blocks/
│   │   └── widgets/
│   ├── style.scss
│   └── style.css
├── js/
│   ├── main.js
│   └── plugins.js
├── images/
├── fonts/
└── templates/
```

### Component Architecture
1. **Layout Components**
   - Header Navigation
   - Slider System
   - Content Grid
   - Sidebar Widgets
   - Footer Blocks

2. **Magazine Blocks**
   - Featured Posts
   - Category Blocks
   - Newsletter Forms
   - Social Media Widgets

## Technical Specifications

### CSS Architecture
1. **SCSS Structure**
   - Base styles
   - Layout components
   - Magazine blocks
   - Widget styles
   - Responsive utilities

2. **CSS Methodology**
   - BEM naming convention
   - Mobile-first approach
   - Modular architecture
   - CSS Grid & Flexbox

### JavaScript Components
1. **Core Functions**
   ```javascript
   // Sticky Navigation
   .fbt_sticky_nav
   
   // Search Functionality
   #search
   
   // Slider Animation
   #TopSliderPosts
   ```

2. **Event Handlers**
   - Scroll events
   - Click handlers
   - Form submissions
   - Animation triggers

## Server Configuration

### Apache Configuration
```apache
# Security Headers
<IfModule mod_headers.c>
    Header set X-Content-Type-Options "nosniff"
    Header set X-Frame-Options "SAMEORIGIN"
    Header set X-XSS-Protection "1; mode=block"
    Header set Referrer-Policy "strict-origin-when-cross-origin"
</IfModule>

# Caching Rules
<IfModule mod_expires.c>
    ExpiresActive On
    ExpiresByType image/jpeg "access plus 1 year"
    ExpiresByType image/png "access plus 1 year"
    ExpiresByType text/css "access plus 1 month"
    ExpiresByType text/javascript "access plus 1 month"
</IfModule>
```

### Nginx Configuration
```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /path/to/nemesis;
    
    location / {
        try_files $uri $uri/ /index.html;
    }
    
    # Caching Headers
    location ~* \.(jpg|jpeg|png|gif|ico|css|js)$ {
        expires 1y;
        add_header Cache-Control "public, no-transform";
    }
}
```

## Performance Optimization

### Image Optimization
1. **Formats & Compression**
   - JPEG for photographs
   - PNG for graphics
   - WebP with fallbacks
   - Responsive images

2. **Lazy Loading**
   ```html
   <img class="lazyloaded" 
        data-src="image.jpg"
        alt="Description">
   ```

### Code Optimization
1. **CSS Minification**
   ```bash
   sass css/style.scss:css/style.min.css --style compressed
   ```

2. **JavaScript Minification**
   ```bash
   terser js/main.js -o js/main.min.js
   ```

## Security Considerations

### Content Security Policy
```html
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self'; 
               img-src 'self' data: https:; 
               style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; 
               script-src 'self' 'unsafe-inline' 'unsafe-eval';">
```

### Form Security
1. **Input Validation**
2. **CSRF Protection**
3. **XSS Prevention**

## Troubleshooting

### Common Issues
1. **Slider Not Working**
   - Check jQuery loading
   - Verify slider initialization
   - Console for errors

2. **CSS Not Updating**
   - Clear browser cache
   - Check SASS compilation
   - Verify file paths

3. **Mobile Menu Issues**
   - Check Bootstrap integration
   - Verify JavaScript events
   - Test viewport settings

## API Documentation

### Search API
```javascript
// Search Trigger
$(".search-trigger").on('click', function() {
    $("#search").addClass("active");
});
```

### Slider API
```javascript
// Slider Configuration
$('#TopSliderPosts').carousel({
    interval: 5000,
    pause: 'hover'
});
```

### Comment System
```javascript
// Comment Toggle
$('.fbt-comment-button').on('click', function() {
    $('.comment-list').slideToggle();
});
```

## Version History

### Current Version: 1.0.0
- Initial release
- Full responsive design
- Multiple page templates
- Magazine blocks
- Widget system

### Planned Updates
1. **Version 1.1.0**
   - Dark mode support
   - Enhanced performance
   - Additional widgets
   - Improved accessibility

2. **Version 1.2.0**
   - PWA support
   - Advanced caching
   - New page templates
   - Enhanced animations
