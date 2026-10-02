# Troubleshooting

| Symptom                                  | What to check                                                                                                                                                                         |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Plugins are missing                      | Expected on first use: open **Settings → Community plugins → Browse**, install Easy PDF Highlight and Terminal, then enable them. Only their settings are included in the starter.    |
| Default colors appear after installation | See **Plugin setup** in the README. Restore the preset `data.json` from the original ZIP while Obsidian is closed, or apply the meaning table manually if you have existing settings. |
| Selecting PDF text shows no palette      | Enable Easy PDF Highlight, use Obsidian desktop, and try the included practice PDF. Image-only scans need OCR before text can be selected.                                            |
| No proxy note appears                    | Turn on **Create highlights note** in Easy PDF Highlight. A note is created on the first highlight, next to its PDF.                                                                  |
| Colors do not match their stored names   | This is intentional: `blue` renders peach, `red` lavender, and `purple` sky blue. See the meaning table in Reading Workflow.                                                          |
| A search shortcut searches the terminal  | Click a Markdown note first. Terminal intercepts shortcuts while focused.                                                                                                             |
| The terminal does not open               | Choose an integrated profile, check the shell executable, and use the profile's Python **Check** button. macOS/Linux need Python 3.9+.                                                |
| `python3` is not found                   | Set the profile's Python executable to your installed Python path. On Windows it may be called `python`.                                                                              |
| `codex` is not found                     | Verify it in your normal terminal, restart Obsidian, and check the login shell's PATH. On macOS/Linux, compare `command -v codex` in both terminals.                                  |
| The agent cannot find these notes        | Check the current directory. Reopen the **integrated terminal at vault root** from the command palette or use `codex -C "path/to/your/vault"`.                                        |
| Codex rendering or scrolling is odd      | Try `codex --no-alt-screen`; if needed, try a different renderer in Terminal settings.                                                                                                |
| The PDF looks clean in another reader    | Expected: the Markdown proxy stores the highlights; Obsidian draws the overlay.                                                                                                       |
| Highlights move after replacing a PDF    | Restore the exact PDF version used when highlighting. Page geometry belongs to that version.                                                                                          |

The shortcut **Option/Alt+Shift+T** opens an integrated terminal at the vault
root. If it conflicts with an OS shortcut, assign another key under
**Settings → Hotkeys → Terminal**.

Update the two plugins through Obsidian when appropriate, then retry the small
practice workflow. The presets were prepared for Easy PDF Highlight 0.1.0 and
Terminal 3.27.2; check settings compatibility after an update. The packaged
configurations are portable defaults; shell and Python paths may need adjustment
on another machine.

References: [Terminal installation and troubleshooting](https://github.com/polyipseity/obsidian-terminal/blob/3.27.2/README.md),
[Codex CLI setup](https://developers.openai.com/codex/cli).
