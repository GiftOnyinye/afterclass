# AFTERCLASS.

> A corner of the internet that isn't trying to sell you anything.

A private, local-first web app for quizzes, moodboards, obsessions, diary entries, fictional group chats, and letters to real friends. No account. No server. No algorithm. Everything you make lives in your browser and nowhere else.

---

## What this is

AFTERCLASS is a fictional-feeling but fully functional digital scrapbook — part teen magazine, part Pinterest board, part diary, part group-chat simulator. It's built as a single HTML file with vanilla JavaScript and no build step, no framework, no dependencies at runtime.

It is deliberately art-directed. The layout is an editorial collage, not a card grid. The type is a three-part system (serif headlines, sans body, handwritten marginalia). The palette is warm paper and pastel ink, not SaaS purple. Every string was written for its context — no lorem ipsum, no placeholder metrics, no fake analytics.

---

## The rooms

| Route | What it is |
|-------|------------|
| `#/` | **The Lobby** — an editorial homepage with a daily question, a featured quiz, a moodboard preview, and links into every room. |
| `#/quizzes` | **Quiz Library** — five original quizzes with real scoring logic and five distinct results each. Save any result as a designed PNG card. |
| `#/obsessions` | **Obsession Files** — a curated archive of music, films, TV, books, characters, and fandoms. Add your own, with notes and ratings. |
| `#/lore` | **Lore Archive** — a private diary. Entries save to your browser only. Export and import as JSON. |
| `#/chat` | **Fictional Group Chat** — three written scenarios with distinct character voices. Regenerate for alternate lines. Clearly fictional. |
| `#/friends` | **Friends Desk** — draft messages to real people. Copy them, or open them in SMS, email, or WhatsApp. Paste their replies back to keep the thread coherent locally. |
| `#/moodboard` | **Moodboard Studio** — a collage canvas with text, quotes, colour swatches, hand-drawn stickers, and images. Drag, nudge with arrow keys, undo/redo, export as PNG. |

---

## Privacy, in plain language

Everything you make lives in this browser's `localStorage`. There is no backend, no account, no analytics, no tracking, no remote calls beyond loading the Google Fonts stylesheet. If you clear your site data or switch browsers, your archive is gone — that's the trade-off for having nothing to log into and nobody to trust but yourself.

The **Friends Desk** does not send messages. It uses `sms:`, `mailto:`, and `wa.me` links so you can hand the text off to your real messaging app, where you press send yourself. Nothing about your friends is stored beyond the name and message text you type.

You can **export** everything as JSON at any time from the settings panel (the icon in the masthead). You can **clear** everything from the same panel.

---

## Running it

Open `index.html` in any modern browser. That's it.

If you want a local server (recommended, because `localStorage` behaves more consistently and image exports work cleanly over `http://` rather than `file://`):

```bash
# Python 3
python -m http.server 8000

# or Node
npx serve .
