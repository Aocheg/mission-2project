# The AI Timeline Pyramid: Tier 2, Pyramid architecture (working design)

The design is the working page. Open `index.html` (double-click it, no server needed) and use the **Design view** bar at the top.

## How the page answers the Tier 2 brief

| Brief item | Where to see it |
|---|---|
| **Layers** | The six layers in the pyramid. The design plan at the bottom has a layer table built from `data.js`. |
| **Visual narrative** | Width = accumulated groundwork (100% down to 40%), tone = depth. Turn on **Connectors** to see events threaded in date order. |
| **Tooling, and why** | Design plan, section 3. Chosen: an interactive HTML page. |
| **Interactivity** | Click or tap any tile to open its detail card. Search, subfield pills, arrow keys and shareable links all work. |
| **Layout grid** | Turn on **Grid overlay** (12 columns on desktop, 4 on phones). Design plan, section 5. |
| **Wireframe/mockup showing layers, event placement and where details appear** | **Mockup** and **Wireframe** buttons. Turn on **Annotations**, then open an event to see the detail card labelled. |

## Design view controls

- **Mockup / Wireframe:** the finished look, or a greyscale layout where each tile shows its milestone number from the brief.
- **Grid overlay:** shows the column grid over the page.
- **Annotations:** numbered callouts on the page and, once you open an event, on the detail card.
- **Connectors:** a dashed thread joins events in date order. It follows the search filter.
- Shareable states: `index.html?view=wire&grid=1&ann=1&threads=1` opens with those switched on. Add `#m16` to open an event too.

## Files (flat)

| File | Purpose |
|---|---|
| `index.html` | Page structure, design controls, detail card, design plan |
| `styles.css` | Design tokens, layers, tiles, themes, wireframe view, overlays, print |
| `app.js` | Rendering, search and filters, detail card, deep links, design tools |
| `data.js` | The 18 starter milestones, layers and subfield colours. The only file to edit to change content |

## Notes

- The pyramid uses the 18-event starter bank from the brief. To add events, add entries to `data.js` (each needs `id`, `year`, `sort`, `title`, `short`, `layer`, `field`, `subfield`, `sig`, `what`, `why`, `impact`). A full layer wraps to a second row; if an entry is incomplete the page skips it and shows a message.
- The notes are draft copy so the cards look real. The Content Writers can replace them in `data.js`.
- Fonts: Cardo and Fira Sans are used if installed; otherwise the page falls back to Iowan Old Style or Georgia and the system sans.
- Publish for free: put the folder in a GitHub repository, then Settings, Pages, Deploy from a branch, `main`, `/ (root)`.

## Tested

Behaviour was tested with an automated script in a simulated browser (23 checks: rendering, views, toggles, connectors, filters, query states, cards, deep links). Check the layout visually in a real browser on a laptop and a phone before submitting.
