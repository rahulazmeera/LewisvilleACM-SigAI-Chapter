# ACM SIGAI &mdash; Lewisville Chapter Website

A single-page static website for the Lewisville ACM SIGAI (Special Interest Group on
Artificial Intelligence) Chapter. No build step, no dependencies &mdash; just HTML, CSS,
and a little vanilla JavaScript.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | All page content and structure |
| `styles.css` | Styling and responsive layout |
| `script.js` | Mobile nav toggle and footer year |
| `assets/logo.svg` | Chapter logo — horizontal lockup (mark + wordmark) |
| `assets/logo-mark.svg` | Chapter logo — mark only (used in the nav and as the favicon) |
| `assets/acm-logo.svg` | **Placeholder** for the official ACM logo — see below |

## Logo & branding

The chapter mark is a Lone Star wired as a small neural network — Texas identity
(navy, wheat-gold star) plus an AI motif (blue traces, orange nodes). Colors:

- Navy `#0e2a4e` · Sunset orange `#d0561f` · Wheat gold `#e0a83d` · Tech blue `#1f6feb`

### The ACM logo (do this before launch)

`assets/acm-logo.svg` is only a dashed placeholder. As a recognized ACM chapter you
may use the ACM name and logo per ACM's guidelines — **use the official artwork
unmodified**, don't redraw it.

1. Download the official logo: <https://www.acm.org/about-acm/acm-branding>
   (chapter resources: <https://www.acm.org/chapters>).
2. Replace `assets/acm-logo.svg` with the official file (keep the name, or update
   the `<img src>` in the footer of `index.html`).

The footer already carries the trademark acknowledgment for ACM / SIGAI / the ACM logo.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy on GitHub Pages

1. Push this repo to GitHub.
2. **Settings &rarr; Pages &rarr; Build and deployment**.
3. Source: **Deploy from a branch**. Branch: `main`, folder: `/ (root)`. Save.
4. The site publishes at `https://<user-or-org>.github.io/<repo>/` within a minute or two.

To use a custom domain, add a `CNAME` file containing the domain and configure DNS.

## Before you go live &mdash; things to fill in

Search the HTML for `TODO` comments. At minimum, update:

- **Officers** (`#officers`): real names, roles, short bios, photos/initials, and contact links.
- **Events** (`#events`): real event titles, dates (set `event-month` / `event-day`), and locations.
- **Join links** (`#join` and nav): the interest-form URL (Google Form) and the Discord/GroupMe invite.
- **Contact email**: currently `intaiacmsociety@gmail.com` (in `#join` and the footer).
- **Chapter status / year** in the hero if needed.

### Adding an officer

Copy one `<article class="officer">` block in `index.html` and edit the name, `officer-role`,
`officer-bio`, the two-letter `officer-avatar` initials, and the `officer-link` href.

### Adding an event

Copy one `<li class="event">` block. Set `event-month` (e.g. `OCT`) and `event-day` (e.g. `14`),
then the title, description, and location.

## License

Content &copy; the chapter. Reuse the template freely.
