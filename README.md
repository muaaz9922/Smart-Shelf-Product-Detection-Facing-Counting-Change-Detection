
### README.md

```markdown
# Smart Shelf: Product Detection, Facing Counting & Change Detection

A complete computer vision pipeline for intelligent retail shelf monitoring. Built on the challenging **SKU-110K** dataset, this project detects densely packed products, counts facings, analyzes shelf density, and detects changes between two shelf states.

---

## Project Overview

Modern retail is moving toward cashierless stores and automated inventory management. This project implements core computer vision capabilities required for a Smart Shelf system:

- Dense product detection on crowded shelves
- Accurate facing counting
- Product density heatmaps
- Change detection (products removed or added)
- Product cropping and embedding-based similarity
- Interactive Gradio deployment

---

## Key Features

- Fine-tuned YOLOv8 for dense product detection
- Facing counting and spatial analysis
- Vertical distribution analysis (top / middle / bottom shelf)
- Before-vs-After change detection using Hungarian matching
- Product crop extraction + ResNet embeddings
- Full shelf status report generation
- Gradio web application

---

## Dataset

**SKU-110K**

- 11,689 images of densely packed retail shelves
- Average of ~147 products per image
- Single class (`object`) – ideal for detection + counting
- Standard YOLO format annotations

---

## Pipeline Architecture

1. **Data Exploration**
2. **Product Detection** (YOLOv8 fine-tuning)
3. **Facing Counting + Density Heatmaps**
4. **Change Detection** (Before vs After)
5. **Full Smart Shelf Pipeline + Status Report**
6. **Evaluation & Improved Matching**
7. **Product Cropping + Embeddings**
8. **Gradio Deployment**

---

## Results Highlights

- Successfully detects and counts products in extremely dense scenes
- Generates clear before/after change visualizations
- Provides structured shelf status reports (Removed / Added / Net Change)
- Supports product-level similarity search using embeddings

---

## Installation

```bash
pip install ultralytics opencv-python matplotlib seaborn numpy pandas gradio scikit-learn torch torchvision tqdm
```

## How to Run
Download the SKU-110K dataset (YOLO format).

Run the project phase by phase (Phase 1 → Phase 8).

Launch the Gradio app for interactive shelf analysis.

## Technologies Used

Ultralytics YOLOv8

OpenCV
PyTorch + torchvision (ResNet embeddings)

Scikit-learn

Gradio

Matplotlib / Seaborn

## Future Improvements

Real temporal shelf sequences (instead of synthetic pairs)

Multi-class product recognition / SKU identification

Planogram compliance checking

Real-time video shelf monitoring

Multi-camera shelf tracking
