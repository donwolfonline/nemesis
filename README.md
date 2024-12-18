# Nemesis - Minimal Blog HTML Template

A modern, responsive, and feature-rich blog template built with HTML5, CSS3, and JavaScript.

![Nemesis Blog Template](./images/logo_nemesis.png)

## 🌟 Features

- 📱 Fully Responsive Design
- 🎨 Multiple Page Layouts
- 🔍 Search Functionality
- 📦 Category System
- 💬 Comment System
- 🖼️ Image Lazy Loading
- 🎠 Animated Slider/Carousel
- 📱 Mobile-First Approach
- 🌓 Dark Footer Section
- 🔗 Social Media Integration
- 📍 Sticky Navigation
- ⚡ Fast Loading Performance

## 🎯 Who Should Use This?

- Bloggers and content creators
- Personal portfolio websites
- Magazine-style websites
- News websites
- Content-driven platforms

## 🔧 Tech Stack

- HTML5
- CSS3/SCSS
- JavaScript/jQuery
- Bootstrap 4
- Font Awesome Icons
- Google Fonts
- Modern Browser APIs

## 📋 Prerequisites

- Basic knowledge of HTML, CSS, and JavaScript
- Code editor (VS Code, Sublime Text, etc.)
- Local development server (Live Server, XAMPP, etc.)
- Node.js (for SCSS compilation)

## 🚀 Quick Start

1. Clone the repository:
   ```bash
   git clone https://github.com/donwolfonline/nemesis.git
   ```

2. Navigate to the project directory:
   ```bash
   cd nemesis
   ```

3. Open index.html in your browser or use a local development server.

## 💻 Local Development Setup

1. Install a local development server:
   - VS Code users can install the "Live Server" extension
   - Or use XAMPP/MAMP for PHP development

2. For SCSS development:
   ```bash
   # Install Node.js from https://nodejs.org/
   
   # Install SASS globally
   npm install -g sass
   
   # Watch SCSS files
   sass --watch css/style.scss css/style.css
   ```

3. Start your local server and open the project in your browser.

## 📁 Project Structure

```
nemesis/
├── css/
│   ├── scss/
│   ├── style.scss
│   ├── style.css
│   └── bootstrap.min.css
├── js/
│   ├── main.js
│   ├── plugins.js
│   └── jquery.min.js
├── images/
├── fonts/
└── *.html
```

## 📄 Available Pages

- Home Page (index.html)
- Blog List (blog.html, blog-2.html)
- Single Post (single.html, single-2.html, single-3.html)
- Contact Page (contact.html)
- Error Page (error.html)
- Multiple Homepage Variations (index-2.html through index-8.html)

## 🛠️ Customization

1. **Styling**: 
   - Modify `css/style.scss` for custom styles
   - Update variables in SCSS files for global changes

2. **Layout**: 
   - Edit HTML files directly
   - Modify Bootstrap classes for layout changes

3. **Features**:
   - Configure sliders in `js/main.js`
   - Customize navigation in HTML files
   - Modify search functionality in JavaScript

## 🚀 Deployment

1. **Build Process**:
   ```bash
   # Compile SCSS to CSS
   sass css/style.scss css/style.css --style compressed
   
   # Minify JavaScript (using terser)
   npm install -g terser
   terser js/main.js -o js/main.min.js
   ```

2. **Deployment Options**:
   - Static hosting (Netlify, GitHub Pages, Vercel)
   - Traditional web hosting
   - CDN deployment

3. **For GitHub Pages**:
   ```bash
   git add .
   git commit -m "Deploy to GitHub Pages"
   git push origin main
   ```

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

- Create an issue in the GitHub repository
- Email: hi@frederickdineen.com
- Documentation: Wiki https://github.com/donwolfonline/nemesis/blob/main/docs/WIKI.md

## 🙏 Acknowledgments

- Bootstrap Team
- jQuery Team
- Font Awesome
- Google Fonts
- All contributors and supporters
