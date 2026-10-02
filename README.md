# Obsidian Research Starter

Read a paper, highlight what matters, and ask Codex to turn those highlights
into connected research notes without leaving Obsidian.

**Two workflows, two community plugins:**

- **PDF → searchable Markdown.** Put a PDF in `papers/`, select text, and choose
  a semantic color. Easy PDF Highlight creates `<filename>_highlights.md`
  next to it, groups passages by meaning, and links them back to the PDF.
- **Your vault → an agent workspace.** Open an integrated Terminal tab and run
  `codex`. Ask it to find related passages, organize notes, or draft a synthesis
  with links to the underlying evidence.

## Get the vault from GitHub

Download this repository with **Code → Download ZIP**, extract it, and open the
extracted folder as an Obsidian vault. Keep the hidden `.obsidian` folder.

If you use Git, clone it instead:

```sh
git clone https://github.com/seunghyukoh/obsidian-research-starter.git
```

Each teammate uses their own copy. Plugins are installed separately through
Obsidian using the steps below. The example notes demonstrate wiki links without
requiring any particular note format.

## Quick start

1. Extract the shared ZIP, keeping the hidden `.obsidian` folder. Move or rename
   `obsidian-research-starter` wherever you keep your notes.
2. In Obsidian **desktop**, choose **Open folder as vault** and select that folder.
   Use a current desktop release compatible with the plugins you install.
