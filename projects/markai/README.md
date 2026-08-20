# MarkAI

[![GitHub](https://img.shields.io/badge/GitHub-MarkAI-blue?style=flat&logo=github)](https://github.com/follen99/MarkAI)
[![PyPI](https://img.shields.io/pypi/v/markai?color=4f5bd5&label=PyPI&logo=pypi&logoColor=white&style=flat)](https://pypi.org/project/markai/)

**Reviewing a document is easy. Getting the review applied is the part that wastes your afternoon.**
Word comments live inside the `.docx`. PDF annotations live inside the PDF. Every annotation tool
keeps your review trapped in its own format, so applying forty notes back into the source means
retyping each one by hand — slower than just fixing the document yourself.

MarkAI is the missing export step. Annotate a Markdown, PDF or DOCX file the way you always would —
click a word, select a phrase, type a note — and it writes the whole review out as compact JSON built
for an AI coding agent to consume: what to change, exactly where (`Chapter 3 / 3.3 Chunking and
pre-processing`), and the quoted text to find it by. Point an agent at the file, let it apply the
fixes, and it flips each note to `done` in a companion status file MarkAI reads back — the notes
panel empties itself as the work lands.

**Tech Stack:** Python | Flask | SQLite | pdf.js | Vanilla JS/CSS (no build step, no frontend framework)

## Highlights

- Markdown, PDF and DOCX in one reader, with character-precise note anchoring in all three.
- A real PDF reader experience: native text selection via pdf.js's own text layer, a chapter outline
  from the PDF's bookmarks, and zoom that stays instant at any page count.
- Two-way sync with a linked source folder: notes go out as JSON, an agent's status updates come back
  in automatically.
- Fully local. Single Flask process, one SQLite file, pdf.js bundled (no CDN) — nothing about your
  documents ever leaves the machine.

## Try it

No clone, no setup:

```bash
uvx markai
```

Opens at `http://localhost:8765` with a ready-to-use account shown right on the login screen.

## Source

Full architecture notes, the export format, and the reasoning behind every non-obvious decision live
in [`CLAUDE.md`](https://github.com/follen99/MarkAI/blob/master/CLAUDE.md) on the repo.
