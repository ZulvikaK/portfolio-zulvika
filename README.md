# Zulvika Kusumadevi - Portfolio Landing Page

A modern, responsive portfolio landing page built with Vue 3 and Tailwind CSS.

## Features

✨ **Modern Design**
- Clean, tech-forward aesthetic with teal/cyan gradient accents
- Fully responsive on all devices
- Dark mode toggle with localStorage persistence
- Smooth animations and transitions

🎯 **Key Sections**
- **Navbar**: Sticky navigation with mobile hamburger menu
- **Hero Section**: Eye-catching introduction with gradient effects
- **About & Tech Stack**: Skills showcase with interactive badges
- **Experience Timeline**: Visual timeline of professional journey
- **Expertise Areas**: Core competencies display
- **Contact/Footer**: Social links and contact information
- **Scroll to Top**: Floating button for easy navigation

🛠️ **Tech Stack**
- Vue 3 (Composition API)
- Tailwind CSS
- Vite
- Inter & Space Mono fonts

## Setup Instructions

### 1. Install Dependencies
```bash
npm install
```

### 2. Run Development Server
```bash
npm run dev
```

The app will open at `http://localhost:3000`

### 3. Build for Production
```bash
npm run build
```

### 4. Preview Production Build
```bash
npm run preview
```

## Customization Guide

### Update Personal Information

**Profile Data** - Edit in `App.vue`:
- Line 192-195: Update LinkedIn and email links
- Line 107-162: Modify skills array
- Line 164-217: Update experience timeline
- Line 219-235: Customize expertise areas

### Change Colors

**Primary Accent** - Find and replace in `App.vue`:
- `teal-500` → your color
- `cyan-500` → your color

**Background Colors**:
- Light mode: `slate-50`, `white`
- Dark mode: `slate-950`, `slate-900`

### Adjust Fonts

Edit `style.css`:
- Replace Google Fonts import URL
- Update `font-family` in Tailwind config

### Add Sections

Add new sections between existing ones in the template, following the same structure:
```vue
<section id="new-section" class="py-20 px-4 sm:px-6 lg:px-8">
  <div class="max-w-7xl mx-auto">
    <!-- Your content -->
  </div>
</section>
```

## Project Structure

```
.
├── index.html          # HTML entry point
├── main.js             # Vue app initialization
├── App.vue             # Main component (all sections)
├── style.css           # Tailwind directives & custom styles
├── package.json        # Dependencies
├── vite.config.js      # Vite configuration
├── tailwind.config.js  # Tailwind configuration
└── postcss.config.js   # PostCSS configuration
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License - Feel free to use this template for your own portfolio!

---

Built with ❤️ using Vue 3 & Tailwind CSS
