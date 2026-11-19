# Diagram Tool

A single-page, browser-only tool that turns a [Mermaid](https://mermaid.js.org/)-syntax text diagram into a clean SVG or PNG image. Rendering is done by [Pele](https://www.npmjs.com/package/pele) (loaded from jsDelivr). There is no build step and no server.

**Privacy:** the tool runs only in your browser. Your diagrams are never uploaded or stored anywhere else, and the tool collects no analytics.

## Usage

Open `index.html` in a browser, or serve the folder with any static server:

```bash
python3 -m http.server
```

1. Type or paste diagram source on the left. You can also drop a text file onto the editor or pick an example from **Load example…**
2. The preview updates as you type. Press <kbd>Ctrl</kbd>/<kbd>⌘</kbd> + <kbd>Enter</kbd> to render by hand.
3. Choose a theme and font. Open **Customise** to change any colour, chart series, corner radius or font weight.
4. Export with **Export SVG**, **Export PNG** (1×–4×) or **Copy SVG**. Tick **Include background** to export with a solid fill instead of a transparent one.

Supported diagrams include flowchart, sequence, state, Gantt, class, entity relationship, pie, XY chart and mindmap.

## Notes

- Exported SVGs have all CSS variables resolved to literal values, so they open correctly in Inkscape, Illustrator, Figma and other converters.
- Your source, theme and settings are saved in `localStorage` and restored the next time you open the page.
- You need an internet connection the first time to load Pele and the Google Fonts used by the page.
