# Multi-Stage Image Search — live demo

Semantic search over 5,000 MS-COCO images, running entirely in your browser.

**Open it:** https://zsadigzade.github.io/image-search-demo/

This repository holds only the built static site. The source, tests and measurements
live in the course repository on GitLab (Charles University, NPRG045).

Text queries are encoded in the browser by CLIP ViT-B/32 (fp16 ONNX, downloaded once
from Hugging Face, ~127 MB) and ranked by exact cosine against 5,000 precomputed image
vectors. Its rankings were measured against the PyTorch model the published figures
come from: identical top result on 318/318 benchmark phrases.

Built from source commit 865c5d0.
