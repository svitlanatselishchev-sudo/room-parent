# How to Update the Room Parent Site

## ⭐ The easy way: post updates & events from a Google Sheet — no code

For **Room Parent Updates**, **School & PTA Events**, all the **links** the site uses (GiftCrowd, Remind, and all three Google Forms), and your **Amazon wishlist link(s)**, you don't need to touch `index.html` at all anymore. The site reads that content from a Google Sheet called **"Room Parent Hub – Content"**, sitting in your Drive. The sheet has **4 tabs** — one per content type — so each kind of content has its own simple table instead of one long mixed list:

| Tab | What it controls |
|---|---|
| **Updates** | The "Room Parent Updates" feed |
| **Events** | The "School & PTA Events" card |
| **Links** | GiftCrowd, Remind, the 3 Google Forms, birthday text & goal |
| **Wishlists** | Every Amazon (or other) wishlist button on the site |

**One-time setup (do this once):**

1. Open the sheet: [Room Parent Hub – Content](https://docs.google.com/spreadsheets/d/1YfOHVxvvDtOB9aTRlZYgyoJRh0chV6stVzZtObiHC3E/edit)
2. Click **Share** (top right) → under "General access," change it from "Restricted" to **"Anyone with the link"**, and make sure the role is set to **Viewer**. This just lets the site *read* the sheet — nobody can edit it unless you send them the edit link directly. **This step still needs to be done** — right now the sheet is set to "Restricted," so the site can't read it yet and is quietly showing its built-in fallback content instead. Nothing looks broken to visitors either way, but flip this switch when you get a chance so your real updates start showing.
3. That's it. From now on, editing a cell in any tab updates the live site within a minute or two — just don't rename the tabs themselves (Updates / Events / Links / Wishlists), since the site looks for those exact names.

### Tab 1 — Updates (columns: `Date`, `Text`, `Tag`)

Add a new row under the header for each update, **newest on top**. `Date` = a short date like `SEP 5` (type it as `'SEP 5` with a leading apostrophe so Sheets treats it as text, not a calendar date). `Text` = the update itself.

`Tag` is optional and controls a small colored label above the update text, so parents can tell at a glance where something came from. Type exactly one of these three words (not case-sensitive):

| Type in `Tag` | Shows as | Color |
|---|---|---|
| `School` | 🏫 School | blue |
| `PTA` | 🤝 PTA | purple |
| `Class` | 🎒 Class | green |
| *(leave blank)* | no label | — |

Leave it blank for your own everyday updates if you don't want a label at all, use `Class` if you'd like your own updates explicitly marked, and use `School` or `PTA` when you're forwarding something that came from the school or the PTA. Anything else typed into `Tag` still works — it just falls back to a plain gold "From [whatever you typed]" label instead of one of the three colors above.

### Tab 2 — Events (columns: `Month`, `Title`, `DateTime`)

Add a row for each School/PTA event: `Month` = a 3-letter month like `OCT`, `Title` = the event name, `DateTime` = text like `October 10 · 6:00 PM`.

### Tab 3 — Links (columns: `Key`, `Value`)

Find the row for the link you want to change and edit `Value` only — covers `GiftCrowdURL`, `RemindURL`, `VolunteerFormURL`, `ThankYouFormURL`, `SuggestionFormURL`, `BirthdayText`, and `BirthdayGoal`. Don't rename anything in the `Key` column or add new keys — the site only looks for those exact names.

### Tab 4 — Wishlists (columns: `Label`, `URL`) — add or remove links freely

This is what you asked about: **the site automatically adjusts to however many wishlist links you have — no code, no layout to fix.** Each row is one button. To add a second wishlist (say, a Target list alongside Amazon), just add a new row with a `Label` (the button text, e.g. `Target Wishlist`) and the `URL`. It appears as a new stacked button inside the existing "Amazon Class Wishlist" card within a minute or two — the card just gets a little taller, the rest of the page layout doesn't move. To remove one, delete its row; the button disappears the same way. To rename a button, just edit its `Label` cell. You can have as many rows here as you want (1, 2, 5 — doesn't matter).

