# How to Update the Room Parent Site

You don't need me (or any coding tools) for day-to-day posts — you can edit the site straight from your GitHub repo in the browser. Here's the process, and the exact copy-paste snippets for each section.

## The basic steps (same every time)

1. Go to your repo: `github.com/svitlanatselishchev-sudo/room-parent`
2. Click **`index.html`** to open the file.
3. Click the **pencil icon** (top right of the file, "Edit this file") to switch into edit mode.
4. Press **Ctrl+F** (or Cmd+F on Mac) and search for the marker for the section you want (see below) — e.g. search `COPY START`.
5. Copy the template block, paste it in the spot the comment tells you to, then edit the text.
6. Scroll to the bottom, click **Commit changes...**, then **Commit changes** again to confirm.
7. Give it about a minute — your change goes live automatically at your site's URL.

You're only ever editing plain text inside the templates below — you don't need to touch anything else in the file.

---

## Post a Room Parent Update

Search for: `HOW TO POST A NEW UPDATE`

Copy this block, paste it where the comment says (newest on top), and edit the date and text:

```html
<div class="update-item">
  <div class="update-date">SEP 5</div>
  <div class="update-text">Picture day moved to September 12 — details in the group chat.</div>
</div>
```

## Post a School / PTA Event

Search for: `HOW TO ADD A NEW EVENT`

Copy this block and edit the 3-letter month, title, and date/time. Leave the icon exactly as-is — it's generic and works for any event:

```html
<div class="event-item">
  <div class="event-month">OCT</div>
  <div class="event-info"><strong><svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 8v4l3 2"/></svg> Event Title Here</strong><span>October 10 · 6:00 PM</span></div>
</div>
```

## Add a Birthday Shoutout

Search for: `Add more birthdays as additional candles`

Copy the button block right below that comment and edit the name and date:

```html
<button class="candle-note" data-name="Name" data-date="Month Day" aria-label="Name's birthday — Month Day">
  <svg viewBox="0 0 20 56" aria-hidden="true">
    <line x1="10" y1="14" x2="10" y2="18" stroke="#3a2a1a" stroke-width="1.5"/>
    <path class="candle-flame" d="M10 4c3 5 3 9 0 13c-3-4-3-8 0-13Z" fill="#f6b53d" stroke="#c8841f" stroke-width="1.5" stroke-linejoin="round"/>
    <rect class="candle-stick" x="6" y="18" width="8" height="34" rx="2.5" stroke="#6b4423" stroke-width="2"/>
    <path d="M6 26 L14 26 M6 34 L14 34 M6 42 L14 42" stroke="#ffffff" stroke-width="1.3" opacity=".5"/>
  </svg>
</button>
```

## Add a Teacher Appreciation Note

Search for: `Add more approved notes as additional apples`

Copy the button block right below that comment and edit the message and family name:

```html
<button class="apple-note" data-message="Full note text here." data-name="The Smith Family" aria-label="Read thank-you note from The Smith Family">
  <svg viewBox="0 0 64 64" aria-hidden="true">
    <path class="apple-body" d="M32 20 C18 12 6 24 6 38 C6 52 17 60 32 60 C47 60 58 52 58 38 C58 24 46 12 32 20 Z" stroke="#6b4423" stroke-width="3"/>
    <ellipse cx="21" cy="32" rx="6" ry="9" fill="#fff" opacity=".45" transform="rotate(-25 21 32)"/>
    <path d="M32 18 C38 6 52 6 54 14 C50 22 38 22 32 18 Z" fill="#7ea24a" stroke="#4f6b34" stroke-width="2"/>
    <path d="M32 18 C30 12 32 7 35 3" stroke="#6b4423" stroke-width="3.2" fill="none" stroke-linecap="round"/>
  </svg>
</button>
```

---

## A few tips

- **Don't delete the comment lines** (the `<!-- ... -->` bits) — they're your landmarks for next time and don't show up on the live site.
- **Removing a birthday or a note?** Just delete its whole `<button>...</button>` block.
- **Made a mistake?** Every commit is saved in GitHub's history (the "History" or "commits" link at the top of the file) — you can always see what changed or revert.
- **Anything bigger** — new sections, design changes, wishlist updates — just come back and ask me, and I'll send you an updated file.
