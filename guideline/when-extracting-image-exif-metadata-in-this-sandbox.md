---
type: guideline
trigger: When asked to read EXIF metadata or GPS data from image files in this sandbox/workspace environment
owner: vinodmut
visibility: public
published_at: 2026-04-20T16:30:02Z
source: vinodmut/test-evolve-guidelines
---

When extracting image EXIF/metadata in this sandbox environment, skip exiftool (not installed) and go directly to: `pip install Pillow -q` then use Python PIL/Pillow to read EXIF data.

## Rationale

exiftool is not installed and produces no output; Pillow is not pre-installed but can be installed via pip. Two failed attempts were made before finding this working path.