3. Under **Settings → Community plugins**, allow community plugins and click
   **Browse**. Install **Easy PDF Highlight** by **Max Dokukin** and **Terminal**
   by **polyipseity**, then enable each one. This starter includes settings only;
   each teammate installs the plugins directly from Obsidian.
   Confirm the five Korean color labels in **Settings → Easy PDF Highlight**.
   See [Plugin setup](#plugin-setup) if the defaults appear instead.
4. Open [Home](Home.md), then [Highlight Playground.pdf](papers/Highlight%20Playground.pdf).
   Select a sentence and click a color. Your first highlight creates
   `papers/Highlight Playground_highlights.md`.
5. Search for that sentence with **Cmd/Ctrl+Shift+F**. Open the result and follow
   its page link back to the PDF. You have completed the first workflow.
6. Complete the one-time terminal setup below, then press **Option/Alt+Shift+T**
   while a note has focus. Select the integrated profile for your OS.
7. Confirm that the terminal is at this vault's root, then run `codex` and sign in.
   Try: `Read AGENTS.md and summarize my paper highlights with source links.`

## Plugin setup

Install these two plugins through **Settings → Community plugins → Browse**:

| Plugin | Author | Directory page |
| --- | --- | --- |
| Easy PDF Highlight | Max Dokukin | [Open plugin page](https://obsidian.md/plugins?id=easy-pdf-highlight) |
| Terminal | polyipseity | [Open plugin page](https://obsidian.md/plugins?id=terminal) |

The `.obsidian/plugins/<id>/data.json` files contain starter preferences only.
Plugin code and manifests are intentionally absent; an empty enabled-plugin list
avoids trying to load plugins before installation. Click **Install**, then **Enable**
for each plugin. Obsidian will maintain the enabled-plugin list on your machine.

After installation, check that Easy PDF Highlight has the five semantic labels
from [Reading Workflow](guides/Reading%20Workflow.md), with **Create highlights note**
enabled and **Note name** set to `{{filename}}_highlights`. Also check the Terminal
profiles and the **Option/Alt+Shift+T** shortcut.

If installation replaces the preset settings, close Obsidian and restore only
the two plugin `data.json` files from the original starter ZIP into their matching
`.obsidian/plugins/<id>/` folders, then reopen Obsidian. Do this before making personal
changes; restoring a preset replaces that plugin's current settings. If you have
already customized it, apply the relevant settings manually instead.

## One-time terminal setup

Each teammate installs the plugins, Python, and Codex on their own computer.
No account, token, model, or global Codex configuration is included in this vault.

**macOS (with Homebrew):** In your usual terminal, run:

```sh
brew install python
brew install --cask codex
python3 --version
codex --version
```

Alternatively, use the installation method in the official
[Codex CLI guide](https://developers.openai.com/codex/cli).
Restart Obsidian after installation so new executables can be discovered.

**Linux:** install Python 3.9+ and Codex using the official guide. The bundled
integrated profile uses `/bin/bash --login`; change it in Terminal settings
if your shell is elsewhere.

**Windows:** install Codex using the official Windows instructions linked from
the CLI guide, then use the bundled Command Prompt profile. Configure its
Python executable if needed; `python3` may be named `python` on your machine.
Terminal's optional Python dependencies and profile checks are described in
its [versioned installation guide](https://github.com/polyipseity/obsidian-terminal/blob/3.27.2/README.md#installation).
A WSL setup needs a separate `wsl` profile and a Codex installation inside WSL.

In **Settings → Terminal → Profiles**, open your integrated profile and use
**Check** for the Python configuration. macOS/Linux require Python 3.9+.
If automatic discovery fails, use the path returned by `command -v python3`
in your usual terminal. This is a per-machine adjustment.

On macOS/Linux, `pwd` should show this vault and `ls AGENTS.md` should succeed.
On Windows Command Prompt, use `cd` and `dir AGENTS.md` to check. The shortcut
opens at the vault root; a folder context-menu terminal may start elsewhere.

```sh
codex
```

If the terminal display behaves oddly, try `codex --no-alt-screen`.
Sign in with your own account on first run. Start Codex from the vault root
so it discovers this vault's `AGENTS.md` instructions.

## Included

| Location | Purpose |
| --- | --- |
| `Home.md` | Start here inside Obsidian |
| `papers/` | PDFs and their generated highlight notes |
| `notes/` | Free-form notes and simple linking examples |
| `projects/` | A simple example page linking to other notes |
| `guides/` | Reading workflow, agent prompts, and troubleshooting |
| `AGENTS.md` | Agent conventions and highlight-preservation rules |
| `.obsidian/` | Portable Obsidian and plugin settings; no plugin code |

Colors keep the original Korean labels and palette. Documentation is in
English; see the meaning table in [Reading Workflow](guides/Reading%20Workflow.md).
You can rename labels under **Settings → Easy PDF Highlight**.

## New to linking notes?

Open [Example Project](projects/Example%20Project.md) and follow its links to the
two example notes. Type `[[` in a note to choose another note from suggestions.
[Linking notes](guides/Linking%20Notes.md) shows the syntax, custom labels, and backlinks.
These examples demonstrate links only; no note content or structure is required.

## Share with the team

Share [this GitHub repository](https://github.com/seunghyukoh/obsidian-research-starter)
or its original ZIP. Each teammate makes their own copy. This is a starter vault,
not a live synchronization service. Keep `.obsidian/` when copying it.

After adding real papers and notes, your working vault is no longer a clean
starter. Use the original distribution for onboarding someone else.
The `.gitignore` excludes local state and new PDFs by default, but it does not
hide your Markdown notes. Keep personal research in your own copy or repository;
only contribute reusable starter changes back here.

The presets were prepared against **Easy PDF Highlight 0.1.0** and **Terminal 3.27.2**.
Installation through Obsidian may provide newer versions; versions are not pinned.
Confirm the color labels and terminal profile after installation or updates.
No plugin implementation, source archive, or third-party license bundle is distributed.
The practice PDF is an original document created for this starter.

## Checks before using this on a new machine

- A first selection creates a highlight note beside the practice PDF.
- A second highlight with another color creates another meaning section.
- Global search finds a selected sentence, and its page link opens the PDF.
- The terminal opens in the vault root, and `codex --version` succeeds.
- Codex can read `AGENTS.md` and cite a highlight in a new note.

Package checks cover configuration syntax, document links, the selectable
practice PDF, and the absence of plugin code or personal runtime state in the ZIP.
Obsidian GUI behavior and Codex sign-in must still be checked on the recipient's
machine. See [Troubleshooting](guides/Troubleshooting.md) if anything fails.
