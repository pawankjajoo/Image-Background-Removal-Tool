# Image Background Remover

AI-powered background removal running entirely in the browser using ONNX neural networks. No server uploads required.

## Features

- Real-time background removal with multiple quality levels (Fast, Balanced, High Quality)
- Zero server cost - all processing happens on your device via WebGPU
- Edge refinement (feathering) slider for smooth transitions
- Batch processing support for multiple images
- Output format options (PNG with transparency or WebP)
- Configurable max resolution (1024px to 4096px or original)
- Live preview with background color swatches
- Processing stats (time, file sizes, dimensions)
- Download individual or batch results
- Drag and drop or click to upload support

## Tech Stack

- HTML5 / CSS3 / Vanilla JavaScript
- ONNX Runtime with WebGPU acceleration
- @imgly/background-removal library
- Canvas API for edge refinement
- LocalStorage for image caching

## License

MIT License

## Author

Pawan K Jajoo, Pushstart LLC
