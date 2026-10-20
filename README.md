# obsidian-open

One static page, published with GitHub Pages, that opens a note in the firm's **Obsidian Team** vault.

Why it exists: the JHLT SOP Index is a claude.ai artifact, which can open ordinary web links in a new tab but
cannot launch `obsidian://` links itself. Its "Obsidian" buttons link here instead, and this page hands the
note to Obsidian.

- Link format: `https://jhugheslegalteam.github.io/obsidian-open/#f=<URL-encoded path inside the vault, ending .md>`,
  e.g. `#f=SOPs%2F09%20General%20Paralegal%20Materials%2F21%20Discovery.md`.
- The note path rides in the URL **fragment** (after `#`), which browsers never send to the web host.
- The page builds only `obsidian://open?vault=Obsidian%20Team&file=…`; any other input is refused.
- It holds no firm data. The repo is public because GitHub Pages on the firm's free plan requires it.
- The page also offers "Open in SharePoint instead" for devices without Obsidian.

Used by: `Jhugheslegalteam/Private-JH` → `artifacts/sop-index/` (`build.py` builds the links).
