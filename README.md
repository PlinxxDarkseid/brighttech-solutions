# BrightTech Solutions — company website

A responsive website for **BrightTech Solutions**, a (fictional) Accra company that sells and supports
computer hardware, software, networking and IT support.

Built for the Web Technologies practical assignment (Level 300, first semester, Knutsford University)
using **HTML and CSS only**: no JavaScript, no Bootstrap or other frameworks, and no external
libraries. Every file the site uses is in this repository.

**Live site:** https://plinxxdarkseid.github.io/brighttech-solutions/

![BrightTech Solutions home page on a laptop](docs/screenshot-desktop.png)

---

## Requirements checklist

| # | Requirement | Where it is |
|---|---|---|
| 1 | **Home page**: company name and logo, welcome message, navigation menu, relevant image | Header logo and name; hero headline with "Welcome to BrightTech Solutions"; menu links to every section; product drawings on the shelf |
| 2 | **About us**: history, mission and vision, headings and paragraphs | `#about`: company story, a dated history timeline, mission and vision statements |
| 3 | **Services**: at least four, as lists/sections/cards, with icons | `#services`: four services with icons and lists, "How a repair works" steps, support plans table |
| 4 | **Our team**: at least four members with name, position, photograph, biography | `#team`: four members |
| 5 | **Products**: at least five with name, image, description, price | `#products`: eight products with a CSS-only category filter |
| 6 | **Contact form**: name, email, phone, subject, message, submit | `#contact`: validated form that opens `thanks.html` |
| 7 | **HTML elements**: at least five of the listed ten | All ten are used (see below) |
| 8 | **CSS styling**: colour scheme, navigation, layout, buttons, tables, forms, images, spacing, fonts, responsive | `style.css`, organised in 15 numbered sections |

### All ten HTML elements

| Element | Used for |
|---|---|
| Ordered list `<ol>` | Company history timeline; "How a repair works" steps |
| Unordered list `<ul>` | What each service includes; navigation; product grid; footer links |
| Table `<table>` | Support plans comparison; opening hours |
| Hyperlinks `<a>` | Navigation, buttons, footer |
| Images `<img>` | Logo, product drawings, service icons, team photographs |
| Video `<video>` | "BrightTech in half a minute" film, with English captions (`<track>`) |
| Audio `<audio>` | Recorded support-line greeting |
| Email link `mailto:` | Contact details; every product's "Order by email" button pre-fills the subject |
| Telephone link `tel:` | Header button, contact details, footer |
| Google Maps link | Showroom address, contact details, footer |

---

## Interactive without JavaScript

| Feature | How it works |
|---|---|
| Mobile menu | A hidden checkbox and its `<label>` (the menu button). `.menu-toggle:checked ~ .site-nav` shows the links. |
| Product filter | Radio buttons, and `:has()` hides products outside the chosen category. Products animate back in when they reappear. |
| Form validation | `required`, `type="email"`, `pattern` and `minlength` in HTML, and `:user-invalid` in CSS shows each error only after the visitor has typed. |
| FAQ accordion | Native `<details>` and `<summary>`, with a plus sign drawn in CSS. |
| Subject suggestions | `<datalist>` suggests subjects while still allowing free text. |
| Smooth scrolling | `scroll-behavior: smooth`, with `scroll-padding-top` so headings are not hidden under the sticky header. |
| Reading progress bar and header colour change | Scroll-driven animations (`animation-timeline: scroll()`), only where the browser supports them. |
| Animations | Products land on the shelf and price tags swing in on load, all switched off for visitors who prefer reduced motion. |

## Accessibility and quality

- Semantic structure: `header`, `nav`, `main`, `section`, `article`, `aside`, `address`, `figure`, `footer`.
- Every form field has a `<label>`; every image has `alt` text (decorative icons use `alt=""`).
- Skip link, visible keyboard focus everywhere, colour contrast checked for projectors.
- Validates with no errors in the W3C HTML checker.
- Tested at desktop (1440px), tablet and phone (390px) widths with no sideways scrolling.

---

## Folder structure

```
index.html          the whole site (six sections)
thanks.html         page shown after the contact form is sent
style.css           all styling
favicon.svg         browser tab icon
fonts/              Funnel Display and Funnel Sans (SIL Open Font License, see fonts/OFL.txt)
images/             logo, product drawings, service icons, team photographs
media/              brand film (MP4), its captions (VTT) and poster, support-line audio (MP3)
docs/               screenshots for this README
```

## Viewing it

- **Online:** open the live site link above (GitHub Pages).
- **On your computer:** open `index.html` in a browser. Everything works except the video captions,
  which browsers only load from a web server, so use the live site to see those.

## Team

| Member | Role on the site | Built |
|---|---|---|
| Kwame Mensah | Managing Director | Home page, header and navigation, mobile menu, colour scheme and typography |
| Ama Owusu | Head of Networking & Security | About us and Services, history timeline, support plans table |
| Yaw Boateng | Lead Software Engineer | Our team and Products, product filter, product drawings |
| Efua Asante | Customer Support Manager | Contact form and validation, thank-you page, video and audio, footer, GitHub Pages |

## Credits

- Illustrations, icons and logo: original SVG drawings made for this site.
- Brand film: animated in HTML and CSS, rendered to MP4; voice-over and support-line greeting
  recorded with a neural text-to-speech voice.
- Fonts: Funnel Display and Funnel Sans, © The Funnel Project Authors, SIL Open Font License 1.1.
- BrightTech Solutions, its staff, prices and address are fictional, created for this assignment.
