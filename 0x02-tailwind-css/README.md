# 0x02 Tailwind CSS Project

A comprehensive project demonstrating Tailwind CSS setup, configuration, and various layout techniques including CSS Grid, Flexbox, responsive design, and component creation.

## 🎯 Project Overview

This project is part of the ALX Intermediate Frontend Development curriculum, focusing on mastering Tailwind CSS utility-first framework. It showcases different layout methodologies and responsive design patterns using Tailwind CSS classes.

## 📚 Learning Objectives

By the end of this project, you will be able to:

- Set up and configure Tailwind CSS in a project
- Understand and apply utility-first CSS methodology
- Create responsive layouts using CSS Grid and Flexbox
- Build navigation components with hover effects
- Implement responsive image galleries
- Optimize CSS output for production
- Apply responsive design principles with Tailwind's breakpoint system

## 🛠️ Technologies Used

- **Tailwind CSS v4.1.11** - Utility-first CSS framework
- **HTML5** - Semantic markup
- **CSS3** - Custom media queries and styles
- **Node.js** - Package management
- **PostCSS** - CSS processing

## 📁 Project Structure

```
0x02-tailwind-css/
│
├── src/                                     # Source files
│   ├── 1-index.html                 # Basic CSS Grid Layout
│   ├── 2-index.html                 # Enhanced Grid Layout
│   ├── 3-nav_index.html          # Flexbox Navigation Bar
│   ├── 4-flexbox_index.html    # Responsive Flexbox Layout
│   ├── 5-gridflex_index.html    # Combined Grid and Flexbox
│   ├── 6-imageGallery.html     # Image Gallery with Grid/Flexbox
│   ├── input.css                        # Tailwind CSS input file
│   └── output.css                      # Compiled CSS output
│
├── 1-index.html                       # Production copies
├── 2-index.html
├── 3-nav_index.html
├── 4-flexbox_index.html
├── 5-gridflex_index.html
├── 6-imageGallery.html
├── package.json                       # Project dependencies
├── tailwind.config.js                 #  Tailwind configuration
└── README.md                       # This file
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/kimoban/0x02-tailwind-css.git
   cd 0x02-tailwind-css
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Build CSS (if needed):**

   ```bash
   npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
   ```

4. **Open any HTML file in your browser** to view the demonstrations.

## 📖 File Descriptions

### 1. Basic CSS Grid Layout (`1-index.html`)

- Demonstrates fundamental CSS Grid implementation
- Uses `grid-cols-3` for three-column layout
- Features color-coded grid items with padding

### 2. Enhanced Grid Layout (`2-index.html`)

- Advanced grid layout with more complex structure
- Responsive design considerations

### 3. Flexbox Navigation Bar (`3-nav_index.html`)

- Responsive navigation bar using Flexbox
- Hover effects on navigation links
- Mobile-responsive with custom media queries
- Center-aligned navigation with spacing utilities

### 4. Responsive Flexbox Layout (`4-flexbox_index.html`)

- Two-column sidebar layout using Flexbox
- Responsive design that stacks on mobile
- Demonstrates `w-1/3` and `w-2/3` width utilities

### 5. Combined Grid and Flexbox (`5-gridflex_index.html`)

- Hybrid approach using both Grid and Flexbox
- Complex layout composition

### 6. Image Gallery (`6-imageGallery.html`)

- Responsive image gallery using CSS Grid
- Three-column gallery that becomes single column on mobile
- Placeholder images with aspect-ratio maintenance
- Combines main layout with gallery section

## 🎨 Key Tailwind CSS Features Demonstrated

### Layout Systems

- **CSS Grid**: `grid`, `grid-cols-3`, `grid-cols-1`, `lg:grid-cols-3`
- **Flexbox**: `flex`, `flex-direction-column`, `justify-center`
- **Responsive Design**: `lg:`, `md:`, mobile-first approach

### Spacing & Sizing

- **Padding**: `p-4`, `px-2`
- **Margins**: `mb-4`, `mt-4`, `mt-8`
- **Gaps**: `gap-4`
- **Width**: `w-1/2`, `w-1/3`, `w-2/3`

### Colors & Styling

- **Background Colors**: `bg-blue-200`, `bg-gray-300`, `bg-red-400`
- **Text Colors**: `text-white`, `text-red-700`
- **Hover Effects**: `hover:bg-gray-500`

### Typography

- **Font Sizes**: `text-xl`, `text-2xl`, `text-3xl`
- **Font Weight**: `font-bold`

### Visual Effects

- **Rounded Corners**: `rounded-lg`
- **Aspect Ratio**: `aspect-square`
- **Object Fit**: `object-cover`
- **Overflow**: `overflow-hidden`

## 📱 Responsive Design Features

The project implements mobile-first responsive design:

- **Desktop**: Multi-column layouts, horizontal navigation
- **Tablet**: Adjusted column counts, optimized spacing
- **Mobile**: Single-column layouts, stacked navigation

### Breakpoints Used

- **Default**: Mobile styles (0px and up)
- **lg**: Large screens (1024px and up)
- **Custom**: 768px breakpoint via CSS media queries

## 🔧 Configuration

### Tailwind Configuration (`tailwind.config.js`)

```javascript
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### Input CSS (`src/input.css`)

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@media (max-width: 768px) { 
  main { grid-template-columns: 1fr; } 
}
```

## 🎯 Best Practices Demonstrated

1. **Utility-First Approach**: Using Tailwind's utility classes instead of custom CSS
2. **Responsive Design**: Mobile-first methodology with progressive enhancement
3. **Semantic HTML**: Proper use of HTML5 semantic elements
4. **Component Organization**: Logical separation of layout concerns
5. **Performance**: Optimized CSS output through Tailwind's purge functionality

## 🚀 Usage Examples

### Creating a Grid Layout

```html
<main class="grid grid-cols-3 gap-4">
  <div class="bg-blue-200 p-4">Item 1</div>
  <div class="bg-blue-300 p-4">Item 2</div>
  <div class="bg-blue-400 p-4">Item 3</div>
</main>
```

### Responsive Flexbox Navigation

```html
<nav class="flex space-x-5 justify-center bg-gray-300 text-white p-4">
  <a href="#" class="px-2 text-xl hover:bg-gray-500 p-2 rounded-lg">Home</a>
  <a href="#" class="px-2 text-xl hover:bg-gray-500 p-2 rounded-lg">About</a>
</nav>
```

## 🔍 Browser Support

This project supports all modern browsers:

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📈 Performance Considerations

- **CSS Purging**: Tailwind removes unused styles in production
- **Minimal Custom CSS**: Leverages utility classes for smaller file sizes
- **Optimized Images**: Uses placeholder images with proper aspect ratios
- **Efficient Layout**: CSS Grid and Flexbox for performant rendering

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-layout`)
3. Commit your changes (`git commit -am 'Add new layout example'`)
4. Push to the branch (`git push origin feature/new-layout`)
5. Create a Pull Request

## 📝 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

### Isaiah Kimoban

- GitHub: [@kimoban](https://github.com/kimoban)
- Project: [0x02-tailwind-css](https://github.com/kimoban/0x02-tailwind-css)

## 🙏 Acknowledgments

- [ALX Software Engineering Program](https://www.alxafrica.com/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## 📚 Additional Resources

- [Tailwind CSS Official Documentation](https://tailwindcss.com/)
- [CSS Grid vs Flexbox](https://css-tricks.com/css-grid-replace-flexbox/)
- [Responsive Web Design Fundamentals](https://web.dev/responsive-web-design-basics/)
- [Modern CSS Layout Techniques](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout)

## Happy Coding! 🚀
