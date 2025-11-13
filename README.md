# Etch-a-Sketch

A browser-based drawing application inspired by the classic Etch-a-Sketch toy. This project allows users to create pixel art by hovering over or touching a grid of cells, with multiple color modes and customizable grid sizes.

## Features

### Drawing Modes
- **White Mode**: Draw with white color (default mode)
- **Black Mode**: Draw with black color for classic sketching
- **Colorful Mode**: Draw with random RGB colors for vibrant, rainbow-like effects
- **Custom Color Mode**: Define your own RGB color by specifying red, green, and blue values (0-255)

### Grid Customization
- **Dynamic Grid Size**: Change the grid dimensions by clicking the "Grid Length" button and entering your desired size
- **Default Grid**: Starts with a 16x16 grid (256 cells)
- **Responsive Design**: Grid scales automatically to fit the viewport using viewport-minimum units (vmin)

### User Controls
- **Clear Button**: Resets the grid while maintaining the current grid size
- **Interactive Drawing**: Works with both mouse hover (desktop) and touch events (mobile devices)

## Technologies Used

- **HTML5**: Structure and layout
- **CSS3**: Styling with Flexbox and CSS Grid
- **Vanilla JavaScript**: All interactivity and DOM manipulation
  - Event listeners for user interactions
  - Dynamic element creation
  - RGB color manipulation

## Project Structure

```
top-1.5.9-etch-a-sketch/
├── index.html          # Main HTML structure
├── scripts/
│   └── main.js        # JavaScript functionality
└── styles/
    └── style.css      # CSS styling
```

## How to Use

1. **Open the Application**: Open `index.html` in any modern web browser
2. **Start Drawing**: Hover your mouse (or touch on mobile) over the grid cells to draw
3. **Change Colors**:
   - Click "White" for white drawing
   - Click "Black" for black drawing
   - Click "Colorful" for random colors
   - Click "Custom Color" and enter RGB values (0-255) for each color channel
4. **Resize Grid**: Click "Grid Length" and enter a number for the new grid size
5. **Clear Canvas**: Click "Clear" to reset the drawing area

## Implementation Highlights

### Responsive Grid System
- Uses CSS Grid for the drawing canvas
- Dynamic grid template columns adjust based on user input
- Cell dimensions calculated using `calc(80vmin/gridNumber)` for consistent sizing

### Color Management
- RGB input validation ensures values stay within 0-255 range
- Custom color mode persists user's color choice until changed
- Random color generation for colorful mode using `Math.random()`

### Mobile Support
- Touch event listeners (`touchstart`) enable drawing on mobile devices
- Responsive sizing using viewport-relative units (vmin)
- Buttons scale appropriately for different screen sizes

### Input Validation
- Grid length input validates for numeric values only
- RGB color inputs loop until valid values (0-255) are provided
- Prevents empty or invalid grid sizes

## Project Origin

This project is part of The Odin Project curriculum (TOP 1.5.9), designed to practice DOM manipulation, event handling, and CSS Grid/Flexbox layout techniques.

## Recent Updates

- Fixed RGB input validation to properly constrain values to the 0-255 range
- Implemented custom color mode with user-defined RGB values
- Added mobile touch support for drawing functionality
