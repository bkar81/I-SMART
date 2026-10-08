# I-SMART — Image & Screenshot Markup, Annotation & Redaction Tool

**Open-source · Offline · Private**

**Version 1.0.0**

I-SMART is a standalone, mobile-first image annotation tool for opening or pasting an image, adding editable Layers, refining annotations and exporting the finished image. It is designed to run locally in the browser and can be hosted from a static site such as GitHub Pages.

## What I-SMART does

I-SMART lets you bring an image into the editor and annotate it without requiring an I-SMART server.

- Open an image from the device.
- Paste an image from the clipboard where the browser allows it.
- Use **Hand** to pan and zoom the image only.
- Use **Select** to select and refine existing Layers. Select never creates a new annotation.
- Draw with **Pen / Freehand**.
- Highlight with **Highlighter**.
- Add **Line** and **Arrow** annotations.
- Add **Rectangle / Box** and **Oval** shapes.
- Add formatted **Text**.
- Add numbered **Step** markers.
- Hide sensitive content with **Blur** or **Pixelate**.
- Reorder, duplicate, delete and refine Layers.
- Undo and redo changes.
- Export as PNG, JPEG or WebP.
- Share the resulting image using the device's sharing support where available.

## Select and Layers

Layers are editable objects rather than permanently painted pixels.

When an annotation is created, I-SMART remembers which tool created that Layer. After a normal annotation is completed, I-SMART returns to **Select** and selects the newly created Layer. Selecting a Layer exposes the properties belonging to the tool that created it, allowing that particular Layer to be refined without changing the main tool's settings.

For example, an Arrow created in red can later be selected and changed to yellow without changing the Arrow tool's current blue setting for the next Arrow you create.

## Pen / Freehand: Keep strokes together

The **Keep strokes together** option controls how your drawing is organized into Layers.

**Keep strokes together ON**

Your entire drawing stays together as one Layer, even when you lift your finger between strokes. This is useful when writing or drawing something that you want to move or edit as a single object.

**Keep strokes together OFF**

Every time you lift your finger, that stroke becomes its own Layer. This is useful when you want to move, resize, recolor, or delete individual strokes separately.

**Example:** If you write **“I am good”** with several strokes and Keep strokes together is ON, the whole writing can be moved together. If it is OFF, each stroke can be handled independently.

## Colors

I-SMART provides quick colors plus a custom color chooser with synchronized **HEX, RGB and HSL** values. The selected color is kept separate for each tool and each editable Layer. The screen eyedropper is used where the browser supports the EyeDropper API.

## Settings

Settings can be exported to and imported from JSON. The backup preserves the current settings for each tool, including dimensions, colors, opacity, styles, text formatting, freehand grouping and export preferences.

The **Tool Defaults** tab shows the factory defaults and provides a confirmation-protected reset of all tool settings. Resetting tool settings does not change existing Layers.

## Redaction

There is intentionally no separate REDACT tool. Use **Rectangle**, **Blur** or **Pixelate** when you need to hide or redact information.

## Privacy and offline behavior

I-SMART is local-first. Normal image annotation does not require an I-SMART application server. Your image and annotation work remain in the browser session unless you explicitly export, download or share the result.

The PWA service worker provides the application shell for offline use. Features that depend on browser capabilities, such as the system clipboard or EyeDropper API, depend on the browser and its permissions.

See the [Privacy Policy](./privacy.html) and [Terms of Service](./terms.html) for more information.

## Installing I-SMART

Open the hosted I-SMART address in a supported browser such as Chrome and choose **Install app** or **Add to Home screen** when offered.

## Files to host

Put these files together in the same folder on your static host:

- `index.html`
- `manifest.json`
- `service-worker.js`
- `pwa-192x192.png`
- `pwa-512x512.png`
- `pwa-maskable-512x512.png`
- `readme.html`
- `readme.md`
- `privacy.html`
- `terms.html`
- `LICENSE`

## What is intentionally not included

- Screenshot capture is not part of I-SMART. Images are brought in by opening or pasting them.
- OCR is intentionally excluded from the roadmap.

## Version

**I-SMART 1.0.0**

Image & Screenshot Markup, Annotation & Redaction Tool
