# Responsive Image Carousel

A lightweight, customizable image carousel built with vanilla JavaScript. No dependencies required!


## Features

- **Fully Responsive** - Adapts to mobile, tablet, and desktop screens
- **Automatic Sliding** - Images advance automatically with configurable timing
- **Navigation Controls** - Intuitive previous/next buttons
- **Lightweight** - No dependencies, just HTML, CSS, and vanilla JavaScript
- **Customizable** - Easy to modify colors, sizes, and timing
- **Smooth Transitions** - Elegant sliding animations
- **Pause on Hover** - Automatic sliding pauses when users hover over the carousel
- **Accessibility** - ARIA attributes for better screen reader support
- **WordPress Compatible** - Works in WordPress HTML blocks without conflicts

## Installation

### Option 1: Direct HTML Include

Simply copy the entire code from the `carousel.html` file and paste it where you want the carousel to appear in your HTML.

### Option 2: WordPress Integration

1. In your WordPress editor, add a "Custom HTML" block
2. Copy the entire code from `carousel.html` and paste it into the HTML block
3. Update the page/post to see your carousel in action

## Customization

### Basic Configuration

The carousel has several easily customizable settings in the JavaScript section:

```javascript
// Configuration options
const autoplaySpeed = 4000; // Time between slides in milliseconds
const transitionSpeed = 500; // Slide transition speed in milliseconds
```

### Adding/Removing Images

To add or remove images, simply modify the card elements within the `.tc-track` container:

```html
<div class="tc-track">
  <!-- Example card -->
  <div class="tc-card">
    <img src="path/to/your/image.jpg" alt="Description of image" />
  </div>
  <!-- Add more cards as needed -->
</div>
```

### Styling

You can easily customize the appearance by modifying these CSS variables:

#### Card Appearance

```css
.tc-card {
  min-width: 250px; /* Card width */
  border-radius: 12px; /* Rounded corners */
  box-shadow: 0 4px 15px rgba(0,0,0,0.1); /* Card shadow */
}
```

#### Colors

```css
.tc-container {
  color: #333; /* Main text color */
}

.tc-description {
  color: #444; /* Description text color */
}

.tc-btn {
  color: #5C258D; /* Button icon color */
}
```

### Responsive Behavior

The carousel automatically shows 3 cards on desktop and 1 card on mobile. You can adjust this by modifying:

```javascript
const cardsToShow = window.innerWidth < 768 ? 1 : 3;
```

And for the CSS:

```css
@media (max-width: 768px) {
  .tc-gallery {
    max-width: 300px; /* Controls how many cards are visible on mobile */
  }
}
```

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)
- iOS Safari
- Android Chrome

## Performance Optimization

The carousel is designed to be lightweight and performant:

- Uses CSS transitions instead of JavaScript animations for smoother sliding
- Efficiently manages event listeners
- Uses requestAnimationFrame for smoother animations
- Minimizes DOM operations for better performance

## License

MIT License - Feel free to use, modify, and distribute this code for personal or commercial projects.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

If you encounter any issues or have questions, please open an issue on the GitHub repository.
