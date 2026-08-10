# Chapter 6 — Metadata Extraction

## What is metadata?
Hidden data embedded inside files (images, PDFs, DOCX, XLS, etc.) — includes camera info, GPS coordinates, author names, software versions, and more.

## How hackers use it
- 🗺️ **Trace location** — GPS EXIF data in photos
- 👤 **Identify target or creator** — author/username fields in documents
- 🏢 **Detect company structure / software used** — reveals internal usernames, domain names, software versions (which can map to known CVEs)

## Bonus tip
PDFs & DOCX files created in MS Office commonly contain:
- Author name
- Company name
- File creation/modification time
- Hidden revision history / tracked changes

## Tools

| Tool | Platform | Use |
|------|----------|-----|
| **exiftool** | Linux/macOS/Windows | CLI — extracts metadata from nearly any file type (`exiftool file.jpg`) |
| **FOCA** | Windows (GUI) | Drag-and-drop PDFs/DOCs/XLS → auto-extracts metadata, correlates usernames/software across many files, maps internal network structure |

> 🎯 "Use FOCA for this. Drag PDFs and boom — all metadata exposed!"

## Additional metadata tools
- **Metagoofil** — automates the FOCA-style workflow on Linux: searches a domain for public documents (pdf/doc/xls/ppt) and extracts metadata in one command.
- **ExifTool GUI variants** — e.g. **ExifCleaner**, **ExifPurge**, useful defensively to *strip* metadata before publishing files.
- **Jeffrey's Image Metadata Viewer** (exif.regex.info) — free web tool to inspect EXIF data from a photo URL, no install needed.
- **PDF metadata via `pdfinfo` / `pdftk`** — quick CLI alternatives to exiftool for PDFs specifically.
- **Google Reverse Image Search / Yandex Images / TinEye** — combine with metadata to find where else an image (and its original, unstripped version) has been posted.

## Defensive takeaway
Strip metadata from files before publishing publicly (most OSes and Office tools have a "remove personal info/properties" option) to avoid leaking usernames, internal software versions, or GPS coordinates.
