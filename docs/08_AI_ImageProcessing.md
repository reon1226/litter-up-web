# AI Image Processing Specification

## Purpose

This document defines the image processing pipeline used by Litter Up Version 1.0.

The objective is to convert an uploaded artwork into a collaborative photo mosaic while preserving the original appearance as accurately as possible.

Every implementation must follow this specification.

---

# Overall Pipeline

The image processing pipeline consists of the following stages:

1. Upload Artwork
2. Resize Image
3. Convert to Lab Color Space
4. Reduce to 20 Colors using K-Means
5. Generate Color Palette
6. Generate Label Map
7. Generate Numbered Blueprint
8. Upload Photos
9. Assign Photos to Color Groups
10. Generate Final Photo Mosaic
11. Export Results

---

# Stage 1 - Artwork Upload

Supported Formats

- JPG
- JPEG
- PNG
- WEBP

The uploaded image should remain unchanged until preprocessing begins.

---

# Stage 2 - Resize

Resize the artwork to:

100 × 100 pixels

This creates exactly

10,000 cells

Each pixel represents one tile in the final mosaic.

---

# Stage 3 - Color Space Conversion

Before color reduction,

convert the image from RGB to Lab Color Space.

Reason:

Lab color distance is closer to human color perception.

All color clustering must operate in Lab space.

---

# Stage 4 - Color Reduction

Algorithm

K-Means Clustering

Number of clusters

20

Output

Twenty representative colors.

Each pixel belongs to exactly one cluster.

---

# Stage 5 - Palette Generation

Generate a palette containing:

- Color ID
- RGB
- HEX
- Percentage
- Preview Color

The palette should be sorted by frequency.

The most common color becomes Color 1.

---

# Stage 6 - Label Map

Create a Label Map.

Each pixel stores

Color ID

Example

1 1 1 2 2

1 3 3 2 2

4 4 3 2 5

The Label Map is the master data for every later process.

---

# Stage 7 - Numbered Blueprint

Generate a printable blueprint.

Requirements

Every cell displays

Color Number

The background color remains visible.

Numbers remain readable.

Zooming should not reduce readability.

---

# Stage 8 - Photo Upload

For every Color ID,

users upload one or more photos.

Example

Color 1

10 Photos

Color 2

6 Photos

Color 3

15 Photos

The application stores them as independent photo groups.

---

# Stage 9 - Photo Assignment

Each Label Map cell uses

its Color ID

to select a photo.

Rules

Only photos belonging to the same Color ID may be used.

If multiple photos exist,

choose randomly.

The same photo should not appear repeatedly next to itself whenever possible.

---

# Stage 10 - Mosaic Generation

Replace every Label Map cell

with one uploaded photo.

Each photo is resized

to the tile size.

The final image should preserve

the overall appearance

of the original artwork.

---

# Random Placement Rules

The algorithm should:

Distribute photos evenly.

Avoid obvious repetition.

Preserve color balance.

Maximize visual variety.

---

# Missing Photos

If a Color ID has no uploaded photos,

display an error.

Do not generate the final mosaic.

The user must upload at least one photo for every Color ID.

---

# Export

Generate:

- Final Photo Mosaic
- Pixel Art
- Label Map
- Numbered Blueprint
- Color Palette

PNG format.

---

# Performance Target

100 × 100

20 Colors

Generation time

Less than

10 seconds.

---

# Future Improvements

Version 2 may introduce:

- AI photo quality enhancement
- Automatic color correction
- Brightness normalization
- Contrast normalization
- Smart photo selection
- Multi-color photo analysis
- Texture-aware placement

These are not part of Version 1.0.

---

# AI Processing Principles

Preserve the original artwork.

Maintain color consistency.

Keep every algorithm deterministic when required.

Prioritize visual quality over implementation simplicity.
