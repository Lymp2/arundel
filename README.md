# Liberal Democrats Local Division Website

A modern, responsive website for Liberal Democrats local divisions, built with Hugo and designed to emulate the style of the Horsham Liberal Democrats site.

## Features

- **Modern Design**: Clean, professional layout using Liberal Democrats branding colors
- **Responsive**: Mobile-friendly design that works on all devices
- **Fast Loading**: Built with Hugo for optimal performance
- **Easy to Customize**: Simple structure that's easy to modify
- **SEO Friendly**: Proper meta tags and structured content
- **Accessibility**: Built with accessibility best practices

## Getting Started

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (Extended version recommended)
- Git (for version control)

### Installation

1. Clone or download this repository
2. Navigate to the project directory
3. Run the development server:

```bash
hugo server -D
```

4. Open your browser to `http://localhost:1313`

## Site Structure

```
lybdems/
├── content/                 # Content pages
│   ├── news/               # News articles
│   ├── councils/           # Councillor information
│   ├── campaigns/          # Campaign details
│   ├── get-involved/       # Volunteer opportunities
│   ├── donate/             # Donation information
│   └── join/               # Membership details
├── themes/                  # Custom theme
│   └── lybdems-theme/      # Main theme files
│       ├── layouts/         # HTML templates
│       ├── assets/          # CSS, JS, and other assets
│       └── static/          # Static files (images, etc.)
├── hugo.toml               # Hugo configuration
└── README.md               # This file
```

## Customization

### Colors and Branding

The site uses Liberal Democrats brand colors defined in CSS variables:

```css
:root {
    --party-yellow: #FDBB30;
    --party-blue: #003DA5;
}
```

You can modify these in `themes/lybdems-theme/assets/css/main.css`.

### Content

#### Adding News Articles

1. Create a new `.md` file in `content/news/`
2. Use this front matter format:

```markdown
---
title: "Your Article Title"
date: 2025-02-09
tags: ["tag1", "tag2"]
summary: "Brief description of the article"
---

Your article content here...
```

#### Adding Councillors

1. Create a new `.md` file in `content/councils/`
2. Include councillor details, contact information, and achievements

#### Adding Campaigns

1. Create a new `.md` file in `content/campaigns/`
2. Describe the campaign goals, progress, and how to get involved

### Navigation

Edit the menu structure in `hugo.toml`:

```toml
[menu]
  [[menu.main]]
    identifier = "councils"
    name = "Councils"
    url = "/councils/"
    weight = 1
```

### Social Media Links

Update social media URLs in:
- `themes/lybdems-theme/layouts/index.html` (homepage)
- `themes/lybdems-theme/layouts/partials/footer.html` (footer)

### Contact Information

Update contact details throughout the site:
- Email addresses
- Phone numbers
- Office addresses
- Social media handles

## Deployment

### Building for Production

```bash
hugo --minify
```

This creates a `public/` directory with your static site.

### Hosting Options

- **Netlify**: Drag and drop the `public/` folder
- **Vercel**: Connect your Git repository
- **GitHub Pages**: Push to a `gh-pages` branch
- **Traditional hosting**: Upload the `public/` folder to your web server

### Environment Variables

For production, you may want to set:
- `HUGO_ENV=production`
- `HUGO_BASEURL` to your actual domain

## Content Management

### Regular Updates

- **News**: Add new articles regularly to keep content fresh
- **Campaigns**: Update progress and add new initiatives
- **Events**: Create event pages and update calendars
- **Photos**: Add images from local events and activities

### Content Guidelines

- Keep content local and relevant to your area
- Use clear, accessible language
- Include calls-to-action where appropriate
- Regular updates show an active local party

## Technical Details

### Theme Structure

- **Base Template**: `layouts/_default/baseof.html`
- **Homepage**: `layouts/index.html`
- **List Pages**: `layouts/_default/list.html`
- **Single Pages**: `layouts/_default/single.html`
- **Header**: `layouts/partials/header.html`
- **Footer**: `layouts/partials/footer.html`

### CSS Architecture

- Mobile-first responsive design
- CSS custom properties for consistent theming
- Flexbox and Grid for modern layouts
- Smooth transitions and hover effects

### JavaScript Features

- Mobile menu toggle with animation
- Smooth scrolling for anchor links
- Header scroll effects
- Button click animations

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- Optimized images and assets
- Minified CSS and JavaScript
- Fast loading with Hugo's static generation
- Responsive images and lazy loading ready

## Accessibility

- Semantic HTML structure
- ARIA labels where appropriate
- Keyboard navigation support
- High contrast color scheme
- Screen reader friendly

## SEO

- Proper meta tags and descriptions
- Structured data ready
- Clean URLs and navigation
- Fast loading times
- Mobile-friendly design

## Support and Maintenance

### Regular Tasks

- Update Hugo to latest version
- Review and update content
- Check for broken links
- Monitor performance
- Backup content regularly

### Troubleshooting

- **Build errors**: Check Hugo version and syntax
- **Styling issues**: Verify CSS file paths
- **Content not showing**: Check front matter and file structure
- **Performance issues**: Optimize images and check Hugo settings

## Contributing

1. Make changes in a feature branch
2. Test locally with `hugo server`
3. Commit with descriptive messages
4. Push and create a pull request

## License

This project is for Liberal Democrats local divisions. Please respect the party's branding guidelines and policies.

## Contact

For questions about this website template:
- Check the Hugo documentation
- Review the Liberal Democrats digital guidelines
- Contact your local party's web team

---

**Built with Hugo** | **Liberal Democrats Local Division**
