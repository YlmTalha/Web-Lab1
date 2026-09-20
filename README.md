# Web Programming — Assignment 1

**Student:** Talha Yılmaz
**Course:** Web Programming, Fall 2026

A four-page website built with HTML5 only — no CSS file and no JavaScript anywhere.

## Theme

The site belongs to **Charge Mahal Enerji A.Ş.**, an electric vehicle charging network in Türkiye.
I chose it because I work at the company, so the content is real: the 34 public station locations,
the 12.99 TL/kWh DC and 9.99 TL/kWh AC tariffs and the eight charging-system families in the table
all come from the company's own material. The site is written in English.

## File organization

```
Lab1/
├── index.html        Home — header, navigation, three articles, footer
├── about.html        About — purpose, figure, semantic elements, video
├── services.html     Services — product table with thead/tbody/tfoot
├── contact.html      Contact — HTML form
├── README.md         This file
└── assets/
    ├── hero-station.jpg      index.html
    ├── network-map.jpg       index.html
    ├── dc-charger.jpg        index.html
    ├── charging-driver.jpg   about.html (inside <figure>)
    ├── video-poster.jpg      about.html (video poster frame)
    └── station-demo.mp4      about.html (11 s clip, 854×480 H.264)
```

All links use relative paths, so the site works both from the file system and over HTTP. Every
page carries the same `<nav>` block in its `<header>`.

## Image and video credits

| File | Author |
|---|---|
| `hero-station.jpg` | Juice (Unsplash) |
| `dc-charger.jpg` | CHUTTERSNAP (Unsplash) |
| `charging-driver.jpg` | Zaptec (Unsplash) |
| `station-demo.mp4` | Pexels |

`network-map.jpg` was drawn for this assignment from the company's station list, and
`video-poster.jpg` is a frame taken from the video clip.

## Challenges I faced

**Writing a real site with no CSS.** Without styling, structure is the only tool left. I used `<hr>`
between sections and real heading levels instead of styled text, so that the default browser
rendering still reads top to bottom. It made me think about which element is correct rather than
how it looks.

**Choosing between `<article>` and `<section>`.** I first wrapped everything in `<article>`. Reading
the specification again, `<article>` is for content that still makes sense on its own — which fits
the three blocks on the home page, but not the parts of one continuous "about us" text, so those
became `<section>`.

**Forms without JavaScript.** All validation had to come from HTML attributes: `required` on the
name, e-mail and message fields, and `type="email"` / `type="date"` so the browser supplies its own
keyboard and validation. Linking every `<label>` to its control with `for` / `id` is also what makes
the label text clickable.
