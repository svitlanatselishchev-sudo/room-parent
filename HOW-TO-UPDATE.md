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

There are two template blocks there. Use the plain one for your own class updates. Use the **"From School/PTA"** one for anything you're forwarding along — like an email from the room parent coordinator (drama club sign-ups, spirit wear, etc.) — the little gold tag makes clear it's not something you wrote yourself. This is the place for exactly that kind of forwarded announcement, until there's a full parent email list.

Copy whichever block fits, paste it where the comment says (newest on top), and edit the date and text:

```html
<div class="update-item">
  <div class="update-date">SEP 5</div>
  <div class="update-text">Picture day moved to September 12 — details in the group chat.</div>
</div>
```

```html
<div class="update-item">
  <div class="update-date">SEP 5</div>
  <div class="update-text"><span class="update-tag">From School/PTA</span><br>Drama Club sign-ups are open through September 12 — see the flyer in the group chat.</div>
</div>
```

## Post a School / PTA Event

Search for: `HOW TO ADD A NEW EVENT`

Copy this block and edit the 3-letter month, title, and date/time. Leave the icon exactly as-is — it's generic and works for any event. Paste it into the **"School & PTA Events"** card (not "Class Dates" or "F.A.S.T. Assessments") so it picks up the right gold styling automatically. The Dates section now has three cards side by side — Class Dates (field trips), F.A.S.T. Assessments (testing windows), and School & PTA Events — each with its own color so they're easy to tell apart at a glance. The assessment dates are set by the district each year; just edit the month/date text directly inside that card's `event-item` blocks when new ones are announced.

```html
<div class="event-item">
  <div class="event-month">OCT</div>
  <div class="event-info"><strong><svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 8v4l3 2"/></svg> Event Title Here</strong><span>October 10 · 6:00 PM</span></div>
</div>
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

## Update Ms. Fernandes' Birthday note

This lives as a featured card at the top of the Teacher Appreciation section (search for `Ms. Fernandes' Birthday` to find it). It's plain text, not a repeating template — just edit the date or wording directly, or delete the whole `celebrate-featured-wrap` block once the occasion has passed.

The card also has a small goal line (search for `celebrate-goal`). To adjust the dollar amount, just edit the number inside the `<strong>` tag. To change the GiftCrowd collection link, edit the `href` on the `<a class="btn btn-celebrate">` tag — each occasion (birthday, event, supply drive, etc.) gets its own GiftCrowd collection link, and funds go straight to the teacher, never through your own account.

---

## Seasonal look (automatic — nothing to do)

The site's colors and little background decorations now shift on their own through the year, based on the visitor's own device date. You don't need to change anything for this to work — no toggle, no setting, nothing to remember.

- **Colors:** the gold/coral/purple palette warms up for fall (Sep–Nov), cools down for winter (Dec–Feb), and eases back for spring (Mar–May) and summer (Jun–Aug). The main plum and text colors stay the same year-round so everything stays easy to read.
- **Background icons:** a small, subtle icon appears in each section's background, changing by month — fall leaves in September, pumpkins & ghosts in October, turkeys in November, snowflakes in December, little trees in January, hearts in February, a shamrock in March, a tulip in April, a butterfly in May, a sun in June, fireworks in July, and a sunflower in August.

If you ever want to change which icon shows in a given month, search for `monthIcons` near the bottom of `index.html` — it's a simple list mapping month numbers (1–12) to icon names. The available icon names are: `leaf`, `pumpkin`, `ghost`, `turkey`, `snowflake`, `tree`, `heart`, `shamrock`, `tulip`, `butterfly`, `sun`, `firework`, `sunflower`. This is the one part of the seasonal system that does need a code edit (not a simple copy-paste template), so come back and ask me if you'd like it adjusted.

---

## Let people know you posted something

The site itself can't send notifications — it's a static page, not an app with a database behind it. The fastest, most reliable way for families to actually see a new post is to drop one quick line in the class group chat (Remind) right after you commit the change. Remind pushes straight to everyone's phone, which beats email or a passive site check every time.

A few ready-to-use lines, so it's fast:

- 📅 New event just went up on the class hub: [Event name], [date]. bit.ly/room-parent#dates
- 🍎 Someone left Ms. Fernandes a sweet note on the Appreciation Wall — go take a look: bit.ly/room-parent#appreciation
- 📣 Quick update posted on the class hub: bit.ly/room-parent#updates

Takes 10 extra seconds after you commit a change, and it's the same "Most Important" channel you're already asking families to join.

## A few tips

- **Don't delete the comment lines** (the `<!-- ... -->` bits) — they're your landmarks for next time and don't show up on the live site.
- **Removing a birthday or a note?** Just delete its whole `<button>...</button>` block.
- **Made a mistake?** Every commit is saved in GitHub's history (the "History" or "commits" link at the top of the file) — you can always see what changed or revert.
- **Anything bigger** — new sections, design changes, wishlist updates — just come back and ask me, and I'll send you an updated file.
