# HoJin Choi - Flight Data Analyst & AI Engineer Portfolio

A professional portfolio website for HoJin Choi, showcasing expertise in flight data analysis, AI/ML engineering, and statistical analysis.

## 🌟 Overview

This is a modern, responsive portfolio website built for GitHub Pages deployment. It showcases professional experience, education, technical skills, and projects in aviation data analysis and AI engineering.

**Live Website**: [View Portfolio](https://gansaw12.github.io/pages)

## 🛠️ Features

- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Modern UI/UX**: Clean, professional design with aviation-themed color scheme
- **Interactive Elements**: Smooth animations, hover effects, and modal popups
- **Project Filtering**: Filter projects by category (Aviation, AI/ML, Data Analysis)
- **Smooth Scrolling**: Navigation with smooth scroll to sections
- **Contact Form**: Interactive contact form (frontend only)

## 📋 Sections

1. **Hero Section**: Professional introduction with call-to-action buttons
2. **About**: Personal introduction and core expertise
3. **Technical Skills**: Categorized technical competencies
4. **Education**: Academic background and training history
5. **Projects**: Portfolio of aviation and AI/ML projects
6. **Certificates**: Professional certifications
7. **Contact**: Contact information and message form

## 🚀 Technologies Used

### Frontend
- HTML5
- CSS3 (Flexbox, Grid, Custom Properties)
- Vanilla JavaScript (ES6+)
- Font Awesome Icons
- Google Fonts (Inter)

### Deployment
- GitHub Pages

## 📁 Project Structure

```
portfolio/
├── index.html      # Main HTML file
├── style.css      # Stylesheet
├── script.js      # JavaScript functionality
└── README.md      # Project documentation
```

## 🎯 Project Categories

### Aviation Projects
- Flight Delay Prediction System
- Aircraft Engine Health Monitoring  
- Aviation Safety Analytics Dashboard
- Fuel Efficiency Optimization

### AI/ML Projects
- Aircraft Engine Health Monitoring
- Passenger Behavior Analysis
- Air Traffic Flow Forecasting

### Data Analysis Projects
- Flight Route Optimization
- Weather Impact on Flight Operations

## 🛠️ Setup for Local Development

1. Clone the repository:
```bash
git clone https://github.com/yourusername/portfolio.git
cd portfolio
```

2. Open `index.html` in your browser or use a local server:
```bash
python -m http.server 8080
```

3. Visit `http://localhost:8080` to view the website

## 🚀 Deployment to GitHub Pages

1. **Fork or create a new repository** on GitHub

2. **Upload all files** to your repository:
   - `index.html`
   - `style.css` 
   - `script.js`
   - `README.md`

3. **Enable GitHub Pages**:
   - Go to your repository Settings
   - Scroll down to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click Save

4. **Access your website**:
   - Your site will be available at: `https://yourusername.github.io/repository-name`
   - It may take a few minutes to deploy

## 🎨 Customization

### Personal Information
Update the following in `index.html`:
- Name and title in header
- About section content
- Contact information
- Education details

### Projects
Modify the `projects` array in `script.js` to add your own projects:
```javascript
{
    id: 1,
    title: "Your Project Title",
    description: "Project description...",
    type: "aviation", // aviation, ai, data
    tech: ["Python", "TensorFlow"],
    icon: "fas fa-icon-name",
    details: {
        problem: "Problem statement...",
        solution: "Your solution...",
        result: "Results achieved..."
    }
}
```

### Colors and Styling
Modify CSS variables in `style.css`:
```css
:root {
    --primary-color: #your-color;
    --secondary-color: #your-color;
    --aviation-blue: #1e3a8a; /* Aviation theme color */
}
```

## 📱 Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 📊 Performance

- Optimized CSS with minimal custom properties
- Efficient JavaScript with modern ES6+ features
- Responsive images using CSS
- Lazy loading for better performance

## 🔧 Customization Tips

### Adding New Projects
1. Add project object to `projects` array in `script.js`
2. Choose appropriate type: "aviation", "ai", or "data"
3. Select relevant icon from Font Awesome
4. Include comprehensive details

### Changing Colors
Modify the CSS variables in `:root` to match your preferred color scheme

### Adding New Sections
1. Add HTML structure in `index.html`
2. Add corresponding CSS in `style.css`
3. Add JavaScript functionality in `script.js`
4. Update navigation menu

## 📞 Contact Information Updates

Replace placeholder contact information in:
- Contact form section
- Footer section
- Social media links

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Contact

- Email: gansaw12@gmail.com
