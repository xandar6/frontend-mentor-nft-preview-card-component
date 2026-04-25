# Frontend Challenge Starter

A lightweight vanilla HTML, CSS, and JavaScript starter for Frontend Mentor challenges and small practice websites.

The goal of this template is not to hide CSS behind a framework. It gives you a clean foundation so you can spend more time practicing layout, responsiveness, accessibility, and component styling.

## Table of Contents

- [Overview](#overview)
- [Folder Structure](#folder-structure)
- [How to Use](#how-to-use)
- [CSS Files](#css-files)
- [Starter Patterns](#starter-patterns)
- [Customization Checklist](#customization-checklist)
- [Author](#author)

## Overview

This starter includes:

- Modern CSS reset
- CSS custom properties for colors, fonts, spacing, sizing, radius, and shadows
- Base typography and element defaults
- A reusable container system
- A few small utility classes
- Accessible focus styles
- A tiny JavaScript entry file
- A README structure you can adapt for each challenge

## Folder Structure

```txt
frontend-challenge-starter/
  index.html
  README.md
  .gitignore
  css/
    reset.css
    variables.css
    base.css
    layout.css
    utilities.css
    style.css
  js/
    script.js
```

## How to Use

1. Copy this folder when starting a new challenge.
2. Rename the copied folder to match the project.
3. Replace the starter HTML in `index.html`.
4. Update the design tokens in `css/variables.css`.
5. Add challenge-specific styles in `css/style.css`.
6. Add JavaScript only when the challenge needs interactivity.

If you turn this into a GitHub template repository, you can start new projects from GitHub by clicking **Use this template**.

## CSS Files

### `reset.css`

Removes common browser defaults and makes sizing more predictable.

### `variables.css`

Stores design tokens such as colors, font families, spacing, container sizes, border radius, and shadows.

This is usually the first file to edit for each new challenge.

### `base.css`

Sets global page styles like body font, default link behavior, image behavior, buttons, and focus states.

### `layout.css`

Contains reusable layout patterns like `.container`, `.section`, and `.cluster`.

### `utilities.css`

Contains small single-purpose helper classes like `.sr-only`, `.flow`, and text alignment helpers.

### `style.css`

Imports the foundation files and gives you a place for project-specific CSS.

## Starter Patterns

### Container

```css
.container {
  width: min(100% - (var(--container-padding) * 2), var(--container-max));
  margin-inline: auto;
}
```

This keeps content centered, gives small screens side breathing room, and stops the layout from becoming too wide on large screens.

### Responsive Section Spacing

```css
.section {
  padding-block: var(--section-padding);
}
```

The value comes from `variables.css`:

```css
--section-padding: clamp(2rem, 6vw, 5rem);
```

This lets vertical spacing grow smoothly between mobile and desktop.

### Flow Utility

```css
.flow > * + * {
  margin-block-start: var(--flow-space, 1rem);
}
```

This adds consistent vertical spacing between direct children. You can customize it per component:

```css
.card {
  --flow-space: 1.5rem;
}
```

## Customization Checklist

Before building a new challenge, update:

- Page title in `index.html`
- Colors in `css/variables.css`
- Font family and font weights
- Container max width
- Main spacing scale if the design uses different spacing
- README project name and links

## Author

- Frontend Mentor - Add your profile URL here
