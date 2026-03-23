# Background Remover

Client-side background removal using ONNX Runtime and WebGPU. Everything runs in the browser — images never leave your machine.

Single HTML file. Open it, drag in images, get transparent PNGs.

## Models

Three quality tiers depending on how much VRAM you want to throw at it:
- Small (~10MB) — fast, good enough for thumbnails
- Medium (~40MB) — solid for most use cases
- Full (~176MB) — best quality, needs a decent GPU

Supports batch processing. Output as transparent PNG or compressed WebP.
