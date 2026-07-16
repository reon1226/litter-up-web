# System Architecture

## Purpose

This document defines the overall architecture of Litter Up Version 1.0.

The goal is to build a modular, maintainable, and scalable application.

Every feature should have a clear responsibility.

---

# Architecture Overview

Litter Up follows a feature-based architecture.

The application is divided into independent modules.

Each module should have a single responsibility.

```
User

↓

Upload Artwork

↓

Image Processing

↓

Color Palette Generation

↓

Blueprint Generation

↓

Photo Assignment

↓

Photo Mosaic Generation

↓

Download
```

---

# Folder Structure

```
app/
│
├── page.tsx
├── layout.tsx
│
├── upload/
├── editor/
├── preview/
├── download/
│
components/
│
├── common/
├── layout/
├── ui/
│
features/
│
├── artwork/
├── palette/
├── blueprint/
├── photo-upload/
├── mosaic/
│
hooks/
│
lib/
│
utils/
│
types/
│
public/
│
docs/
```

---

# Feature Responsibilities

## Artwork

Responsible for:

- Upload artwork
- Validate image
- Resize image

---

## Palette

Responsible for:

- Generate 20 colors
- Calculate RGB
- Calculate HEX
- Calculate percentages

---

## Blueprint

Responsible for:

- Number assignment
- Number rendering
- Export blueprint

---

## Photo Upload

Responsible for:

- Upload photos
- Folder upload
- Preview
- Delete
- Replace

---

## Mosaic

Responsible for:

- Match photos
- Random placement
- Generate final artwork

---

# Data Flow

```
Artwork

↓

Resize

↓

100×100

↓

20 Colors

↓

Label Map

↓

Palette

↓

Blueprint

↓

Photo Assignment

↓

Mosaic

↓

Download
```

---

# Component Rules

Components should:

- Do one thing
- Be reusable
- Be independent

Avoid large components.

---

# State Flow

Global State

- Uploaded artwork
- Palette
- Label Map
- Uploaded Photos
- Final Mosaic

Local State

- Dialog
- Hover
- Loading

---

# File Management

Temporary files remain in memory.

No files are stored permanently.

Users control all downloads.

---

# Error Flow

Every processing step should return:

Success

or

Error

Every error must include:

- Message
- Cause
- Suggested solution

---

# Performance Strategy

Heavy processing should happen asynchronously.

The UI should never freeze.

Loading indicators should appear during long operations.

---

# Future Expansion

The architecture should support:

- Multiple artworks
- Additional color counts
- AI color correction
- Cloud storage
- User accounts
- Team collaboration

without major refactoring.

---

# Architecture Principles

Every module should be:

- Independent
- Reusable
- Testable
- Replaceable

The system should remain easy to understand even as new features are added.
