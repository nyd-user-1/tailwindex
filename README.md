# tailwindex

The fastest way to learn and apply Tailwind CSS classes: click an element in a live preview, search a complete utility index, try a class by hovering it, apply it with a click or Enter.

- **Select:** click an element in the preview. Arrow keys walk the element tree, and the breadcrumb selects ancestors.
- **Search:** press `/`, then type a utility (`p-6`), a property (`justify`) or a full class (`md:hover:bg-sky-500`). Variants typed in front of a class are applied with it.
- **Try:** hover a row, or arrow to it, and the selected element shows the class immediately. Moving off reverts it.
- **Apply:** click, or press Enter. A class that sets the same thing under the same variants is swapped, not stacked (`p-4` → `p-6`, `bg-white` → `bg-sky-500`, `md:p-8` → `md:p-4`).
- **Undo:** `⌘Z` / `⇧⌘Z` (Ctrl on other systems).
- **Changes:** the Changes tab lists every touched element, original beside current, with revert per element and copy all.
- **Export:** HTML, JSX (`className`, camelCased attributes, style objects, self-closing tags), Vue, and a permalink carrying the whole document.

Open `index.html` in a browser. Work is saved in the browser's local storage.

## Offline

`vendor/tailwindcss-browser-4.1.11.js` is the MIT-licensed Tailwind browser engine (260 kB, unmodified, wrapped in one function). Kept beside `index.html`, the preview works with no connection, including from `file://`. Without it, the engine loads from the jsDelivr CDN, and the preview says so when it cannot.
