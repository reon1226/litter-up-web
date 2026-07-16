# MVP Specification

## Purpose

This document defines the Minimum Viable Product (MVP) for Litter Up.

The goal of Version 1.0 is to build a complete, polished photo mosaic generator focused on environmental art.

Only the features described in this document should be implemented.

Anything not listed here should be considered out of scope for Version 1.0.

---

# Product Goal

Allow users to transform a famous artwork into a collaborative photo mosaic using photographs of collected litter.

The entire process should be simple enough that anyone can complete it without reading instructions.

---

# User Flow

The application should guide users through the following steps:

1. Upload an artwork.
2. Generate pixel art.
3. Generate a numbered blueprint.
4. Review the color palette.
5. Upload photos for each color.
6. Generate the photo mosaic.
7. Download the completed artwork.

---

# MVP Features

## 1. Artwork Upload

The user can upload:

- JPG
- JPEG
- PNG
- WEBP

Features:

- Drag & Drop
- File Picker
- Preview Image

---

## 2. Pixel Art Generation

Automatically convert the uploaded artwork into:

- 100 × 100 pixels
- Exactly 20 colors
- Lab Color Space
- KMeans Color Quantization

The generated image should preserve the original appearance as much as possible.

---

## 3. Numbered Blueprint

Generate a blueprint where:

- Each color has a unique number (1–20).
- Every pixel displays its assigned number.
- Identical colors always use the same number.
- The blueprint can be downloaded as PNG.

---

## 4. Color Palette

Display all generated colors.

Each color should include:

- Color Number
- Color Preview
- RGB
- HEX
- Percentage of the image

---

## 5. Photo Upload

The user should NOT rename files manually.

Instead:

Each palette color should display an upload area.

Example:

Color 1

[ Upload Photos ]

Color 2

[ Upload Photos ]

...

Color 20

[ Upload Photos ]

The user can:

- Drag & Drop
- Select multiple photos
- Upload folders (if supported)

---

## 6. Photo Management

For each color:

Display:

- Uploaded photo count
- Thumbnail preview
- Delete button
- Replace button

The application should remember which photos belong to each color.

---

## 7. Mosaic Generation

Generate the final artwork.

Rules:

- Replace every numbered cell with a random photo from the corresponding color.
- Preserve the original artwork.
- Avoid repeating identical neighboring photos whenever possible.
- Fill every cell.

---

## 8. Download

Allow users to download:

- Final Mosaic (PNG)
- Numbered Blueprint
- Color Palette
- Original Pixel Art

---

# User Interface Requirements

The application should feel like a step-by-step wizard.

Each step should clearly indicate:

- Current step
- Completed steps
- Remaining steps

The user should never wonder what to do next.

---

# Performance

Target generation time:

Less than 10 seconds

Target image size:

100 × 100

20 Colors

---

# Out of Scope

Version 1.0 must NOT include:

- Login
- Accounts
- Database
- Cloud Storage
- AI Chat
- Payment
- Social Sharing
- Ranking
- Event Management
- Mobile App
- Admin Dashboard

---

# Success Criteria

Version 1.0 is considered complete when a first-time user can:

- Upload an artwork
- Generate a numbered blueprint
- Upload photos for every color
- Generate the final photo mosaic
- Download the finished artwork

without needing any external instructions.

---

# Development Rule

When making implementation decisions, always prioritize:

1. Simplicity
2. Stability
3. Speed
4. User Experience

Fancy features should never be added at the cost of usability.
