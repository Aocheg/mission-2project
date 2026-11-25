# The AI Timeline Pyramid: Tier 2, Pyramid architecture (built on the research table)

The design is the working page. Open `index.html` (double-click it, no server needed) and use the **Design view** bar at the top.

It is built on the 31 milestones in the research table (`Research.md`): every event, subfield and source link on the pyramid comes from that table.

## How the page answers the Tier 2 brief

| Brief item | Where to see it |
|---|---|
| **Layers** | Seven layers in the pyramid (plus an optional eighth for the future). The design plan at the bottom has a layer table built from `data.js`. |
| **Visual narrative** | Width = accumulated groundwork (100% down to 52%, 8 points per layer), tone = depth. Turn on **Connectors** to see events threaded in date order. |
| **Tooling, and why** | Design plan, section 3. Chosen: an interactive HTML page. |
| **Interactivity** | Click or tap a tile to open its card: four-part note plus a link to the source. Search, subfield pills, arrow keys and shareable links all work. |
| **Layout grid** | Turn on **Grid overlay** (12 columns on desktop, 4 on phones). Design plan, section 5. |
| **Wireframe/mockup showing layers, event placement and where details appear** | **Mockup** and **Wireframe** buttons. Turn on **Annotations**, then open an event to see the card labelled. |

## Layers and where each research milestone sits

| Layer | Name | Milestones (numbers follow the research table order) |
|---|---|---|
| 1 | Foundations | 1 McCulloch-Pitts, 2 Turing, 3 Dartmouth |
| 2 | Symbolic AI, expert systems and search | 5 LISP, 6 ELIZA, 8 PROLOG, 9 Lighthill, 10 XCON, 13 Deep Blue |
| 3 | Neural networks and early machine learning | 4 Perceptron, 7 Perceptrons book, 11 Backpropagation, 12 CNNs, 14 Deep belief nets |
| 4 | Deep learning at scale | 15 ImageNet, 16 AlexNet, 18 Seq2seq and attention, 19 AlphaGo |
| 5 | Transformers and large language models | 20 Transformer, 21 BERT, 22 GPT-3, 27 ChatGPT, 28 GPT-4, 29 Llama 2 |
| 6 | Generative image models | 17 GANs, 24 Diffusion, 25 DALL·E, 26 Stable Diffusion |
| 7 | AI for science and reasoning | 23 AlphaFold 2, 30 AlphaFold 3, 31 AlphaProof and AlphaGeometry 2 |
| 8 | The future (optional) | Appears when an event with `"layer": 8` is added |

Layers follow technique, not date, so they overlap in time (the perceptron is from 1957 but sits above LISP, from 1958). Layers with more tiles than fit one row wrap into balanced rows (3 + 3).

## Design view controls

- **Mockup / Wireframe:** the finished look, or a greyscale layout where each tile shows its milestone number.
- **Grid overlay**, **Annotations**, **Connectors:** as described above. Connectors follow the search filter.
- Shareable states: `index.html?view=wire&grid=1&ann=1&threads=1`. Add `#m20` to open an event too.

## Files (flat)

| File | Purpose |
|---|---|
| `index.html` | Page structure, design controls, detail card, design plan |
| `styles.css` | Design tokens, layers, tiles, themes, wireframe view, overlays, print |
| `app.js` | Rendering, search and filters, detail card, deep links, design tools |
| `data.js` | The 31 milestones, layers and subfield colours. The only file to edit to change content |

## Notes and gaps to agree with the research owner

- **No future row.** The research table ends at 2024 and has no AGI or open-questions entry, which the brief puts at the apex. Add one to `data.js` with `"layer": 8` and the apex layer appears automatically.
- **Card text.** "What happened", the subfield and the source link are the research table's own words. "Why it matters" and "Impact" are short drafts so the cards look complete; the Content Writers replace them in Tier 3. The card says so.
- **Date notes.** Where the table gives two dates (perceptron 1957/1958, attention 2014/2015, BERT 2018/2019, AlphaFold 2 2020/2021) the card shows a "Date note".
- Fonts: Cardo and Fira Sans are used if installed; otherwise the page falls back to Iowan Old Style or Georgia and the system sans.
- Publish for free: put the folder in a GitHub repository, then Settings, Pages, Deploy from a branch, `main`, `/ (root)`.

## Tested

Behaviour was tested with an automated script in a simulated browser (22 checks: rendering, layer counts, optional layer, source links, date notes, filters, connectors, views, deep links, bad data). Check the layout visually in a real browser on a laptop and a phone before submitting.
