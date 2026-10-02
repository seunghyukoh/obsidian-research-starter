# Research vault instructions

This directory is an Obsidian research vault. Help the user find, connect,
organize, and write research notes while preserving source evidence.

## Navigation

- Start with `Home.md` and the user's specific question.
- Search relevant Markdown with `rg` or an available equivalent before reading
  broad collections. Search `papers/**/*_highlights.md` for annotated evidence.
- PDFs and generated highlight notes live together under `papers/`.
- Notes are free-form. Follow the user's preferred content, format, and location.
  The folders and examples are optional conveniences, not a required
  taxonomy, research process, or note schema.
- Use Obsidian wikilinks when helpful. The example notes demonstrate linking only;
  do not impose their content or structure on the user's notes.

## Preserve annotations

- Treat `*_highlights.md` as plugin-managed evidence. Read it freely; write
  synthesis to a separate note unless the user explicitly requests an edit.
- Never silently rewrite quoted text, PDF selection links, `(page:: ...)`,
  `(type:: ...)`, `%%hl:...%%` geometry, or `^h...` block IDs.
- Do not delete a proxy note or an entry as cleanup: it is the highlight record.
- Keep PDFs and their proxy notes paired. Before an explicitly requested move
  or rename, inspect the plugin's filename convention and update affected links.
- Do not edit plugin code, plugin state, or binary PDFs as routine note work.

## Evidence and writing

- Cite existing note paths, highlight blocks, and PDF page links.
- Distinguish source claims, the user's notes, your interpretation, and proposals.
- Do not invent quotations, results, authors, venues, or citations.
- Highlights are excerpts. Do not call their summary a complete paper analysis.
  For full-paper requests, extract/read the PDF and state coverage limitations.
- Use English documentation and comments by default. Respond in the user's
  language; preserve English technical terminology in Korean responses.
- Preserve existing user content and make focused edits. Ask before deletion
  or bulk moves. Do not publish or send notes without an explicit request.

## Verification

- Check new links against actual vault paths. Preserve YAML frontmatter if present; do not require it.
- Report changed notes and any evidence or verification limitations.
- Do not claim Obsidian GUI or authentication checks unless actually performed.
