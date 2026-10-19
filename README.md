# MTG Print Template

A single-page web app that generates Magic: The Gathering style card templates designed for FDM 3D printing with a 0.4 mm nozzle.

Inspired by [mtg.design](https://mtg.design/create), rebuilt so every line, letter and image prints cleanly on a printer like the Ender 3 with manual filament swaps.

## Features

- Standard card size: 63 x 88 mm
- Selectable color layers (2 by default: white base plate + black ink, so only one filament swap)
- Uniform line widths of 0.4, 0.8 or 1.2 mm with rounded corners
- Text converted to outline shapes, with 10 fonts including rounder options
- Mana cost pips and a set symbol area
- Art upload with a threshold editor (brightness, contrast, smoothing, minimum feature size, invert), then drag and zoom in the preview
- Warnings when text strokes or details fall below 0.4 mm

## Exports

- **PNG** per layer: black on transparent, 20 px/mm (1260 x 1760)
- **SVG** per layer or combined: one solid shape per layer (white base plate, black for the rest), at exact 63 x 88 mm scale for slicer import

## Usage

Open `index.html` in any modern browser. No install or build step is needed. An internet connection is required on first load for the font rendering library (opentype.js from cdnjs).

To print, import the combined SVG into your slicer, assign a filament to each layer, and add a filament change between them.
