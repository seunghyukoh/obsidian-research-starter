# Linking notes

An Obsidian note is a Markdown file. Write whatever you like; no special
headings, properties, or note format are required.

## Open a link

Start at [[Example Project]], then follow its links to [[Example Note A]]
and [[Example Note B]]. In Reading view, click a link to open it. While
editing, use Cmd-click on macOS or Ctrl-click on Windows/Linux.

The examples only demonstrate connections. Their folders and contents are
not rules for organizing your own notes.

## Make your own link

1. Open any note and start typing two opening square brackets: `[[`.
2. Type part of another note's name and select it from the suggestions.
3. Obsidian inserts a link such as:

```text
[[Example Note A]]
```

That link points to the existing note. It does not copy the note's content.
A note can be linked from as many other notes as you like.

## Change the displayed text

Put `|` between the target and the label you want to show:

```text
[[Example Note A|my other note]]
```

Try it: [[Example Note A|my other note]]. Both labels open the same file.

## Link across folders or to a PDF

Selecting a note from the suggestions handles its location. If names are
ambiguous, include the folder path:

```text
[[notes/Example Note A]]
[[papers/Highlight Playground.pdf|practice PDF]]
```

Try it: [[notes/Example Note A]] or [[papers/Highlight Playground.pdf|practice PDF]].

## See what links here

Open [[Example Note B]] and look at the **Backlinks** pane. It shows notes
that link to this one, even when you have not added a return link yourself.
If the pane is hidden, open the command palette and search for **Backlinks**.

You can also open **Graph view** to see notes and their links as a diagram.
These are built-in Obsidian features; no extra plugin is needed.
