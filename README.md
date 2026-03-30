# 語彙練習 — Vocab Writing Practice

A minimal browser-based writing tool for practicing Japanese using vocabulary you've studied. As you write, words from your vocab list are automatically tracked — moving from **unused** to **used** as you incorporate them into your text.

No server, no dependencies, no install. Just open `index.html` or use it via [GitHub Pages](https://tacoccino.github.io/vocab-writing-practice/).

---

## Features

- **Vocab tag panel** — add words as capsule-shaped tags; unused and used words live in collapsible sections
- **Auto-detection** — as you type in the editor, words are matched against your list in real time
  - Japanese/kana/kanji: substring match (since Japanese doesn't use spaces between words)
  - Romaji/latin: whole-word, case-insensitive match
- **Import from .txt** — load a word list from a plain text file (one word per line, or comma/space separated)
- **Save & load** — export your session (word list + editor content) as a `.json` file; reload it anytime with **↑ load**
- **Autosave** — your session is automatically saved to `localStorage` every second, so a refresh won't lose your work
- **Rich text editor** — bold, italic, underline, lists, alignment
- **Dark mode** — toggle with the ☀︎/☽ button; preference is saved to `localStorage`
- **Status bar** — tracks character count (excluding whitespace), rough word count, and vocab hit ratio

---

## Usage

1. Open `index.html` in any modern browser
2. Add vocab words by typing in the input field and pressing **Enter**, or click **⤓ import .txt** to load a list
3. Start writing in the editor — words will move to the **used** section as you type them
4. Remove individual words with the **✕** on each tag, or wipe everything with **✕ clear all words**
5. Collapse either the unused or used section by clicking its header to save panel space
6. Click **↓ save** to download a `.json` snapshot of your word list and editor content
7. Click **↑ load** to restore a previous session from a `.json` save file
8. Your session is also autosaved to `localStorage` every second — a small "autosaved" indicator flashes in the status bar

---

## Word list .txt format

The importer is flexible — any of these formats work:

```
食べる
飲む
走る
```
```
食べる, 飲む, 走る
```
```
食べる 飲む 走る
```

---

## Why this exists

Vocabulary drilling (Anki, textbooks, etc.) is one thing — but actually *using* words in free writing is a different skill. This tool bridges the gap: load your recent vocab deck, write whatever you want, and see at a glance which words you've managed to use and which ones you're still avoiding.

---

## No build step

This is a single `index.html` file with no dependencies beyond a Google Fonts import. Works offline once the fonts are cached. Can also be hosted as a static site (GitHub Pages, Netlify, etc.).
