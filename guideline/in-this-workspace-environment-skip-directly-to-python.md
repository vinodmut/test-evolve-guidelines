---
type: guideline
trigger: When extracting EXIF or GPS metadata from images in this workspace
owner: vinodmut
visibility: public
published_at: 2026-04-20T21:42:25Z
source: vinodmut/test-evolve-guidelines
---

In this workspace environment, skip directly to Python struct-based manual EXIF parsing. Neither exiftool nor PIL/Pillow are installed.

## Rationale

Both exiftool and PIL failed in this session before struct succeeded. Encoding the environment state avoids 2 wasted attempts on every future EXIF task.
