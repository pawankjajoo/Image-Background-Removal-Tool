# Background Remover

**100% client-side background removal** using modern AI models. Upload images, remove backgrounds, download transparent PNGs — all processed directly in your browser. Your images never leave your machine.

## Features

- **Client-Side Processing**: Everything runs in your browser using WebGPU/WebNN
- **No Server Upload**: Images never leave your machine — complete privacy
- **Multiple Quality Tiers**: Choose between speed and quality based on your GPU
- **Batch Processing**: Remove backgrounds from multiple images at once
- **Multiple Export Formats**:
  - Transparent PNG (standard)
  - Compressed WebP (smaller files)
- **Model Options**:
  - Small (~10MB) — fast, good for thumbnails
  - Medium (~40MB) — balanced, most use cases
  - Full (~176MB) — best quality, needs decent GPU
- **Progress Indication**: Real-time processing status
- **Drag & Drop Interface**: Simple, intuitive UX

## Tech Stack

- **Runtime**: ONNX Runtime Web with WebGPU acceleration
- **Models**: Pre-trained semantic segmentation models
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Processing**: Client-side canvas API
- **Export**: PNG/WebP encoding

## How It Works

1. **Upload Image**: Drag & drop or click to select from your device
2. **Choose Model**: Select quality tier based on your GPU capacity
3. **Process**: AI removes background in real-time
4. **Download**: Save as PNG or WebP

### Processing Pipeline

1. **Image Loading**: Detect format, load into canvas
2. **Preprocessing**: Resize/normalize for model input
3. **Model Inference**: Run semantic segmentation (Person/Object detection)
4. **Mask Generation**: Create binary mask from predictions
5. **Refinement**: Edge smoothing, feathering for clean results
6. **Alpha Channel**: Generate transparent output
7. **Export**: Encode as PNG or WebP

## Usage

### Web Interface

Simply open `index.html` in any modern web browser.

1. **Drag & Drop**: Drop images onto the upload area
2. **Or Click**: Click to open file picker
3. **Select Model**:
   - Small: Fastest, ~10MB download
   - Medium: Balanced (recommended)
   - Full: Best quality, ~176MB
4. **Wait**: Processing happens automatically
5. **Download**: Click download button for PNG or WebP

### Batch Processing

- Load multiple images
- Process sequentially with progress tracking
- Download all at once as ZIP file

## Model Details

### Small Model (~10MB)
- Resolution: 320x320
- Speed: <100ms per image
- Use Case: Thumbnails, web optimization
- GPU: Integrated graphics sufficient

### Medium Model (~40MB)
- Resolution: 512x512
- Speed: 200-500ms per image
- Use Case: General purpose, product photos
- GPU: 2GB VRAM typical
- **Recommended for most users**

### Full Model (~176MB)
- Resolution: 1024x1024
- Speed: 1-3s per image
- Use Case: Print quality, detailed backgrounds
- GPU: 4GB+ VRAM recommended

## Performance

- First run: Model download + initialization (~30s depending on model)
- Subsequent runs: Model cached in browser storage
- Processing: Parallelized across GPU cores
- Memory: Efficient model quantization reduces footprint

## Browser Requirements

### Minimum Requirements
- Chrome 113+ / Edge 113+ (WebGPU support)
- Firefox 123+ (experimental WebGPU)
- Safari 17.4+ (WebGPU beta)

### For Best Performance
- 4GB+ system RAM
- GPU with WebGPU support
- Modern OS (Windows 10+, macOS 10.15+, Linux)

## Supported Image Formats

**Input**: JPG, PNG, WebP, BMP, TIFF (up to 8MB)

**Output**:
- PNG (lossless, transparent background)
- WebP (smaller file size, transparent background)

## Privacy & Security

✅ **100% Private**: No image uploads to servers
✅ **No Tracking**: No analytics or telemetry
✅ **No Cookies**: Respects your privacy
✅ **Open Source Ready**: Transparent implementation
✅ **Offline Capable**: Works without internet (after model download)

## Use Cases

- **E-commerce**: Product photography background removal
- **Design**: Quick image editing for social media
- **Photography**: Batch background removal
- **Graphic Design**: Isolate subjects from backgrounds
- **Portrait Photography**: Professional background separation
- **Real Estate**: Property photo cleaning
- **Web Design**: Asset preparation

## Tips for Best Results

1. **Clear Subject**: Best results with well-defined subjects
2. **Good Lighting**: Adequate lighting improves accuracy
3. **Contrast**: Higher contrast with background works better
4. **Model Choice**: Use Full model for best quality on complex images
5. **Image Size**: Larger source images = better detail preservation

## Limitations

- Works best on photos with clear subject/background separation
- May struggle with:
  - Semi-transparent objects
  - Hair/fur with similar color to background
  - Complex patterns similar to subject
  - Very small subjects
- Not designed for medical/scientific image analysis

## File Structure

```
Image-Background-Removal-Tool/
├── index.html                    # Main application
└── README.md                     # This file
```

## Performance Metrics

- Typical background removal time: 100ms - 3s (depends on model)
- Model download: One-time, ~10-176MB depending on selection
- Browser storage: ~200-200MB total with all models

## FAQ

**Q: Where does my image go?**
A: Nowhere! Processing happens entirely in your browser. No servers involved.

**Q: Why is the first load slow?**
A: The AI model needs to be downloaded and initialized. Subsequent uses are instant (cached).

**Q: Which model should I use?**
A: Start with Medium. Use Small for speed, Full for quality.

**Q: Can I use this offline?**
A: After initial model download, yes! The model is cached.

**Q: What image sizes work best?**
A: 512x512 to 2048x2048 pixels works great. Larger = slower.

**Q: Can I batch process?**
A: Yes! Load multiple images and they'll queue automatically.

## Troubleshooting

- **WebGPU Not Available**: Update your browser to latest version
- **Out of Memory**: Use smaller model or process fewer images at once
- **Processing Slow**: Check GPU drivers are up to date
- **Unusual Results**: Try different model or check image quality

## Browser Compatibility

| Browser | Support | Notes |
|---------|---------|-------|
| Chrome 113+ | ✅ Full | Recommended |
| Edge 113+ | ✅ Full | Excellent |
| Firefox 123+ | ⚠️ Experimental | WebGPU flag may need enabling |
| Safari 17.4+ | ⚠️ Beta | Requires latest OS |
| Opera 99+ | ✅ Full | Based on Chromium |

## License

Created by Pawan K Jajoo

---

**Tags**: photoshop, tensorflow, photo-editing, website-editor, pytorch-implementation, remove-background