The sheet has its own instructions written into the bottom of the original tab too, in case you need a reminder later. Class Dates (field trips) and F.A.S.T. testing windows aren't on the sheet — those change rarely, so they still get a quick code edit the old way (see below), or just ask me.

---

## Google Forms (one-time setup for each)

I've replaced every Cheddarup form on the site with a Google Form — same free, no-code concept as the content sheet above. Each one is already created and already linked into the site; you just need to add the questions once, the same way for all three (~3 minutes each).

### 1. Volunteer Interest Form

Open: [Volunteer Interest – Room Parent Hub](https://docs.google.com/forms/d/1sNEEtZvy5_DmnPTMSQs9BYQjqXNPIU3K1_HNcxA0rnE/edit)

Keeping this focused on **in-class needs** specifically (not field trips or school-wide PTA stuff — those have their own channels already). Suggested form description text: *"Ways to help directly in Ms. Fernandes' classroom this year — no experience or time commitment required."*

| # | Question | Type | Required? |
|---|---|---|---|
| 1 | First & Last Name | Short answer | Yes |
| 2 | Email | Short answer | Yes |
| 3 | Child's Name | Short answer | No |
| 4 | Are you willing to help in the classroom this year? | Multiple choice: Yes / No / Maybe | Yes |
| 5 | Are you already an approved Martin County volunteer? | Multiple choice: Yes / No / Not sure | Yes |
| 6 | If yes, what level? | Multiple choice: Level 1 / Level 2 / Not sure / N/A | No |
| 7 | What in-class help are you interested in? | Checkboxes: Classroom parties · Classroom stations/centers · Classroom supplies & wishlist · Reading with kids / listening to them read · Event planning & ideas for the class · Teacher appreciation · Other | No |
| 8 | Anything else you'd like to share? | Paragraph | No |

I added **Email** even though you didn't ask for it — without it, there's no way to follow up with people who say "Yes" or "Maybe" to send them the volunteer application. Worth keeping. I dropped "Field trip chaperone" from question 7 since that's off-site, not an in-class need — let me know if you'd rather I add it back as its own category.

(Optional polish: in Forms, you can make Question 6 only appear when Question 5 = "Yes" using **Sections** — but it's fine to skip this and just leave "N/A" as an option.)

### 2. Thank-You Notes Form

Open: [Thank-You Notes – Room Parent Hub](https://docs.google.com/forms/d/1POhbOmc6o2W5UORGYN9hMLgdAB5-eBaXC7qn2ptlKrA/edit)

This replaces the old Cheddarup "Send Thank-You" link. Suggested description: *"Leave Ms. Fernandes a quick thank-you — share your name or stay anonymous, whatever you're comfortable with. Notes are reviewed before they're added to the wall."*

| # | Question | Type | Required? |
|---|---|---|---|
| 1 | Your name (or family name) — leave blank to stay anonymous | Short answer | No |
| 2 | Your message for Ms. Fernandes | Paragraph | Yes |

Responses land in the form's Responses tab. To publish an approved one to the site, it's the same manual step as before — see **Add a Teacher Appreciation Note** below, just copy the name and message from the response instead of from a Cheddarup email.

### 3. Suggestions & Ideas Form

Open: [Suggestions & Ideas – Room Parent Hub](https://docs.google.com/forms/d/17jNdu35EcwHxdkcbBHpM_4EDjLvda0ZL0s357rHZCV8/edit)

This replaces the old Cheddarup "Share a Suggestion" link (used on both the site and the welcome email). Suggested description: *"A party theme, event, or way to make this year great — I'd love to hear it."*

| # | Question | Type | Required? |
|---|---|---|---|
| 1 | Your name | Short answer | No |
| 2 | Your idea or suggestion | Paragraph | Yes |

**For all three forms:** once you're done adding questions, there's nothing else to do — the links are already live on the site (and, for Suggestions, in the welcome email too). Responses land in each form's own **Responses** tab (click the green Sheets icon there if you'd rather read them as a spreadsheet) — none of that is shown anywhere on the public site.

---

## The old way (still works, for everything else)

You don't need me (or any coding tools) for the sections below — you can edit the site straight from your GitHub repo in the browser. Here's the process, and the exact copy-paste snippets for each section.

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

*(You probably want the Google Sheet method above instead — this is the manual fallback.)*

Search for: `HOW TO POST A NEW UPDATE`

There are four template blocks there — plain (no label), and one each for **School** (blue), **PTA** (purple), and **Class** (green). Use whichever fits: the plain one for an update with no label, "Class" if you want your own update explicitly marked, or "School"/"PTA" for anything you're forwarding along — like an email from the room parent coordinator (drama club sign-ups, spirit wear, etc.) — the colored tag makes clear where it came from at a glance. This is the place for exactly that kind of forwarded announcement, until there's a full parent email list.

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

*(You probably want the Google Sheet method above instead — this is the manual fallback.)*

Search for: `HOW TO ADD A NEW EVENT`

Copy this block and edit the 3-letter month, title, and date/time. Leave the icon exactly as-is — it's generic and works for any event. Paste it into the **"School & PTA Events"** card (not "Class Dates" or "F.A.S.T. Assessments") so it picks up the right gold styling automatically. The Dates section now has three cards side by side — Class Dates (field trips), F.A.S.T. Assessments (testing windows), and School & PTA Events — each with its own color so they're easy to tell apart at a glance. The assessment dates are set by the district each year; just edit the month/date text directly inside that card's `event-item` blocks when new ones are announced.

```html
<div class="event-item">
  <div class="event-month">OCT</div>
  <div class="event-info"><strong><svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 8v4l3 2"/></svg> Event Title Here</strong><span>October 10 · 6:00 PM</span></div>
</div>
```

## Add a Teacher Appreciation Note

Notes now come in through the **Thank-You Notes Form** (see above) instead of Cheddarup. Once you've reviewed one in the form's Responses tab and want to publish it to the tree, search for: `Add more approved notes as additional apples`

Copy the button block right below that comment and edit the message and family name (pulled from the form response):

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

This lives as a featured card at the bottom of the Teacher Appreciation section (search for `Ms. Fernandes' Birthday` to find it).

The description text and the goal amount are both sheet-driven now — edit the `BirthdayText` and `BirthdayGoal` rows in the Google Sheet (see the top of this doc) and they'll update on the site automatically. The GiftCrowd link on this card is also sheet-driven — it's the same `GiftCrowdURL` row used elsewhere, so updating it there updates both spots at once.

If you ever want to change the badge text ("🎉 Coming Up"), the heading ("Ms. Fernandes' Birthday"), or remove the card entirely once the occasion has passed, that's still a direct edit here in `index.html` — delete the whole `celebrate-featured-wrap` block to remove it.

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

- 📅 New event just went up on the class hub: [Event name], [date]. https://svitlanatselishchev-sudo.github.io/room-parent/#dates
- 🍎 Someone left Ms. Fernandes a sweet note on the Appreciation Wall — go take a look: https://svitlanatselishchev-sudo.github.io/room-parent/#appreciation
- 📣 Quick update posted on the class hub: https://svitlanatselishchev-sudo.github.io/room-parent/#updates

Takes 10 extra seconds after you commit a change, and it's the same "Most Important" channel you're already asking families to join.

## A few tips

- **Don't delete the comment lines** (the `<!-- ... -->` bits) — they're your landmarks for next time and don't show up on the live site.
- **Removing a birthday or a note?** Just delete its whole `<button>...</button>` block.
- **Made a mistake?** Every commit is saved in GitHub's history (the "History" or "commits" link at the top of the file) — you can always see what changed or revert.
- **Anything bigger** — new sections, design changes, wishlist updates — just come back and ask me, and I'll send you an updated file.
