# Technical Specification

## Purpose

This document defines the technical stack and development standards for Litter Up Version 1.0.

All implementation must follow these specifications.

---

# Frontend

Framework

- Next.js (App Router)

Language

- TypeScript

Styling

- Tailwind CSS

UI Components

- shadcn/ui

Icons

- Lucide React

Animation

- Framer Motion

---

# Backend

Version 1.0 does not use a dedicated backend server.

Image processing should run locally within the Next.js application.

Future versions may introduce API Routes.

---

# Image Processing

Libraries

- sharp
- jimp
- colorjs.io

Algorithms

- Lab Color Space
- KMeans Clustering

Target

20 Color Quantization

100 × 100 Pixels

---

# File Upload

Supported Formats

- JPG
- JPEG
- PNG
- WEBP

Maximum File Size

20MB

---

# State Management

Use

React Context

Only introduce Zustand if the application becomes difficult to manage.

Redux should not be used.

---

# Folder Structure

app/

components/

features/

hooks/

lib/

types/

utils/

public/

docs/

---

# Code Style

Use TypeScript everywhere.

Avoid JavaScript.

Use functional components.

Avoid duplicated code.

Keep components small.

---

# Naming Rules

Components

PascalCase

Example

PhotoUploader.tsx

Functions

camelCase

Example

generatePalette()

Variables

camelCase

Constants

UPPER_SNAKE_CASE

---

# Styling Rules

Tailwind CSS only.

Do not write inline styles.

Keep spacing consistent.

Use reusable UI components.

---

# Performance Goals

First Load

Less than 3 seconds

Image Generation

Less than 10 seconds

Page Transition

Less than 300ms

---

# Browser Support

Latest

Chrome

Safari

Edge

Firefox

---

# Accessibility

Keyboard navigation required.

ARIA labels required.

Color alone must never communicate important information.

---

# Error Handling

Every error must include

- Cause
- Solution
- Retry Option

The application should never fail silently.

---

# Deployment

Hosting

Vercel

Repository

GitHub

Automatic Deployment

Enabled

---

# Package Manager

npm

---

# Quality Requirements

npm install

must complete successfully.

npm run lint

must pass.

npm run build

must pass.

No TypeScript errors.

No ESLint errors.

---

# Security

Never execute uploaded files.

Validate every uploaded image.

Limit upload size.

Prevent unsupported file types.

---

# Development Philosophy

Choose maintainability over complexity.

Choose readability over clever code.

Choose user experience over technical novelty.
