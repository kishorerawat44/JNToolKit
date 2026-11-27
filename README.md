# JNToolkits

JNToolkits is a static collection of free, browser-based utility tools for everyday tasks. The site includes PDF tools, image tools, calculators, productivity tools, student tools, and developer utilities.

## Features

- **Browser-based tools** – most tools run locally in the browser.
- **No signup required** – open a tool and use it directly.
- **Simple static deployment** – no build step required.
- **Tool categories** – PDF, Image, Document, Calculators, Productivity, Student, and Tech tools.

## Project structure

```text
.
├── index.html                # Homepage / tool directory
├── assets/
│   ├── css/                  # Shared styles
│   ├── js/                   # Vendored third-party libraries
│   ├── calculators/          # Calculator tools
│   ├── document/             # Document tools
│   ├── image/                # Image tools
│   ├── pdf/                  # PDF tools
│   ├── productivity/         # Productivity tools
│   ├── student/              # Student/security tools
│   └── tech/                 # Developer utilities
```

## Run locally

Because this is a static site, you can serve it with any static file server.

### Option 1: Python

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

### Option 2: Node static server

```bash
npx serve .
```

## Included tools

- **PDF:** Merge, Split, Extract Pages, Compress, Rotate, Rearrange, JPG to PDF, Edit PDF, PDF to DOC.
- **Document:** Fill Scanned Form.
- **Image:** Image Splitter, Compress Image, Passport Photo Maker.
- **Calculators:** EMI, BMI, Age, Tip.
- **Productivity:** Word Counter, Unit Converter, Pomodoro Timer.
- **Student:** QR Code Generator, Password Generator.
- **Tech:** JSON/Base64/URL/Timestamp utilities.

## Privacy note

Most tools are designed to process data in the browser. However, the current UI loads Google Fonts from `fonts.googleapis.com` / `fonts.gstatic.com` via `assets/css/jntoolkits.css`, which creates external requests. Review and self-host fonts if you need a fully self-contained/offline deployment.

## Development notes

- The project currently has no automated test suite or CI configuration.
- Tool pages are mostly standalone HTML files with inline scripts and shared CSS.
- Vendored libraries live in `assets/js/`; review their licenses and update policy before redistribution or major changes.

## Contributing

1. Create a branch for your change.
2. Keep changes focused and test the affected tool pages manually in a browser.
3. For bug fixes, include a clear reproduction case in the pull request description.
4. For UI changes, verify desktop and mobile layouts.

## License

No license file is currently included in this repository. Add an appropriate `LICENSE` file before distributing or accepting external contributions.
