# Docket

A small pair of offline browser tools for commercial insurance policy processing — no install, no server, no data ever leaves your device.

## What's inside

### 🗂️ Docket (`index.html`)
The main tool. Creates a job folder and renames your checklist Excel + policy documents to a consistent naming convention, in one click per file.

- Enter policy period, LOB, insured name, and policy number → generates the job tag automatically
- Remembers your last-used period / previous period between sessions
- Creates the job folder on your computer (via the browser's native folder picker)
- Renames and saves your checklist Excel into that folder
- Renames and saves each PDF (Current / Previous / Application / Quote / Proposal / Binder) into the same folder, with overwrite protection if a file already exists
- A pinned banner always shows which LOB/insured you're currently working on
- Progress chips show which of the six document types are still missing
- "Start next policy" resets the form for the next job without a page reload
- Generates two ready-to-paste notes for your checklist:
  - **Starting the checklist** — which documents were available / not available
  - **Finishing the checklist** — the standard "Please see the attached [LOB] Policy Checklist" reminder line for whichever LOB you're on

**Privacy:** this tool never opens, reads, or analyzes the contents of any file. It only takes the file you select and writes it to disk under a new name.

### 📊 Forms Checker (`forms-checker.html`)
Compares Previous vs Current forms & endorsements schedules and flags additions, removals, edition changes, and possible typos. Fully offline — pasted data is never uploaded. Linked from Docket's header.

## Requirements

Both tools use the browser's **File System Access API**, which needs a **Chromium-based desktop browser** — **Chrome or Edge**. Firefox and Safari are not supported for the folder/file-saving features.

## Running it

- **Locally:** download the repo, open `index.html` (Docket) or `forms-checker.html` directly in Chrome/Edge.
- **Hosted:** enable GitHub Pages on this repo (see below) and open the pages from anywhere.

## GitHub Pages setup

1. Go to **Settings → Pages** in this repo.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
4. After a minute, your site will be live at:
   `https://pilipjan.github.io/docket/` → Docket (main tool)
   `https://pilipjan.github.io/docket/forms-checker.html` → Forms Checker
5. The File System Access API requires a secure context — GitHub Pages serves over HTTPS, so this works automatically.

## Notes

- All processing happens client-side. No backend, no analytics, no external requests.
- Both files are self-contained (HTML/CSS/JS in one file each) — safe to copy anywhere.
