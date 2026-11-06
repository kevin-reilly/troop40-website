# Troop 40 · Rockville Centre, NY

The website for Scout Troop 40 of Rockville Centre, New York. The troop was established in 1914 and is sponsored by United Church of RVC.

**Live site:** https://kevin-reilly.github.io/troop40-website/

## What's here

The website is the `docs/` folder. It's plain HTML and CSS, with no build tools or frameworks to install.

| File | Page |
|---|---|
| `docs/index.html` | Home |
| `docs/news.html` | News & Events |
| `docs/contact.html` | Contact |
| `docs/styles.css` | Shared styles for every page |
| `docs/images/` | Troop logo and site icons |

The colors come from the troop logo and are defined once, at the top of `styles.css` (red, pine green, sky blue and ink). Use those variables instead of adding new colors.

## Previewing your changes

Open `docs/index.html` in a web browser. You can also run a small local server from the project folder:

```sh
python3 -m http.server 8000 --directory docs
```

Then visit http://localhost:8000.

## Updating the site

### Header, menu and footer
Every page has its own copy of the header, menu and footer. If you change one, make the same change on all three pages.

In the menu, the link for the page you're on has `aria-current="page"`, which highlights it. On each page, that attribute belongs on that page's own link.

### Google Analytics
Every page loads Google Analytics (ID `G-KSK9N3DKMB`) at the top of its `<head>`. If you add a new page, copy that snippet into it so its visits are counted.

### Search engines
- Each page has a title, description and a "canonical" link that help Google understand and rank it.
- `docs/sitemap.xml` lists every page. If you add a page, add it to the sitemap too.
- The home page includes structured data describing the troop (ages, council, sponsor and so on). Update it if any of those details change.

### Posting an upcoming event
In `docs/news.html`, the **Upcoming Events** section has instructions in a comment. To post events:

1. Delete the "Upcoming events to be announced" note.
2. Uncomment the example list.
3. For each event, copy one `<li class="event">` block and edit its month, day, title, details and description.

Remove events once they've passed. When nothing is scheduled, restore the "to be announced" note.

### Adding a "Troop 40 in the News" story
Add a new `<li class="event">` block at the **top** of the list, so the newest story comes first. The date box shows the month and year the article was published. For an Eagle Scout story, list each Scout and their project. End each entry with a "Read the article" link.

## Publishing

The site is hosted on GitHub Pages from the `docs/` folder of the `main` branch. Pushing a change to `main` updates the live site, usually within a couple of minutes.

The `main` branch is protected against deletion and force-pushes. Only the repository owner can publish changes. Anyone else can suggest a change by opening a pull request, which the owner reviews and merges.

## Contact

- Email: [RVCTroop40scouts@gmail.com](mailto:RVCTroop40scouts@gmail.com)
- Facebook: [Troop 40 group](https://www.facebook.com/groups/199059495469/)
