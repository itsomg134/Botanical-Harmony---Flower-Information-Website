#  Botanical Harmony - Flower Information Website

![Flower Website Preview](https://images.pexels.com/photos/736230/rose-flower-petal-beauty-736230.jpeg?auto=compress&cs=tinysrgb&w=1200&h=400&fit=crop)

A beautifully crafted, responsive flower encyclopedia website that showcases detailed information about various flowers including their scientific names, seasonal preferences, origins, and symbolic meanings. Built with pure HTML, CSS, and JavaScript.

##  Live Demo

[View Live Demo](#) *(Add your deployment link here - GitHub Pages, Netlify, Vercel, etc.)*

##  Table of Contents

- [Features](#-features)
- [Technologies Used](#-technologies-used)
- [Flower Database](#-flower-database)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Customization](#-customization)
- [Screenshots](#-screenshots)
- [Browser Support](#-browser-support)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

##  Features

- **Interactive Filtering System** - Filter flowers by season (Spring, Summer, Autumn) or special categories (Tropical, Romantic)
- **Rich Flower Database** - 12+ flowers with detailed information including:
  - Common and scientific names
  - Detailed descriptions
  - Seasonal preferences
  - Geographic origins
  - Symbolic meanings and cultural facts
- **Responsive Design** - Fully responsive grid layout that works beautifully on desktop, tablet, and mobile devices
- **Modern UI/UX** - Smooth hover animations, custom scrollbar, and elegant card-based design
- **Dynamic Content Rendering** - Pure JavaScript DOM manipulation without external frameworks
- **Image Fallback System** - Robust error handling for images
- **Accessibility Friendly** - Semantic HTML and proper contrast ratios

##  Technologies Used

- **HTML5** - Semantic markup structure
- **CSS3** - Modern styling with Flexbox and Grid, custom animations, gradients
- **JavaScript (ES6+)** - Dynamic content rendering, filtering logic, event handling
- **Google Fonts** - Inter and Playfair Display typography
- **Pexels API (Images)** - High-quality royalty-free flower photography

##  Flower Database

The website currently features 12 beautiful flowers:

| Flower | Scientific Name | Season | Origin | Symbolism |
|--------|----------------|--------|--------|------------|
| Rose | Rosa rubiginosa | Spring | Asia & Europe | Love & passion |
| Sunflower | Helianthus annuus | Summer | North America | Adoration & loyalty |
| Cherry Blossom | Prunus serrulata | Spring | Japan | Renewal & fleeting beauty |
| Lotus | Nelumbo nucifera | Summer | Asia & Australia | Spiritual awakening |
| Tulip | Tulipa gesneriana | Spring | Central Asia | Perfect love |
| Orchid | Orchidaceae family | Tropical | Worldwide tropics | Luxury & strength |
| Marigold | Tagetes erecta | Summer | Mexico | Festival & ritual |
| Peony | Paeonia lactiflora | Spring | China | Romance & prosperity |
| Chrysanthemum | Chrysanthemum morifolium | Autumn | East Asia | Joy & longevity |
| Dahlia | Dahlia pinnata | Autumn | Mexico | Elegance & dignity |
| Hibiscus | Hibiscus rosa-sinensis | Tropical | Pacific | Feminine energy |
| Lavender | Lavandula angustifolia | Summer | Mediterranean | Calmness & serenity |

##  Installation

### Option 1: Direct Download

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/botanical-harmony.git
   ```

2. **Navigate to the project directory**
   ```bash
   cd botanical-harmony
   ```

3. **Open the website**
   - Simply open `index.html` in your preferred web browser
   - Or use a local development server:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js (if you have live-server installed)
     npx live-server
     ```

### Option 2: One-click HTML File

The entire project is contained in a single HTML file. You can:
- Download the `index.html` file directly
- Copy the code into a new file named `index.html`
- Open it in any modern browser

##  Usage

### Filtering Flowers

Click on any filter button to sort flowers by category:
- ** All Flowers** - Display the complete collection
- ** Spring** - Show flowers that bloom in spring (Rose, Cherry Blossom, Tulip, Peony)
- ** Summer** - Summer blooming flowers (Sunflower, Marigold, Lavender, Lotus)
- ** Autumn** - Autumn flowers (Chrysanthemum, Dahlia)
- ** Tropical** - Tropical varieties (Orchid, Hibiscus, Lotus)
- ** Romantic** - Flowers associated with romance (Rose, Peony)

### Flower Cards

Each flower card displays:
- High-quality image of the flower
- Common name and scientific name
- Detailed description
- Season badge
- Origin information
- Fun symbolic fact

##  Project Structure

```
botanical-harmony/
│
├── index.html              # Main HTML file (contains all CSS, JS)
├── README.md               # Project documentation
└── assets/                 # (Optional) Additional assets folder
    └── images/             # Local images (if you prefer local storage)
```

*Note: The current version is self-contained in a single HTML file for easy deployment.*

##  Customization

### Adding New Flowers

To add more flowers to the database, locate the `flowersData` array in the JavaScript section and add a new object:

```javascript
{
  id: 13,
  name: "Your Flower Name",
  scientific: "Scientific name",
  description: "Detailed description of the flower...",
  season: "spring/summer/autumn/tropical",
  category: "spring/summer/autumn/tropical/romantic",
  origin: "Geographic origin",
  image: "URL to flower image"
}
```

### Modifying Colors

The color scheme can be customized by modifying the CSS variables in the `<style>` section:

```css
body {
  background: linear-gradient(145deg, #faf6f0 0%, #f0ebe2 100%);
}

.hero {
  background: linear-gradient(112deg, #2d4f3b 0%, #1e3a2f 100%);
}

.filter-btn.active {
  background: #8b5a2b;  /* Change active button color */
}
```

### Adding New Filter Categories

1. Add a new button in the filter bar HTML:
   ```html
   <button class="filter-btn" data-filter="newcategory"> New Category</button>
   ```

2. Update the filtering logic in the `filterFlowers()` function:
   ```javascript
   if (currentFilter === 'newcategory') return flower.category === 'newcategory';
   ```

##  Browser Support

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | 60+ |  Fully supported |
| Firefox | 60+ |  Fully supported |
| Safari | 12+ |  Fully supported |
| Edge | 79+ |  Fully supported |
| Opera | 50+ |  Fully supported |
| iOS Safari | 12+ |  Fully supported |
| Chrome (Android) | 60+ |  Fully supported |

##  Future Enhancements

- [ ] **Search Functionality** - Add search bar to find flowers by name
- [ ] **User Accounts** - Allow users to save favorite flowers
- [ ] **Care Guides** - Detailed growing and care instructions for each flower
- [ ] **Seasonal Calendar** - Visual calendar showing when flowers bloom
- [ ] **Language Support** - Multi-language translations (Spanish, French, Japanese)
- [ ] **Dark Mode** - Toggle between light and dark themes
- [ ] **Share Feature** - Share flower information on social media
- [ ] **Print Function** - Printable care cards for gardeners
- [ ] **Backend Integration** - Dynamic flower database with admin panel
- [ ] **User Ratings** - Allow users to rate and review flowers
- [ ] **Similar Flowers** - "You might also like" recommendations

##  Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

### Contribution Guidelines

- Follow existing code style and formatting
- Add comments for complex logic
- Test your changes across different browsers
- Update the README if adding new features
- Ensure responsive design remains intact

##  License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files...
```

## Acknowledgments

- **Images** - High-quality flower photographs from [Pexels](https://www.pexels.com)
- **Fonts** - [Google Fonts](https://fonts.google.com) for Inter and Playfair Display
- **Inspiration** - Nature and botanical gardens worldwide
- **Quote** - Lady Bird Johnson: "Where flowers bloom, so does hope."

##  Contact

documentation for your flower information website, including setup instructions, customization guides, and future enhancement ideas. You can customize the placeholder links, screenshots, and contact information as needed.
