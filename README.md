# Corpus

A vintage book you write your question into. Pick a topic of the body, write it on the front cover in ink, and the book opens, with pages assembled from real sources: Wikipedia, Wikimedia Commons and Europe PMC. No word in it is written, chosen or summarised by an AI.

**[Open the book →](#)** *https://devanshi208.github.io/corpus/*

---

## What it does

**You write on the cover, not into a search box.** The front of the book is aged leather with a paper label. Write what you want to learn about, press Enter, and the cover swings open to full screen.

**The first pages tell you where you are.** The left page shows what you wrote, which Wikipedia entry the archive matched, and other entries it might have meant. If it picked the wrong one, touch another and it rewrites the book. The right page is an index of what is on which page, and every line is a link.

**Real content, set in order.**
- A short *In plain words* summary from Simple English Wikipedia, when that article exists
- The full Wikipedia entry, with its real headings, paragraphs and lists. Every major section starts on a fresh page with a heading and a tiny picture beside it
- Pictures taken from the entry itself, each with a caption and a link to its file page for the author and licence
- Old anatomical plates from *Gray's Anatomy*, tinted sepia, where they match
- A **Terminology** page: technical terms from the entry, each defined by the opening lines of that term's own Wikipedia entry, unchanged
- **The research record:** how many papers Europe PMC lists on the topic, with the most relevant and most recent linked
- **Neighbouring subjects:** related topics with their paper counts, fewest first, so thinly researched corners stand out
- A **Colophon** listing every source and licence

**It says so when little is known.** If nothing matches, or the research is thin, the book says that plainly and shows nearby subjects. It never says "nobody has researched this", only "none found in these databases", because a missing record can mean the work sits under another name.

**Reading controls.** Turn pages with the arrows, arrow keys or a swipe. Switch between printed type and handwriting. Full screen. Phone layout shows one page at a time.

---

## Built with

- **Vanilla JavaScript, HTML and CSS** in a single file with no framework, no build step and no backend
- **Wikipedia API** for the entry, matches, definitions and Simple English summary
- **Wikimedia Commons API** for plates and extra pictures
- **Europe PMC REST API** for paper counts and links
- **Google Fonts** (IM Fell English, Patrick Hand) for the type

The paper, leather and ink are all drawn in CSS and generated SVG noise. There are no image files for the book itself. Pages are split by measuring real text in a hidden, page-sized box, so they are re-measured and re-set when the window changes size or you switch to handwriting.

---

## Running it

Everything is in `index.html`. Open it in a browser with an internet connection, because it fetches from the three sources live.

To put it online on GitHub Pages: push to `main`, then go to **Settings → Pages** and set the source to the `main` branch, `/ (root)`. It goes live at `https://YOUR-USERNAME.github.io/corpus/`.

If the sources cannot be reached (offline, or a browser that blocks outside requests), the book says so and opens a small sample instead of inventing content.

---

## On honesty

Corpus is built around not making things up.

- **No AI writes any page.** Code collects text from Wikipedia and Europe PMC and sets it in the book. Search ordering is done by those sites' own search engines.
- **It follows the entry it found,** which is not always what you meant. That is why the matched entry and alternatives are shown on the first page.
- **Pictures are labelled.** Pictures from the entry carry a link to their file page. Plates from *Gray's Anatomy* are old engravings showing the anatomy of their day, not necessarily the exact thing you searched, and later work has corrected parts of it. Pictures marked "related" or "matched by search" were not placed by the entry's editors and have not been checked by hand.
- **Paper counts are a pointer, not a verdict.** A low number can mean a subject is little studied, or that researchers use another name for it.
- **This is a teaching book, not medical advice or a diagnosis.**

---

## Sources and licences

- Wikipedia text and Simple English Wikipedia: CC BY-SA 4.0. Authors are listed in each page's history
- Pictures: Wikimedia Commons, free licences shown on each file's page
- *Gray's Anatomy* plates: public domain
- Papers and counts: Europe PMC

---

## What is next

- An **advanced** mode with denser, more technical sources
- Plants and oceans, using the same engine
- More ways to find thinly researched subjects
- Better handling of messy Wikipedia articles

---

## Notes

Built as a learning project, by directing AI tools. The goal was a book that feels old and handmade but runs on real, checkable sources, and that is honest about what it does not know.

If a page looks wrong or a picture does not fit, open an issue with the topic you searched.
