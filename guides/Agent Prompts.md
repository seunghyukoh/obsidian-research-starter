# Agent prompts

Open an integrated terminal at the vault root and run `codex`. Start with a
concrete question; the agent reads `AGENTS.md` for this vault's conventions.
Prompts can be in Korean or English. These are optional ideas, not a required
note format or workflow. Replace bracketed placeholders below, or ask for
whatever content and structure you prefer.

## Find evidence

> Find passages about [topic] in papers/*_highlights.md, including subfolders.
> Group the evidence by claim, method, result, and limitation. Link to the
> original highlight blocks and report when there is insufficient evidence.

## Turn highlights into a paper note

> Read the highlight note for [paper] and create a new note in the format
> I request. Separate the paper's claims from my interpretation,
> retain evidence links, and leave unknown information explicitly unverified.
> Do not modify the generated highlight note.

## Compare papers

> Compare [paper A] and [paper B] using my highlights. Write a note in notes/
> with their assumptions, methods, experimental settings, and limitations.
> Flag incompatible evaluation settings before comparing numbers. Cite evidence.

## Organize a topic

> Find existing notes related to [topic] and create notes/[topic] - Index.md
> with short descriptions and links. Identify duplicate or disconnected notes.
> Keep existing filenames and folder structure intact.

## Connect reading to a project

> Read projects/[project].md and the relevant paper highlights. Add a section
> with three testable ideas, the evidence for each, and the main uncertainty.
> Mark new ideas as proposals rather than established results.

## Draft an update

> Draft a team research update from [specific notes]. Include what we learned,
> what is still uncertain, and the next experiment, with links to the sources.
> Save the draft in notes/ and do not send it anywhere.

## Request the full paper explicitly

> Analyze the complete PDF [path], including experiments, limitations, and
> appendix. Use an available PDF extraction tool. If only highlights or partial
> text are available, state that limitation rather than implying a full reading.

For full-PDF reading, `pdftotext` is useful but optional. On macOS it is supplied
by `brew install poppler`. Searching existing highlight notes needs no PDF tool.
