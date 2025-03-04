# HomeBuilderBlinds-Website

A modern, high-performance website for Home Builder Blinds built with HTML, CSS, and vanilla JavaScript. This project creates a professional web presence that maintains visual consistency with our operations suite while providing an optimal user experience.

## 🌟 Overview

This website serves as the public-facing platform for Home Builder Blinds, showcasing our products, services, and expertise in the window treatment industry. Built with clean, efficient code and modern web standards, it provides a seamless experience for visitors while maintaining the same look and feel as our internal systems.

## 🛠️ Technology Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Backend**: Node.js with Express.js
- **Build Tools**: Vite for modern development experience
- **Deployment**: ************

## 📂 Project Structure

```
HomeBuilderBlinds-Website/
├── public/              # Static assets
│   ├── css/
│   │   ├── main.css     # Primary styles
│   │   ├── shared.css   # Styles shared with operations suite
│   │   └── normalize.css # Cross-browser consistency
│   ├── js/
│   │   ├── main.js      # Main JavaScript file
│   │   └── modules/     # Modular JS functionality
│   │       ├── navigation.js
│   │       ├── animations.js
│   │       └── form-handlers.js
│   ├── images/
│   └── fonts/
├── views/               # HTML templates
│   ├── partials/        # Reusable HTML components
│   │   ├── header.html
│   │   ├── navigation.html
│   │   └── footer.html
│   ├── index.html
│   └── pages/
│       ├── products.html
│       ├── services.html
│       ├── about.html
│       └── contact.html
├── server.js            # Node.js Express server
├── package.json
└── README.md
```


## 📱 Design Philosophy

### Visual Consistency
Our website maintains visual consistency with our operations suite through:
- Shared color schemes and typography
- Consistent navigation patterns and UI components
- Familiar layout structures and interaction patterns

### Key UI Components
- Responsive navigation bar with dropdown menus
- Product galleries with filtering options
- Contact forms with validation
- Quote request system
- Location maps and store finder

### Performance Optimization
- Optimized image loading with responsive sizes
- Lazy loading for below-the-fold content
- Minimal JavaScript with efficient DOM operations
- Critical CSS inlining for faster initial render

## 🔄 Server Implementation

The Express.js server provides:

```javascript
const express = require('express');
const path = require('path');
const app = express();
const port = process.env.PORT || 3000;

// Serve static files
app.use(express.static(path.join(__dirname, 'public')));

// Basic route for the home page
app.get('/', (req, res) => {
  res.sendFile(path.join(__dirname, 'views', 'index.html'));
});

// Additional routes for other pages
app.get('/products', (req, res) => {
  res.sendFile(path.join(__dirname, 'views', 'pages', 'products.html'));
});

app.get('/services', (req, res) => {
  res.sendFile(path.join(__dirname, 'views', 'pages', 'services.html'));
});

app.get('/about', (req, res) => {
  res.sendFile(path.join(__dirname, 'views', 'pages', 'about.html'));
});

app.get('/contact', (req, res) => {
  res.sendFile(path.join(__dirname, 'views', 'pages', 'contact.html'));
});

// API endpoints for form submissions
app.post('/api/contact', express.json(), (req, res) => {
  // Process contact form data
  console.log('Contact form submission:', req.body);
  res.json({ success: true });
});

app.post('/api/quote', express.json(), (req, res) => {
  // Process quote request
  console.log('Quote request:', req.body);
  res.json({ success: true });
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
```

## 📊 Business Integration

The website connects with other HomeBuilderBlinds systems:

```
┌─────────────────────┐      ┌─────────────────────┐
│                     │      │                     │
│  HBB-Website        │◄────►│  HBB-Marketing      │
│  (Public Interface) │      │  (CRM & Campaigns)  │
│                     │      │                     │
└─────────────────────┘      └─────────┬───────────┘
                                        │
                                        │
                                        ▼
              ┌─────────────────────────────────────┐
              │                                     │
              │          HBB-Operations             │
              │     (Order & Work Management)       │
              │                                     │
              └─────────────────────────────────────┘
```

## 🔍 SEO Optimization

- Semantic HTML structure for better search engine understanding
- Optimized metadata for each page
- Structured data for products and services
- Performance optimization for improved search rankings
- Mobile-friendly responsive design

## 📱 Responsive Design

The website is fully responsive with:
- Fluid layouts that adapt to any screen size
- Touch-friendly navigation for mobile devices
- Optimized images for different viewport sizes
- Consistent experience across devices

## 📈 Analytics & Tracking

- Integration with Google Analytics for visitor insights
- Event tracking for key user interactions
- Conversion tracking for lead generation
- Heat maps for user behavior analysis
- A/B testing capabilities for optimization

## 🔒 Security Considerations

- HTTPS encryption for all traffic
- Input validation for all form submissions
- Protection against common web vulnerabilities
- Regular security updates and maintenance
- Privacy-compliant data handling

## 🛠️ Development Workflow

1. Create feature branches from `develop` branch
2. Implement changes and test locally
3. Submit pull requests for code review
4. Merge approved changes to `develop`
5. Deploy to staging environment for testing
6. Release to production via `main` branch

## 📋 Deployment

1. Build production assets:
   ```bash
   npm run build
   ```

2. Deploy to your hosting environment:
   ```bash
   npm run deploy
   ```

## 🔄 Maintenance

- Regular dependency updates
- Performance monitoring and optimization
- Content updates as needed
- Security patches and vulnerability fixes
- Browser compatibility checks

## 👥 Contributors
- Michael W. Gumfory
- Email: gumfory@gmail.com

## 📜 License
- Proprietary software for Home Builder Blinds
