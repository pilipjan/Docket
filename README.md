# Policy Organizer

A small pair of offline browser tools for commercial insurance policy processing — no install, no server, no data ever leaves your device.

## What's inside

### 🗂️ Policy Filer (`policy-filer.html`)
Creates a job folder and renames your checklist Excel + policy documents to a consistent naming convention, in one click per file.

- Enter policy period, LOB, insured name, and policy number → generates the job tag automatically
- Creates the job folder on your computer (via the browser's native folder picker)
- Renames and saves your checklist Excel into that folder
- Renames and saves each PDF (Current / Previous / Application / Quote / Proposal / Binder) into the same folder
- Generates two ready-to-paste notes for your checklist:
  - **Starting the checklist** — which documents were available / not available
  - **Finishing the checklist** — the standard "Please see the attached [LOB] Policy Checklist" line for whichever LOB you're on, so it's never forgotten
- A pinned banner always shows which LOB you're currently working on

**Privacy:** this tool never opens, reads, or analyzes the contents of any file. It only takes the file you select and writes it to disk under a new name.

### 📊 Insurance Forms Comparator (`index.html`)
Compares Previous vs Current forms & endorsements schedules and flags additions, removals, edition changes, and possible typos. Fully offline — pasted data is never uploaded.

## Requirements

Both tools use the browser's **File System Access API**, which needs a **Chromium-based desktop browser** — **Chrome or Edge**. Firefox and Safari are not supported for the folder/file-saving features.

## Running it

- **Locally:** download the repo, open `index.html` (or `policy-filer.html`) directly in Chrome/Edge.
- **Hosted:** enable GitHub Pages on this repo (see below) and open the pages from anywhere.

## GitHub Pages setup

1. Go to **Settings → Pages** in this repo.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
4. After a minute, your site will be live at:
   `https://pilipjan.github.io/Policy-Organizer-v1/` → Forms Comparator
   `https://pilipjan.github.io/Policy-Organizer-v1/policy-filer.html` → Policy Filer
5. The File System Access API requires a secure context — GitHub Pages serves over HTTPS, so this works automatically.

## Notes

- All processing happens client-side. No backend, no analytics, no external requests.
- Both files are self-contained (HTML/CSS/JS in one file each) — safe to copy anywhere.
