# Camp Directory Builder — User Manual

This manual walks you through every part of Camp Directory Builder, from preparing your files to printing the finished directory. It assumes no technical background. Wherever a technical term or abbreviation comes up, it's explained right there.

---

## Contents

1. [What the app does](#what-the-app-does)
2. [What you'll need](#what-youll-need)
3. [Opening the app](#opening-the-app)
4. [Preparing your roster CSV](#preparing-your-roster-csv)
5. [Preparing your photo PDF](#preparing-your-photo-pdf)
6. [Step 1 — Camp Details](#step-1--camp-details)
7. [Step 2 — Roster CSV](#step-2--roster-csv)
8. [Step 3 — Photo PDF](#step-3--photo-pdf)
9. [Editing a photo](#editing-a-photo)
10. [Editing a listing](#editing-a-listing)
11. [Saving your edits](#saving-your-edits)
12. [Downloading all photos](#downloading-all-photos)
13. [Step 4 — Generate](#step-4--generate)
14. [What the finished directory looks like](#what-the-finished-directory-looks-like)
15. [Printing tips](#printing-tips)
16. [Troubleshooting](#troubleshooting)
17. [Frequently asked questions](#frequently-asked-questions)
18. [Glossary](#glossary)

---

## What the app does

Making a camp directory by hand means copying and pasting dozens (or hundreds) of names, photos, and bios into a layout program, then fixing everything when one person's listing pushes the whole page out of place.

Camp Directory Builder does that work for you. It takes:

- **a roster** (a spreadsheet of everyone's details), and
- **a photo PDF** (a document where each person's photo is on a page with their name),

…matches each photo to the right person, and produces a finished, two-column directory PDF ready to print.

**Everything happens inside your web browser on your own computer.** Your files are never uploaded anywhere.

---

## What you'll need

- **A computer, iPad, or iPhone** with a modern web browser — Safari, Chrome, Firefox, or Edge.
- **An internet connection** when you first open the app. The app downloads a few helper tools it needs to read and create PDFs. (Your files are *not* sent over the internet.)
- **Your roster**, saved as a CSV file. See [Preparing your roster CSV](#preparing-your-roster-csv).
- **Your photo PDF.** See [Preparing your photo PDF](#preparing-your-photo-pdf).
- *(Optional)* **A cover photo** — a JPG or PNG image for the front of the directory.

> **JPG and PNG** are the two most common picture file types. Photos from phones and cameras are usually JPG (sometimes spelled JPEG, for *Joint Photographic Experts Group*, the committee that created it). PNG (*Portable Network Graphics*) is common for screenshots and graphics.

---

## Opening the app

1. Find the file `camp-directory-builder.html` (in your Downloads folder, or wherever you saved it).
2. **Double-click it.** It opens in your default web browser.

That's it — there's nothing to install.

**On an iPhone or iPad:** save the file to the Files app, tap it, then tap the Share button and choose to open it in Safari. Or, if your group has put the app online (see the README's "Putting it online" section), just visit the web link.

You'll see the title **Camp Directory. Builder** at the top, and a row of four numbered tabs:

**1 Camp Details · 2 Roster CSV · 3 Photo PDF · 4 Generate**

You'll work through them left to right. You can click back to an earlier tab at any time to change something.

---

## Preparing your roster CSV

### What is a CSV?

**CSV** stands for **Comma-Separated Values**. It's a plain, simple version of a spreadsheet: each row is one line of text, and the columns are separated by commas. Every spreadsheet program can save one:

- **Excel:** File → Save As → choose **CSV UTF-8 (Comma delimited)**.
- **Numbers (Mac):** File → Export To → **CSV…**
- **Google Sheets:** File → Download → **Comma Separated Values (.csv)**.

> **UTF-8** is a way of storing text that handles accented letters (é, ñ, ü) and other special characters correctly. If you have a choice, pick UTF-8.

### Required layout

- **Row 1 must contain the column headings.**
- **Every row after that is one person.**
- Blank rows are ignored.

### Column headings the app recognizes

| Column heading | What to put in it | Example |
|---|---|---|
| `First Name` | First name | `Maya` |
| `Last Name` | Last name | `Okafor` |
| `Date of Birth` | Full date **or** just month and day | `2006-12-21` or `10-09` |
| `Registrations` | Any text containing the word "Camper" or "Staff" | `Oregon 2026 – Camper` |
| `GI Address` | Street address | `123 Fir Lane` |
| `GI City` | City | `Eugene` |
| `GI State/Province` | State or province | `OR` |
| `GI Email` | Email address | `maya@example.com` |
| `GI Phone` | Phone number | `541-555-0100` |
| `GI Host Family` | `Yes` if they're a host family | `Yes` |
| `GI Directory Bio` | Their short self-description | `I love rock climbing and bad puns…` |

**Only First Name and Last Name are truly required.** Leave any other column empty and that detail simply won't appear in that person's listing.

> **Why "GI"?** It stands for "General Information" — the prefix used by the registration system NBTSC exports from. The headings need to match exactly, so keep the "GI" even if your system doesn't use it.

### How Camper vs. Staff is decided

The app reads the `Registrations` column for each person:

- If it contains the word **"Staff"** and *not* the word "Camper" → the person goes in the **Staff** section.
- Anything else → the person goes in the **Campers** section.

Capital letters don't matter. You can always change anyone's group by hand in Step 2.

### Tips

- **Bios with commas, quotation marks, or line breaks are fine.** Spreadsheet programs automatically wrap those in quotes when saving a CSV, and the app reads them correctly.
- **Emoji (😀 🌲) will be removed** from the printed directory. The fonts used in the PDF can't display them. Everything else in the bio stays.
- If you've used the app before and clicked **Save Edits to CSV**, you can load that saved file here — it uses exactly the right headings.

---

## Preparing your photo PDF

The app expects a PDF where **each person's photo sits on a page together with their printed name**. Many registration and yearbook tools can export something like this — for example, one page per person with a photo and a name caption.

The app works through the PDF page by page:

1. It **pulls out the photo** on each page (the actual image, not a screenshot of the whole page).
2. It **reads the text** on that page to find a name.
3. It **compares that name to your roster** to decide who the photo belongs to.

For best results:

- **One person per page.**
- **The name on the page should match the roster** as closely as possible. Small differences are OK — the app uses "fuzzy matching," which means it can tell that "Jon Smith" probably means "John Smith."
- **The PDF needs real text, not a picture of text.** If you can click and highlight the name in a PDF viewer, you're fine. If you can't, the app won't be able to read names automatically — but you can still assign photos by hand.

---

## Step 1 — Camp Details

This page sets up everything about the directory itself: its title, cover, and look.

### Basic information

| Field | What it does |
|---|---|
| **Camp / Organization Name** | The main title on the cover and in the top corner of every page. |
| **Subtitle** | Appears under the name on the cover and alongside it in page headers. Example: *Myrtlewood 2026 · Directory*. |
| **Footer line** | A short line repeated at the bottom of every page. Example: *2026 Myrtlewood Directory*. |
| **Age reference date** | The date the app uses to work out everyone's age. It's set to **today** automatically. Change it to the first day of camp if you want ages to be accurate for camp week. |
| **Cover quote** *(optional)* | A quotation for the cover. |
| **Cover photo credit** *(optional)* | Gives credit to whoever took the cover photo. Example: *Photo by Kiki, Oregon 2025*. |
| **Cover photo** *(optional)* | Drag a JPG or PNG onto the box, or click the box to choose a file. A small preview appears once it's loaded. |

### Placeholder silhouette

**"Show a placeholder silhouette icon for anyone missing a photo"** — when this box is ticked (the default), anyone without a photo gets a simple gray head-and-shoulders outline in their photo square. Untick it to leave the square empty instead.

### Typography (fonts and sizes)

"Typography" just means the style and size of the lettering. You can set a font and size for five parts of the directory:

| Part of the directory | Default font | Default size |
|---|---|---|
| Person's Name | Helvetica (sans-serif) | 12 |
| Age / Address Info | Helvetica (sans-serif) | 8.7 |
| Description (Bio) | Times New Roman (serif) | 9 |
| Campers / Staff Divider | Helvetica (sans-serif) | 9.5 |
| Page Header & Footer | Helvetica (sans-serif) | 8.5 |

The font choices are **Times New Roman**, **Helvetica**, and **Courier**:

- **Serif** fonts (like Times New Roman) have small "feet" on the ends of the letters. They're traditional and easy to read in long paragraphs.
- **Sans-serif** fonts (like Helvetica) don't have those feet ("sans" is French for "without"). They look clean and modern and are great for names and labels.
- **Courier** looks like an old typewriter. Every letter takes up the same width.

These three fonts are built into every PDF reader in the world, so your directory will look exactly the same on every computer and printer.

**Sizes are in "points."** A point is a printing measurement: 72 points = 1 inch. Most books use 10–12 point text. You can type sizes with a decimal (like 8.7) for fine control.

**If you don't touch any of these, you get the default design.**

### Spacing

Two settings control the breathing room between listings, both measured in points:

| Setting | What it controls | Default |
|---|---|---|
| **Space before dividing line** | The gap between the end of someone's bio and the thin line beneath it. This is the blank area people can use for handwritten notes. | 20 |
| **Space before next listing** | The gap between that line and the start of the next person. | 18 |

Bigger numbers = more writing space, but fewer people per page (so more pages to print).

### Moving on

Click **Next: Roster CSV →**. If you've left any of the main fields blank, a message asks if you want to continue anyway. Click **OK** to move on — those parts will just be blank in the PDF until you come back and fill them in.

---

## Step 2 — Roster CSV

1. **Drag your CSV file** onto the box that says *"Drop your roster CSV here, or click to browse"* — or click the box and choose the file.
2. The app reads it right away. Below the box you'll see a short status line, then three summary boxes:
   - **Campers** — how many people were placed in the Campers group.
   - **Staff** — how many were placed in Staff.
   - **Total People** — everyone together.
3. Below that is a table listing every person with three columns:
   - **Name**
   - **Group** — a dropdown showing Camper or Staff. **Change it here** if the app guessed wrong.
   - **Detected From** — shows the text from the Registrations column that the app used to make its guess, so you can see *why* it chose that group.
4. When it all looks right, click **Next: Photo PDF →**. (There's a Next button both above and below the list, so you don't have to scroll to the bottom of a long roster.)

**Save Edits to CSV** is also available here — see [Saving your edits](#saving-your-edits).

---

## Step 3 — Photo PDF

### Loading and extracting

1. **Drag your photo PDF** onto the box that says *"Drop the directory PDF (with photos) here, or click to browse."*
2. A progress panel appears with a spinning film-reel icon and the word **"Developing…"** along with a progress bar and a note about which page it's reading. Large PDFs can take a minute or two — let it finish.

The app also tries to **straighten sideways photos automatically**. Some PDFs store photos rotated and only *display* them upright; the app works out the correct direction and fixes it. If a photo still comes out sideways, you can rotate it yourself (see [Editing a photo](#editing-a-photo)).

### Reviewing the matches

When extraction finishes you'll see three summary boxes:

- **Matched** — people who now have a photo.
- **No Photo** — people still without one.
- **Photos Extracted** — the total number of photos found in the PDF.

Below that is the review table. Each row is one person:

| Column | What it shows / does |
|---|---|
| *(thumbnail)* | A small preview of their photo, if they have one. |
| **Name** | The person's name. |
| **Group** | Camper or Staff. |
| **Match** | How the photo was matched: an **exact** match, a **fuzzy** (close-but-not-identical) match, a **manual** choice you made, or **no photo**. Color-coded badges make problems easy to spot. |
| **Photo** | A dropdown listing every extracted photo. Use it to **assign the right photo** to anyone marked "no photo," or to fix a wrong match. |
| **Edit Photo** | Opens the photo editor (or **Add Photo** if they don't have one yet). |
| **Edit** | Opens the listing editor to change this person's text details. |

**Work down the list** and fix anyone marked "no photo" or anyone whose fuzzy match looks wrong.

When you're done, click **Next: Generate →** (available above and below the table).

---

## Editing a photo

Click **Edit Photo** (or **Add Photo**) on anyone's row. A window opens showing their full photo with a **square frame** on top. Whatever's inside the square is what appears in the directory.

| Control | What it does |
|---|---|
| **Drag the square** | Move it to choose which part of the photo to keep. |
| **Zoom slider** | Make the square smaller to zoom in closer on a face, or larger to show more. |
| **↺ Rotate** | Turn the photo a quarter-turn to the left (counterclockwise). |
| **↻ Rotate** | Turn the photo a quarter-turn to the right (clockwise). |
| **Import Photo** | Replace the photo with a different picture from your computer. The app automatically labels it with this person's name, so the file's original name doesn't matter. |
| **Reset** | Undo your cropping and rotation and go back to the original centered view. |
| **Cancel** | Close without saving changes. |
| **Apply** | Save your changes and close. |

**If someone has no photo at all**, the window shows an empty space with an **Import Photo** button. Click it to add one.

Your crop and rotation changes only affect that one person's square in the directory — the original PDF is never changed.

---

## Editing a listing

Click **Edit** on anyone's row to open the listing editor. It shows every piece of text that appears in their directory entry:

- **First Name** and **Last Name**
- **Date of Birth** — type it as `YYYY-MM-DD` (year-month-day, e.g. `2006-12-21`), or as `MM-DD` (month-day, e.g. `10-09`) if you only know the birthday and not the year.
- **Group** — Camper or Staff
- **Address**, **City**, **State/Province**
- **Phone** and **Email**
- **Host Family** — yes or no
- **Bio** — their description

Click **Save** to keep your changes or **Cancel** to throw them away.

> **How ages appear:** if a full birthdate is given, the listing shows something like *Age 19 · Dec 21, 2006*, calculated as of the **age reference date** from Step 1. If only a month and day are given, it shows *Birthday: Oct 9*.

Edits you make here live inside the app while it's open. **To keep them for next time, use Save Edits to CSV** (next section).

---

## Saving your edits

The app doesn't remember anything once you close the browser tab. To protect your work, click **Save Edits to CSV** (on the Roster and Photo pages).

This downloads a new CSV file containing the whole roster **including every change you've made** — group changes, fixed typos, updated bios, and so on. The file is named with the date and time, for example:

`roster_edits_2026-07-20_1432.csv`

(That's July 20, 2026, at 2:32 pm.)

Next time, load this file in Step 2 instead of the original. It uses exactly the column headings the app expects, so everything comes back in correctly.

> **Note:** Photo crops and rotations aren't stored in the CSV — a CSV can only hold text. To keep your finished photos, use **Download All Photos**.

---

## Downloading all photos

**Download All Photos** saves every matched photo — *with your crops and rotations applied* — into a single **ZIP file**.

> **ZIP** is a way of packing many files into one compressed bundle, like putting lots of papers into a single envelope. Double-click a ZIP on a Mac or PC to open it and see the files inside.

Each photo is named after its person, so this is a handy way to keep a tidy, ready-to-use photo set for next year, a slideshow, or name tags.

---

## Step 4 — Generate

Click **Generate Directory PDF**.

A progress panel shows what the app is doing (building the cover, placing photos, laying out pages) with a progress bar. When it's done:

- **The PDF downloads automatically** to your Downloads folder. It's named after your camp — for example, `Not Back to School Camp.pdf`.
- A message confirms how many photos were included, e.g. *"Your directory has downloaded, with 80 photos."*
- **If some photos couldn't be included**, the message tells you how many and why, so you can go back and fix them.

Open the PDF to check it. If you want to change anything, just go back to any earlier tab, make the change, and generate again. It only takes a few seconds.

---

## What the finished directory looks like

- **Cover page** with your camp name, subtitle, cover photo, quote, and photo credit.
- **Campers section**, then a fresh page for the **Staff section**. Each section is labeled with a small boxed heading at the top of its pages.
- Within each section, **everyone is sorted alphabetically by first name**.
- **Two columns per page**, fitting as many people as can be read comfortably.
- Each listing contains:
  - a **square photo** (or silhouette placeholder),
  - their **name** in bold,
  - their **age or birthday**,
  - their **location and contact details**,
  - their **bio**,
  - **blank space for handwritten notes**, then a thin dividing line.
- **Page header** with the camp name and subtitle; **page footer** with your footer line and page number.
- Page size is US Letter (8½ × 11 inches).

---

## Printing tips

- Print at **100% / "Actual Size."** Avoid "Fit to Page," which can shrink the text.
- **Double-sided printing** works well and halves your paper use.
- For a booklet, most print shops can take the PDF as-is and bind it with staples or a spiral.
- Do a **one-page test print** first to check the font sizes and note space feel right on paper.

---

## Troubleshooting

**The app looks broken or nothing happens when I drop a file.**
You probably opened it without an internet connection, so the helper tools didn't load. Connect to the internet and refresh the page (Mac: ⌘ Command + R; Windows: Ctrl + R).

**My CSV loaded, but names or details are missing.**
Check that the first row of your CSV has the exact headings listed in [Preparing your roster CSV](#preparing-your-roster-csv) — spelling and spacing matter. Re-save the file as **CSV UTF-8** if accented letters look garbled (for example, "Ã©" instead of "é").

**Everyone ended up as a Camper (or the groups are wrong).**
The `Registrations` column must contain the word "Staff" for staff members. Fix it in the spreadsheet, or just change each person's Group dropdown in Step 2.

**Lots of people show "no photo."**
- The names in the PDF might be quite different from the roster (nicknames, maiden names). Assign those photos by hand with the Photo dropdown.
- The PDF's names might be pictures rather than real text. Try highlighting a name in a PDF viewer — if you can't, the app can't read it either. Assign photos by hand.

**A photo is sideways or upside down.**
Click **Edit Photo** and use the **Rotate** buttons, then **Apply**.

**A photo is cropped badly (top of head cut off, etc.).**
Click **Edit Photo**, drag the square and adjust the zoom, then **Apply**.

**The generate message says some photos didn't embed.**
That photo file is probably damaged or in an unusual format. Use **Edit Photo → Import Photo** to replace it with a fresh JPG or PNG.

**Emoji disappeared from someone's bio.**
That's expected — the standard PDF fonts can't draw emoji, so they're removed to keep the PDF from breaking.

**It's slow on my iPhone or iPad.**
Very large photo PDFs take a lot of memory. Try a computer, or close other apps and browser tabs first.

**I closed the tab and lost my changes.**
Unfortunately the app can't recover them. Next time, click **Save Edits to CSV** (and **Download All Photos** if you edited photos) before closing.

---

## Frequently asked questions

**Is my data uploaded anywhere?**
No. The app reads your files inside your browser, on your own device. Nothing is sent to a server — not even when the app is hosted on GitHub Pages.

**Do I need to install anything?**
No. It's a single web page file. Just open it in a browser.

**Can I use it without internet?**
You need internet when you first open the page so it can load its PDF tools. After it's loaded, your work happens locally.

**Can I change the order (for example, sort by last name)?**
Not currently — listings are always sorted by first name within each section.

**Can I add someone who isn't in the CSV?**
Add them as a new row in your spreadsheet, re-save the CSV, and load it again in Step 2. (Tip: save your edits first so you don't lose other changes.)

**Can I use fonts other than Times New Roman, Helvetica, and Courier?**
Not at the moment. Those three are built into every PDF reader, which guarantees the directory looks identical everywhere it's opened or printed.

**Does it work for groups other than camps?**
Yes — any group with a roster and photos. Just use "Camper" and "Staff" in the Registrations column to divide people into the two sections (for example, members and leaders).

---

## Glossary

| Term | Plain-English meaning |
|---|---|
| **Browser** | The program you use to visit websites — Safari, Chrome, Firefox, Edge. |
| **CDN** | *Content Delivery Network.* A public server that hosts commonly used code so websites can load it quickly. The app uses one called cdnjs to load its PDF tools. |
| **CSV** | *Comma-Separated Values.* A plain-text spreadsheet file. |
| **Crop** | To trim a photo so only part of it shows. |
| **Fuzzy matching** | Matching names that are close but not identical, such as "Jon" and "John." |
| **GitHub** | A website for storing and sharing projects like this one. |
| **GitHub Pages** | A free GitHub feature that turns files in a project into a working website. |
| **HTML** | *HyperText Markup Language.* The language web pages are written in. The whole app is one HTML file. |
| **JPG / JPEG** | *Joint Photographic Experts Group.* The most common photo file type. |
| **PDF** | *Portable Document Format.* A document file that looks the same on every device and printer. |
| **PNG** | *Portable Network Graphics.* A common image file type, often used for graphics and screenshots. |
| **Point (pt)** | A printing measurement. 72 points = 1 inch. |
| **Sans-serif** | A font without small "feet" on the letters, like Helvetica. |
| **Serif** | A font with small "feet" on the letters, like Times New Roman. |
| **Typography** | The style, size, and arrangement of text. |
| **UTF-8** | A way of saving text that handles accented and special characters correctly. |
| **ZIP** | A single compressed file that holds many files inside it. |
