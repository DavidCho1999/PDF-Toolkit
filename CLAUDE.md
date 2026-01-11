# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

PDF Toolkit is a client-side web application that provides 17 PDF manipulation tools. Everything runs in the browser with no server-side processing required.

## Architecture

**Single-file application**: All HTML, CSS, and JavaScript are contained in `index.html`.

**External Dependencies** (loaded via CDN):
- PDF.js (v3.11.174) - Mozilla's library for PDF rendering and text extraction
- pdf-lib (v1.17.1) - For PDF creation, editing, and manipulation

**Key Global Objects**:
- `pdfjsLib` - PDF.js library for reading/rendering PDFs
- `PDFDocument`, `rgb`, `degrees` - pdf-lib exports for creating/editing PDFs

## Code Structure

The JavaScript is organized into:
1. **Configuration** (`toolConfigs` object) - Defines each tool's icon, title, accepted file types, and action button text
2. **UI Management** - Modal handling, file drop zones, option buttons, sliders
3. **Tool Functions** - One async function per tool (e.g., `pdfToImages()`, `mergePdfs()`, `addWatermark()`)
4. **Utility Functions** - `downloadPdf()`, `downloadBlob()`, `formatFileSize()`, `showToast()`

## Available Tools

**Convert**: PDF to Images, Images to PDF, PDF to Text, PDF to Grayscale
**Edit**: Merge, Split, Rotate, Reorder, Add Pages, Remove Pages, Watermark
**Optimize**: Compress, Optimize for web
**Security**: Protect (add password), Unlock (remove password)
**Info**: View Metadata, Page Count

## Development

Open `index.html` directly in a browser. No build step required.

## Design System

- Color scheme: Ocean Blue (#3b82f6 primary, #06b6d4 secondary)
- Dark theme with glassmorphism effects
- Font: Inter (Google Fonts)
