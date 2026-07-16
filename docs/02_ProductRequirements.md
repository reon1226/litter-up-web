# Product Requirements

## Overview

Litter Up is a web application that transforms photographs of collected litter into collaborative digital artwork.

The application should allow anyone to easily create artwork without requiring design or technical knowledge.

The entire experience should be completed in only a few simple steps.

---

# Target Users

## Primary Users

- Students
- Schools
- Local communities
- Environmental organizations
- Event organizers

## Secondary Users

- Companies (CSR activities)
- Municipalities
- NGOs
- Families
- Tourists

---

# User Journey

Every user should experience the following flow.

1. Upload a reference artwork.
2. Convert the artwork into pixel art.
3. Reduce the image to exactly 20 colors.
4. Generate a numbered blueprint.
5. Display the color palette.
6. Upload litter photographs.
7. Automatically classify each photograph into the nearest color group.
8. Generate the completed photo mosaic.
9. Download all generated files.

---

# Functional Requirements

## Artwork Upload

The user can upload:

- JPG
- JPEG
- PNG
- WEBP

Maximum size: 20MB

---

## Pixel Art Generation

The uploaded artwork should automatically become:

- 100 × 100 pixels
- 20 colors
- Lab Color Space
- KMeans Color Quantization

The original appearance should remain as recognizable as possible.

---

## Numbered Blueprint

Generate a blueprint where:

- Every color has a unique number.
- Every pixel displays its number.
- Identical colors always use the same number.
- The blueprint is easy to print.

---

## Color Palette

Display

- Number
- Color Preview
- RGB Value
- HEX Value
- Percentage of Image

for every color.

---

## Photograph Upload

Users should be able to upload:

- one photo
- multiple photos
- entire folders

using drag & drop.

---

## Automatic Classification

The application should:

- Analyze the representative color of every uploaded photo.
- Calculate the nearest palette color.
- Automatically assign the photo.
- Allow manual reassignment.

---

## Mosaic Generation

Replace every numbered cell using a random photograph from the corresponding color group.

Requirements:

- Random distribution
- Avoid repeated neighboring photos
- Preserve artwork appearance

---

## Export

Users can download:

- Completed Mosaic
- Numbered Blueprint
- Palette
- Classification List

---

# Non-Functional Requirements

The application should be

- Fast
- Responsive
- Easy to use
- Mobile friendly
- Accessible
- Stable

---

# Performance

Target generation time

100 × 100

20 colors

Less than 10 seconds

---

# Future Features

The current version should NOT include:

- Login
- Database
- User accounts
- Payment
- Ranking
- Social functions

These will be added in future versions.

The priority is creating the best possible mosaic generation experience.

---

# Development Principle

Whenever a new feature is proposed, ask:

Does this improve the experience of creating environmental art?

If not,

do not implement it.
