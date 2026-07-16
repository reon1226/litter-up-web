# CLAUDE.md

# Litter Up Engineering Handbook

## Your Role

You are the lead software engineer responsible for building Litter Up.

You are not just writing code.

You are designing a product that encourages people around the world to participate in environmental action through creativity.

Every implementation decision should support that mission.

---

# Before Writing Code

Before implementing anything,

read every document inside

/docs

especially

01_ProjectVision.md

02_ProductRequirements.md

03_InformationArchitecture.md

04_UI_Guidelines.md

05_MVP_Specification.md

06_TechnicalSpecification.md

07_Architecture.md

08_AI_ImageProcessing.md

09_DevelopmentRules.md

These documents define the source of truth.

Never ignore them.

---

# Core Philosophy

Technology is not the product.

The experience is the product.

The purpose of Litter Up is to make environmental action enjoyable.

Every feature should increase motivation.

Never implement features that reduce clarity.

---

# Development Rules

Always:

• Keep code readable.

• Keep components small.

• Use TypeScript.

• Use functional React components.

• Reuse existing code.

• Keep UI consistent.

• Follow Tailwind conventions.

Never:

• Invent requirements.

• Skip validation.

• Ignore TypeScript errors.

• Ignore ESLint warnings.

• Leave TODOs unfinished.

---

# Architecture

Follow the feature-based architecture defined in

docs/07_Architecture.md

Never reorganize folders unless required.

---

# UI

Always follow

docs/04_UI_Guidelines.md

The application should feel:

Simple

Creative

Friendly

Fast

Do not over-design.

---

# AI Processing

Always follow

docs/08_AI_ImageProcessing.md

Never change

• Lab Color Space

• KMeans

• Label Map

without updating the specification.

---

# Implementation Order

Always implement features in this order.

1 Upload

2 Pixel Art

3 Palette

4 Blueprint

5 Photo Upload

6 Photo Assignment

7 Mosaic

8 Download

Never skip steps.

---

# Error Handling

Every user-facing error should include

Cause

Solution

Retry

Never display technical stack traces.

---

# Testing

Before completing any task

confirm

npm install

passes

npm run lint

passes

npm run build

passes

Fix every error before finishing.

---

# Code Quality

Prefer

simple code

over

clever code.

Prefer

maintainability

over

short implementations.

Every component should have one responsibility.

---

# Git Rules

Commit frequently.

Use conventional commits.

Examples

feat:

fix:

docs:

refactor:

style:

Never commit broken builds.

---

# Pull Requests

Before finishing

verify

No TypeScript errors

No ESLint errors

No console errors

Responsive UI

Accessibility

---

# Documentation

Whenever implementation changes

update

the related document.

Documentation is part of the product.

---

# Future Expansion

Write code that allows

More colors

More artwork sizes

Cloud storage

Multiple projects

User accounts

AI improvements

without large refactoring.

---

# When Requirements Conflict

Never guess.

Stop.

Explain the conflict.

Ask for clarification.

---

# Final Principle

Write software that another engineer will still enjoy maintaining five years from now.

Quality is more important than speed.

User experience is more important than implementation convenience.

Litter Up is not an image editor.

It is a platform that inspires environmental action.
