# Calendar Wheel UI

An interactive, mobile-friendly calendar interface featuring a slot machine-style date selection system with six synchronized wheels.

## Features

- Six interactive rotatable wheels for date selection
- Smooth scrolling with momentum and touch support
- Day of week labels (SUN-SAT) with corresponding dates
- Responsive design for mobile and desktop
- Visual feedback with alternating row colors
- Center marker for precise selection
- Mobile-optimized with touch event handling

## Setup

1. Include required CDN:
```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css" rel="stylesheet">
```

2. Add the HTML structure:
```html
<div class="slot-machine">
    <div class="slot" data-slot="1">
        <div class="slot-content"></div>
        <div class="center-marker"></div>
    </div>
    <!-- Repeat for slots 2-6 -->
</div>
```

## Wheel Configuration

The interface consists of 6 wheels with different data ranges:
- Wheel 1: 1-365 + 55 zeros
- Wheel 2: 1-366 + 54 zeros
- Wheel 3: Complex date format with day labels
- Wheel 4: 1-354 + 66 zeros
- Wheel 5: 1-355 + 65 zeros
- Wheel 6: 1-384 + 36 zeros

## Mobile Optimization

- Prevents default scroll behavior
- Supports touch events
- Responsive font sizing
- Hardware-accelerated animations
- Smooth momentum scrolling

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers with touch support
- iOS Safari with momentum scrolling

## Usage

Initialize the calendar wheel:

```javascript
document.addEventListener('DOMContentLoaded', () => {
    const slotMachine = new SlotMachine();
});
```

## Custom Styling

The interface uses CSS variables for easy customization:

```css
:root {
    --slot-width: min(15vw, 180px);
    --slot-height: 80vh;
    --slot-background: #f0f0f0;
    --slot-border: #ccc;
    --text-color: #333;
    --selected-color: #007bff;
}
```

## Performance

- Uses requestAnimationFrame for smooth animations
- Hardware-accelerated transforms
- Efficient DOM updates
- Optimized touch event handling

## License

MIT License