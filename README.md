# The Jordan Family Bible — 1862

A page-by-page heritage record of the leather-bound family Bible printed in 1862,
preserved alongside a modern comparison Bible and the custodian's notebook.

Hosted at **[www.jordanhisstory.com](https://www.jordanhisstory.com)**.

Dedicated to Sylas, and to the hands that held this Bible before ours — beginning
with those who crossed on the *Ark* and the *Dove* in 1634 and made landfall at
St. Clement's Island in what is now St. Mary's County, Maryland.

---

## What's in the project

The project is three documents working together.

**The application** (`index.html`) is the interactive page-by-page record. It
holds the Bibles, the Pages, the Family Register, the Journal entries, the People,
the Comparisons, the Inserts, the chain of Custodianship, the Scribes, and the
work Sessions. Records are entered through the tabs at the top of the page and
stored locally in the browser. The Dashboard is the home view; the Data & Backup
tab is where the project can be exported to JSON for backup or re-imported on a
new device.

**The companion reading** (`companion.html`) is a heritage essay reading Genesis
1 verse by verse across both Bibles, with the custodian's notebook entries woven
in as a third voice. Eight sections cover the framing, the 1862's Reformation-era
calendar at the chapter head, the philosophy behind formal-equivalence and
dynamic-equivalence translations, all thirty-one verses of Genesis 1 plus the
seventh-day rest in parallel with commentary, a thematic analysis of the
notebook, the difference between each era's marginal apparatus, and a closing
section on what the next reading session should pursue.

**The photograph manifest** (`manifest.html`) is the catalogue of every
photograph in the heritage archive — the Bible pages, the notebook scans, the
cleaned derivatives, and the project files themselves. Each entry carries the
filename, a content description, and a direct link to view the original in Google
Drive.

---

## Access code

The application is gated behind a small access code so family content stays for
family eyes. The current code is **1634** — the year of the Ark and Dove landing
at St. Clement's Island. The code can be changed by editing one line near the
bottom of the JavaScript section in `index.html`:

```javascript
const GATE_CODE = "1634";  // change this to set a different code
```

Once entered with the "Remember on this device" box checked, the gate skips on
subsequent visits from that same browser. Each device or browser is gated
independently — the code is the entry tax, not a per-user login.

---

## How the file structure works

The application references photographs by filename. When the application says a
notebook scan called `89373_warm.jpg` should appear next to a journal entry, the
browser looks for a file with exactly that name in the same folder as the HTML.
For all the images to display, the image files must sit in the repository
alongside the HTML files. The expected layout:

```
/                         (the repository root, served at www.jordanhisstory.com)
├── index.html            (the application — start here)
├── companion.html        (the Genesis 1 reading)
├── manifest.html         (the photograph manifest)
├── README.md             (this file)
├── 89309.jpg             ┐
├── 89310.jpg             │
├── ...                   ├─ 1862 Bible pages (camera originals)
├── 89346.jpg             ┘
├── 89373_warm.jpg        ┐
├── 89373_mono.jpg        │
├── ...                   ├─ Cleaned notebook scans
├── 89388_mono.jpg        ┘
├── 20260522_214011.jpg   ┐
├── 20260522_214020.jpg   │
├── ...                   ├─ Modern Bible front matter (Drive originals)
└── 20260522_214251.jpg   ┘
```

The records inside the application are pre-loaded automatically the first time
each visitor opens the page. The seed button on the Data & Backup tab is still
available for manual reloading after a data wipe.

---

## How to update the site

Updates happen by uploading replacement files to the GitHub repository. From
the web interface this is a four-step process for each file:

1. Open the file in the repository on GitHub.
2. Click the pencil icon (edit) or the upload button (if replacing wholesale).
3. Paste or attach the new content.
4. Commit the change.

GitHub Pages rebuilds the site automatically after each commit. The new content
usually appears at www.jordanhisstory.com within one to five minutes. A hard
refresh (Ctrl+Shift+R, or pull-to-refresh on mobile) ensures the browser pulls
the latest version rather than serving from cache.

For new photographs added to a reading session, the workflow is to upload the
photograph files to the repository (or to the Google Drive folder and then to the
repository), update the application to add a Page or Journal record referencing
the new filename, export the application's JSON from the Data & Backup tab to
preserve the additions, and commit both the new image files and the updated
`index.html` to the repository together.

---

## Where the source material lives

The Google Drive folder titled "Jordan His Story" holds the canonical
source archive: the original camera photographs from each reading session, the
cleaned derivative scans, and the project files at every version. The manifest
document (`manifest.html`) catalogues the contents of that folder with direct
"View" links to each file.

The GitHub repository serving www.jordanhisstory.com is the public-facing copy.
It contains what the family sees. The Drive folder is the working archive that
holds the raw material the public site is built from.

---

## For the next custodian

The chain of Custodianship in the application is meant to be added to. When the
project passes from one keeper to the next, the new keeper:

1. Receives the access code and the credentials for the Drive folder and the
   GitHub repository.
2. Adds a Custodian row in the application showing the date the project passed
   to them and any notes about the transfer.
3. Updates this README's "Hosted at" line if the domain changes, and the access
   code if they choose to set a new one.

The project is designed to live across generations, not to be a one-person work.
Each custodian's contributions become part of the record. Future readings of new
chapters, new family register entries discovered in the Bible, new photographs of
inserts and ephemera, new custodianship rows — all of it belongs in the
application and gets committed to the repository alongside the photographs it
references.

---

## Project history

The project was begun in May 2026 by Clifton Wayne Jordan, who received the 1862
Bible into his custody from prior holders in the family. The first reading
session, on the eve of Memorial Day 2026, covered Genesis 1 across both the
1862 and a modern comparison Bible, with notes kept in a spiral notebook
documenting the Creation week day by day. The Maryland Dove — the modern
reconstruction of the ship that brought the family to Maryland in 1634 — was
launched at the Chesapeake Bay Maritime Museum in 2022 and is moored at Historic
St. Mary's City, within sight of where the family first stepped ashore.

---

*Percussa resurgo* — Being struck down, I rise again.
