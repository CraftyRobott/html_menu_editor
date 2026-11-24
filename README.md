# HTML Menu Editor

A standalone browser-based editor for importing and modifying an existing HTML/CSS/JavaScript menu system.

## Run it

Open [index.html](index.html) in a modern browser, or serve the repository locally:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Workflow

1. Choose **Import files** and select the menu's HTML, CSS and JavaScript files.
2. Select the HTML file in the project list to load its menu structure and preview.
3. Select elements in the structure tree to edit their text, class, ID, link destination and common inline styles.
4. Reorder elements with drag and drop or the Move up / Move down / Indent / Outdent controls.
5. Use the HTML, CSS and JavaScript source tabs for full-file changes.
6. Export the edited project as a ZIP, or explicitly push the files to GitHub.

## GitHub publishing

The Push to GitHub dialog targets `CraftyRobott/html_menu_editor` by default. Supply a GitHub personal access token with repository Contents read/write permission. The token is held only in the page's memory and sent directly to GitHub's API; it is not stored by this app. Confirm the upload before publishing.

## Preview safety

Imported JavaScript is disabled in the preview by default. Enable **Run imported JS** only when you trust the source. The preview runs in a sandboxed iframe without same-origin access to the editor.

## Notes and limitations

- This is a lightweight structural editor, not a full visual page builder.
- The menu tree focuses on navigation/menu-related elements such as `nav`, links, buttons, menu items, list items, and elements with menu/nav names in their class or ID.
- Complex layout changes are best made in the source editor.
- The editor preserves imported files and exports them together in a ZIP. The browser preview inlines imported CSS and JavaScript so it can render without a local development server.
