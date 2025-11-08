# WLED Pixel Editor

A web-based pixel art editor for WLED LED matrices, created for my kids to easily create and manage pixel art on our LED displays.

## Features

- Draw pixel art with paint, fill, and color picker tools
- Auto-discover WLED devices on your network
- Save presets directly to WLED
- Works on desktop and mobile
- GIF Player integration
- Real-time LED updates
- Supports any matrix size (auto-detected from WLED device)
- Dynamic grid layout (max 32 pixels wide, wraps to multiple rows)

## Requirements

This app was designed using the latest [WLED Nightly build](https://github.com/wled/WLED/releases).

For GIF playback functionality, you'll need to install the [WLED GifPlayer UI](https://github.com/Manut38/WLED-GifPlayer-UI/tree/main) on your WLED device.

## How to Use

### Option 1: Use from Computer
1. Download `pixel-editor.html`
2. Open the file in any modern web browser
3. Click "Scan for WLED Devices" or enter your WLED IP manually
4. Start creating pixel art

### Option 2: Upload to ESP32
1. Go to your WLED device at `http://[your-ip]/edit`
2. Upload `pixel-editor.html`
3. Access at `http://[your-ip]/pixel-editor.html`

## Device Discovery

The app can automatically scan your network for WLED devices:
- Scans common IP ranges (192.168.1.x, 192.168.0.x, 10.0.0.x)
- Auto-detects matrix dimensions
- Configures grid layout automatically

## Grid Layout

- Was designed for 16x16 grids, but has been adapted for different sizes
- Displays exact number of LEDs in your string
- Maximum 32 pixels wide
- Automatically wraps to multiple rows for longer strips

## Browser Compatibility

Tested on Brave browser. Should work on other modern browsers with Fetch API support (Chrome, Firefox, Edge, Safari).

## Technical Details

- No server required - runs entirely client-side
- All presets stored directly on WLED device
- Settings saved in browser localStorage
- No personal data included in the HTML file

## Credits

Created for family use. Uses the WLED API for all device communication.

## License

MIT License
