# Steady Start VA

A small static website for pregnant and new parents in Virginia who have Medicaid or FAMIS.
Plain HTML and CSS. No JavaScript, no trackers, no cookies, no forms.

## Files

| File | Page |
| --- | --- |
| `index.html` | Home |
| `food.html` | Get help buying food (WIC) |
| `rides.html` | Get a ride to a medical visit |
| `coverage.html` | What else does my Medicaid cover? |
| `how-long.html` | How long does my coverage last? |
| `baby.html` | How do I report my baby's birth? |
| `family.html` | Other help for your family |
| `apply.html` | Apply for health coverage |
| `talk.html` | Talk to someone |
| `urgent.html` | Urgent help |
| `about.html` | About (linked in the footer) |
| `404.html` | "We couldn't find that page" |
| `favicon.svg`, `favicon.png` | The leaf logo shown in browser tabs |
| `og-image.png` | The picture shown when a link to the site is shared |
| `styles.css` | The one stylesheet every page shares |
| `fonts/` | Font files, served from this folder (with their licenses) |

To look at the site, open `index.html` in a browser. To publish it, upload the whole folder as it is.

## How to update a phone number

Each phone number is written **twice** in a link: once for the phone to dial, and once for people to read.

```html
<a class="phone" href="tel:18552428282"><span>Call</span>1-855-242-8282</a>
```

- `tel:18552428282` is what the phone dials: digits only, no dashes.
- `1-855-242-8282` is what people see.

Steps:

1. Search **all** the `.html` files for the old number in both forms (for example `18552428282` and `1-855-242-8282`). The same number can be on several pages.
2. Change both forms everywhere you find them. Make sure the two forms match.
3. On each page you changed, confirm the number against the official source linked at the bottom of that page, then update the "Last checked" date there.
4. Open the page on a phone and tap the number to make sure it dials correctly.

Where each number is used now:

| Number | Who it reaches | Pages |
| --- | --- | --- |
| 1-855-242-8282 | Cover Virginia | `coverage.html`, `how-long.html`, `baby.html`, `apply.html`, `talk.html` |
| 1-888-221-1590 | Cover Virginia TTY | `talk.html` |
| 1-800-643-2273 | Cardinal Care Managed Care Helpline | `rides.html`, `coverage.html` |
| 1-833-522-5582 | SNAP application line | `food.html` |
| 1-888-912-3456 | Medicaid dental program (marked VERIFY in the HTML: confirm before launch) | `coverage.html` |
| 1-855-635-4370 | TANF application line | `family.html` |
| 1-833-852-6262 | National Maternal Mental Health Hotline | `urgent.html` |
| 988, 911 | Crisis line, emergency | `urgent.html` (911 is also named in the strip at the top of every page) |

## Other edits

- The urgent strip, the "Pilot version" line and the footer are repeated in every `.html` file. If you change one, change it in every `.html` file.
- Colors, fonts and spacing are all in `styles.css`. The color values are listed at the top of that file. The site is always light; there is no dark mode.
- Do not add facts, numbers or claims without an official source link and a "Last checked" date.
- Share preview: every page points to `og-image.png` with a short address. Many apps only show the picture if the address is complete, so once the site has a web address, change `content="og-image.png"` (two places per page) to the full address, for example `https://your-site.example/og-image.png`.
- `404.html` uses short addresses for the stylesheet and links, so it only looks right when the site sits at the top level of its web address.
