# IMIC Dataset

This dataset contains paired white-light and fluorescence images for porcine fluorescence endoscopy image fusion research. It supports the study of anatomical detail preservation and fluorescence visualization, including pseudocolor fusion.

## Directory Structure

```text
.
├── README.md
├── ir/       # Fluorescence images stored in RGB format
├── vi/       # White-light images (WLI)
└── ir_gray/  # Grayscale fluorescence images
```

The folder name `ir` refers to fluorescence images in this dataset; it does not denote thermal infrared images.

## Image Summary

| Folder | Content | Number of Images | Image Mode |
| --- | --- | ---: | --- |
| `ir` | RGB-stored fluorescence images | 201 | RGB |
| `vi` | White-light images | 201 | RGB |
| `ir_gray` | Grayscale fluorescence images | 201 | Grayscale |

All images are JPEG files with a resolution of **1440 × 1080 pixels** (width × height). The dataset contains **201 matched WLI–grayscale fluorescence pairs** and **200 sample IDs represented in all three folders**. The RGB and grayscale fluorescence files are representations of the same modality, not additional independent samples.

## Image Pairing

Match images by their numeric sample ID, rather than by the complete filename. For example, sample `001` consists of:

```text
vi/image_001_color.jpg
ir/image_001_fluorescence.jpg
ir_gray/image_001_fluorescence.jpg
```

Use `vi` with `ir_gray` for experiments requiring grayscale fluorescence input. Use `ir` when the RGB-stored fluorescence representation is needed.
