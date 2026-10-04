# HTML & CSS Assignments Collection

A collection of beginner-to-intermediate HTML and CSS assignments, all opened from one hub page. The hub (`index.html`) shows a list of "Assignment" buttons on the left and loads each assignment in an `<iframe>` on the right.

## Project Structure

The hub links to files inside a folder named `sub file`, so keep this layout:

```
.
├── index.html            # Hub page with the iframe viewer
├── README.md
└── sub file/
    ├── style.css         # Shared styles for the navigation pages
    ├── images/           # Images used by the assignments (see below)
    ├── background.html
    ├── newspage.html
    ├── flexbox.html
    ├── dgallery.html
    ├── card.html
    ├── home.html
    ├── aboutus.html
    ├── gallery.html
    ├── achivment.html
    ├── contactus.html
    ├── iframe.html
    ├── table.html
    ├── box Ploting.html
    ├── sign up.html
    ├── login1.html
    └── animation.html
```

## Assignment Index

| # | File | Topic | What it demonstrates |
|---|------|-------|----------------------|
| 1 | `background.html` | Background image | Full-screen `background-image` with `background-size: cover` and a semi-transparent text overlay (`rgba`) |
| 2 | `newspage.html` | Newspaper layout | CSS multi-column text (`column-count`, `column-gap`, `column-rule`), `<marquee>`, justified text |
| 3 | `flexbox.html` | Flexbox layout | Header / body / footer layout with nested flex containers |
| 4 | `dgallery.html` | Dynamic gallery | Four-column image gallery with flexbox, each column in a different image order |
| 5 | `card.html` | Profile card UI | Card layout with border radius, shadows, a circular profile image, Font Awesome social icons and buttons |
| 6 | `home.html` | Navigation bar | Flex-based nav bar linking to the other pages, using `style.css` |
| 7 | `iframe.html` | Iframe viewer | An earlier version of the hub page that loads pages in an iframe |
| 8 | `table.html` | Table | Styled table with `colspan`, a header row, hover highlight and a total row |
| 9 | `box Ploting.html` | CSS box model | Visualizes content, padding, border and margin with labeled, colored layers |
| 10 | `sign up.html` | Sign-up form | Form with text, date, radio, tel, email, password and checkbox inputs |
| 11 | `animation.html` | CSS animations | `@keyframes` for color, move, rotate, pulse, fade, a loader, a square-path animation and a staggered "Google" dots animation |

### Supporting pages

| File | Purpose |
|------|---------|
| `login1.html` | Log-in form. Linked from the sign-up page, and links back to it |
| `aboutus.html`, `gallery.html`, `achivment.html`, `contactus.html` | Other pages of the navigation bar from Assignment 6. Same layout as `home.html` with a different gradient background |
| `style.css` | Shared stylesheet for the five navigation pages (transparent rounded nav box, flex list, hover zoom on links) |

## How the Pages Connect

- `index.html` opens each assignment in the iframe named `sahil`.
- The five navigation pages (`home`, `aboutus`, `gallery`, `achivment`, `contactus`) link to one another.
- `sign up.html` and `login1.html` link to each other.

## Getting Started

No installation or build step is needed.

1. Place the files as shown in **Project Structure**.
2. Open `index.html` in a modern web browser.
3. Click an **Assignment** button to load it on the right.

You can also open any assignment on its own by opening its file directly.

## Requirements
- **Internet connection:** `card.html` loads Font Awesome icons from a CDN (`cdnjs.cloudflare.com`).

## Known Issues

- **Missing links in `iframe.html`:** it points to files such as `sub file/1.html`, `2.html` and `1.1.html` that are not part of this set.
- **File names:** several names contain spaces or capital letters (`box Ploting.html`, `sign up.html`). The hub links to `box Ploting.html` while the file may be saved in lowercase. This works on Windows but can break on case-sensitive servers (Linux hosting, GitHub Pages).
- **Typos:** "Achivements" / `achivment.html`, "Ploting", "Persented", and the label "Context" in the box-model page (should be "Content").
- **`animation.html`:** the `.g1` rule is declared twice (red is overridden by orange), and the "Square Path Animation" and "Google Animation" titles use hard-coded pixel positions, so they may not line up on every screen size.
- **`card.html`:** the profile circle is positioned with percentages (`top` / `right`), so it can drift on different screen sizes. The selector `.bottom>h1,h2,h3` only applies `.bottom>` to the `h1`.
- **`table.html`:** the Television amount is `1460000`, but 48 x 30000 = `1440000`. The total of `9850000` only works with `1440000`.
- **Deprecated HTML:** `<marquee>`, `align="center"` and `border="1px"` are outdated and are better done in CSS.
- **Forms:** the sign-up and log-in forms have no JavaScript or backend, so they do not submit or validate anything.
- **Layout:** most pages use fixed percentages and `100vh`, so they are designed for desktop screens and are not fully responsive.
- All pages share the default title "Document".

## Possible Improvements

- Give each page a meaningful `<title>`
- Rename files without spaces or capitals (e.g., `box-model.html`, `sign-up.html`) and update the links
- Move the repeated CSS into shared stylesheets
- Replace deprecated tags with CSS
- Add media queries for mobile screens
- Add JavaScript validation to the forms
- Add a default page for the iframe so it isn't blank on first load

## Tech Stack

- HTML5
- CSS3 (flexbox, multi-column layout, gradients, `@keyframes` animations, transitions)
- Font Awesome (via CDN, `card.html` only)
