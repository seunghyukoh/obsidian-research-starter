# Reading workflow

## 1. Add a paper

Save the PDF under `papers/` with a descriptive, stable name, for example
`2026-10 -- Paper title.pdf`. The plugin writes its proxy Markdown note next
to the PDF on your first highlight. A browser download is sufficient.

## 2. Highlight by meaning

Select text in Obsidian's PDF viewer and click a color in the floating palette.

| Visible color | Hex | Section label | Meaning | Stored type |
| --- | --- | --- | --- | --- |
| Yellow | `#fffe01` | 핵심 주장/기여 | Main claim or contribution | `yellow` |
| Mint | `#8affd7` | 방법/설정 | Method or experimental setup | `green` |
| Peach | `#ffbbab` | 결과/근거 | Result or supporting evidence | `blue` |
| Lavender | `#d6b7fe` | 가정/한계/의문 | Assumption, limitation, or question | `red` |
| Sky blue | `#98e6ff` | 내 연구와 연결 | Connection to your research | `purple` |

Stored type IDs are stable identifiers, not the current visual colors.
The palette intentionally preserves that distinction from the original setup.
Section order follows palette order; empty sections appear once used.
You can change labels and colors in the plugin settings without changing IDs.

## 3. Search what you read

Focus a note, press **Cmd/Ctrl+Shift+F**, and try these Obsidian searches:

```text
path:papers file:_highlights "searchable"
path:papers file:_highlights line:("(type:: red)")
path:papers file:_highlights line:("(type:: blue)" "accuracy")
```

The last two searches find limitation entries and result entries mentioning
accuracy. Replace the words with your own topic. No Dataview plugin is required.
Search indexes the proxy note, which is why selected PDF passages become easy
to rediscover.

## 4. Link evidence to your thinking

A generated item contains the quote, a PDF page/selection link, its type,
hidden geometry (`%%hl:...%%`), and a block ID (`^h...`). Follow the page link
to revisit the source. Use Obsidian's block-link completion to link to one
exact highlight from a research note.

Your own notes can use any content and format. You can link them to a PDF or
a highlight wherever useful. An indented comment beneath a generated item is
also supported; the plugin preserves those comments when sorting. See
[[guides/Linking Notes|Linking notes]] for the basics.

The proxy note is the highlight record. Removing a highlight entry removes
its overlay. Preserve geometry, type fields, page links, and block IDs.
The PDF itself stays unchanged: opening it in another PDF reader will not show
these overlays. Keep the PDF and its proxy note together when sharing or backing up.
Replacing a PDF with another edition may invalidate the stored positions.

Source: [Easy PDF Highlight documentation](https://github.com/maxdokukin/easy-pdf-highlight).
