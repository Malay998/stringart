# MalayPaul Arts — Gallery Page Editing Guide

> Best file name: `GALLERY_PAGE_EDITING_GUIDE.md`  
> Keep this guide in your website folder beside `gallery.html`.

---

# 0. How To Open This Guide Beautifully In VS Code

Open this file in VS Code.

Then press:

```txt
Ctrl + Shift + V
```

Or open preview on the side:

```txt
Ctrl + K, then V
```

This guide is written in Markdown, so HTML, CSS, and JavaScript examples will appear colourful in VS Code preview.

---

# 1. What This Gallery Page Controls

Your gallery page controls:

- Gallery hero section
- Featured hero artwork image
- Floating hero notes
- Portfolio filter buttons
- Gallery image cards
- Gallery card categories
- Gallery card text
- Wide / tall gallery layouts
- Image fallback placeholders
- Lightbox popup
- Next / previous lightbox arrows
- Lightbox title, type, description
- Memory strip section
- Memory collage images
- Emotional explanation cards
- Process section
- CTA section
- Footer
- Mobile sticky CTA
- Navbar active state
- Mobile menu
- Reveal animations
- Mouse glow effect

This page is usually saved as:

```txt
gallery.html
```

---

# 2. Quick Search Cheat Sheet

Press `Ctrl + F` in VS Code and search these:

| What You Want To Edit | Search This |
|---|---|
| Browser tab title | `<title>` |
| Main colours | `:root` |
| Navbar | `<nav class="navbar"` |
| Logo image | `logo.png` |
| Page identity | `body data-page="gallery"` |
| Hero section | `<header class="hero"` |
| Hero image | `gallery-hero.jpg` |
| Floating notes | `floating-note` |
| Main gallery section | `id="gallery"` |
| Filter buttons | `filter-btn` |
| Filter categories | `data-filter` |
| Gallery grid | `gallery-grid` |
| Gallery card | `gallery-card` |
| Card category | `data-category` |
| Card title for lightbox | `data-title` |
| Card type for lightbox | `data-type` |
| Card description for lightbox | `data-description` |
| Card image file | `<img src=` |
| Wide card style | `wide` |
| Tall card style | `tall` |
| Lightbox popup | `id="lightbox"` |
| Lightbox JS | `openLightbox` |
| Image fallback | `imageFallback` |
| Memory strip | `memory-strip` |
| Memory collage | `memory-collage` |
| Memory tile image | `memory-tile` |
| Process cards | `process-road` |
| CTA section | `class="cta"` |
| Footer | `premium-footer` |
| Mobile sticky button | `mobile-sticky-cta` |
| Reveal animation | `revealObserver` |

---

# 3. Before Editing Anything

Make a backup.

In your folder:

1. Copy `gallery.html`
2. Paste it in the same folder
3. Rename the copy:

```txt
gallery-backup.html
```

Now edit only:

```txt
gallery.html
```

When something breaks, open the backup and copy the working part back.

---

# 4. The Most Important Gallery Rule

A gallery card has two important sides:

## Side 1: What customer sees on the card

```html
<div class="card-content">
  <span class="card-pill">Couple Memory</span>
  <h3>Anniversary Portrait</h3>
  <p>A warm handmade portrait made for a love story.</p>
</div>
```

## Side 2: What the lightbox popup reads

```html
data-title="Anniversary Portrait"
data-type="Couple Memory"
data-description="A warm handmade portrait made for a love story."
```

So when you edit a gallery card, update both:

- Visible card text
- `data-title`, `data-type`, and `data-description`

That keeps the popup matching the card.

---

# 5. How To Change The Browser Tab Title

Search:

```html
<title>
```

You may see:

```html
<title>Gallery - MalayPaul Arts</title>
```

Better versions:

```html
<title>Gallery | MalayPaul Arts Handmade String Art</title>
```

```html
<title>MalayPaul Arts Gallery | Premium Handmade String Art</title>
```

```html
<title>MalayPaul Arts | Custom String Art Portfolio</title>
```

---

# 6. How To Change Main Colours

Search:

```css
:root
```

You will see:

```css
:root {
  --bg: #f5f1ea;
  --card: #fffaf3;
  --text: #2f2420;
  --muted: #7a6258;
  --gold: #b08968;
  --gold-dark: #8f5f3b;
  --line: #e8d7c4;
  --cream: #fffaf3;
  --deep: #2f2420;
  --deep-soft: #51382b;
}
```

## What these mean

| Variable | Meaning |
|---|---|
| `--bg` | Main page background |
| `--card` | Gallery card base colour |
| `--text` | Main dark text |
| `--muted` | Paragraph text |
| `--gold` | Premium gold |
| `--gold-dark` | Dark gold / brown |
| `--line` | Soft border colour |
| `--cream` | Premium cream |
| `--deep` | Dark CTA section |
| `--deep-soft` | Softer dark brown |

## Safe premium palette

```css
:root {
  --bg: #f5f1ea;
  --card: #fffaf3;
  --text: #2f2420;
  --muted: #7a6258;
  --gold: #b08968;
  --gold-dark: #8f5f3b;
  --line: #e8d7c4;
  --cream: #fffaf3;
  --deep: #2f2420;
  --deep-soft: #51382b;
  --shadow: rgba(62,47,47,0.14);
  --soft-shadow: rgba(62,47,47,0.08);
}
```

Do not use loud neon colours. Gallery should feel calm, premium, and expensive.

---

# 7. How To Change The Logo

Search:

```html
logo.png
```

You will find:

```html
<img src="logo.png" alt="MalayPaul Arts Logo">
```

## Easiest method

Put your logo in the same folder as `gallery.html` and name it:

```txt
logo.png
```

No code change needed.

## Different logo file name

Example file:

```txt
premium-logo.png
```

Change:

```html
<img src="logo.png" alt="MalayPaul Arts Logo">
```

to:

```html
<img src="premium-logo.png" alt="MalayPaul Arts Logo">
```

Do this for navbar and footer logo.

---

# 8. How To Edit Navbar Links

Search:

```html
<div class="menu" id="menu">
```

You will see:

```html
<a href="index.html" class="nav-link" data-page="home">Home</a>
<a href="order.html" class="nav-link" data-page="order">Order</a>
<a href="gallery.html" class="nav-link" data-page="gallery">Gallery</a>
<a href="contact.html" class="nav-link" data-page="contact">Contact</a>
```

## Change visible text

```html
<a href="gallery.html" class="nav-link" data-page="gallery">Gallery</a>
```

to:

```html
<a href="gallery.html" class="nav-link" data-page="gallery">Portfolio</a>
```

## Change destination

Change the `href`.

```html
<a href="portfolio.html" class="nav-link" data-page="gallery">Portfolio</a>
```

## Do not break active highlight

Keep this on gallery page:

```html
<body data-page="gallery">
```

And keep this for gallery nav link:

```html
data-page="gallery"
```

The JavaScript uses this to highlight the Gallery tab.

---

# 9. How To Edit The Hero Section

Search:

```html
<header class="hero">
```

You will see:

```html
<div class="eyebrow">Premium Handmade Portfolio</div>
<h1>Real memories, turned into <span>statement art</span>.</h1>
<p>
  This gallery is for the people who do not want a normal gift.
</p>
```

## Better hero options

```html
<div class="eyebrow">Premium Handmade Portfolio</div>
<h1>Real memories, turned into <span>statement art</span>.</h1>
<p>
  Explore handmade string art styles created for love stories, family memories, pets, names, logos, and gifts that deserve to feel personal.
</p>
```

```html
<div class="eyebrow">String Art Gallery</div>
<h1>Find the style your memory deserves.</h1>
<p>
  Every piece starts with a photo, a person, a pet, or a feeling. Use this gallery to choose the kind of artwork you want to create.
</p>
```

```html
<div class="eyebrow">Premium Handmade Inspiration</div>
<h1>Not just artwork. A memory made <span>visible</span>.</h1>
<p>
  Browse styles, open any piece, and use it as inspiration for your own custom handmade string art.
</p>
```

---

# 10. How To Edit Hero Buttons

Search:

```html
hero-actions
```

You will see:

```html
<div class="hero-actions">
  <a href="#gallery" class="btn btn-primary">Explore Gallery →</a>
  <a href="order.html" class="btn btn-soft">Create Similar Artwork</a>
</div>
```

## Better button options

```html
<a href="#gallery" class="btn btn-primary">Explore Portfolio →</a>
<a href="order.html" class="btn btn-soft">Create Yours</a>
```

```html
<a href="#gallery" class="btn btn-primary">View Artwork Styles →</a>
<a href="order.html" class="btn btn-soft">Start Custom Order</a>
```

```html
<a href="#gallery" class="btn btn-primary">Find Your Style →</a>
<a href="order.html" class="btn btn-soft">Reserve Slot</a>
```

Keep these classes:

```html
class="btn btn-primary"
class="btn btn-soft"
```

They control the styling.

---

# 11. How To Edit Hero Mini Steps

Search:

```html
hero-mini
```

You will see:

```html
<div class="hero-mini">
  <div class="mini-stat">
    <b>01</b>
    <small>Pick the artwork feeling you love.</small>
  </div>
  <div class="mini-stat">
    <b>02</b>
    <small>Send your photo and personal details.</small>
  </div>
  <div class="mini-stat">
    <b>03</b>
    <small>Get a handmade piece made only for you.</small>
  </div>
</div>
```

Better version:

```html
<div class="hero-mini">
  <div class="mini-stat">
    <b>01</b>
    <small>Choose the style that feels closest to your memory.</small>
  </div>
  <div class="mini-stat">
    <b>02</b>
    <small>Send your photo, size, and personal details.</small>
  </div>
  <div class="mini-stat">
    <b>03</b>
    <small>I guide you and create the artwork by hand.</small>
  </div>
</div>
```

Keep the text short so the cards stay clean.

---

# 12. How To Change Hero Featured Image

Search:

```html
gallery-hero.jpg
```

You will see:

```html
<div class="featured-frame" data-placeholder="Add your best artwork image here: gallery-hero.jpg">
  <img src="gallery-hero.jpg" alt="Featured MalayPaul Arts artwork" onerror="imageFallback(this)">
</div>
```

## Easiest method

Put your best gallery image in the same folder and name it:

```txt
gallery-hero.jpg
```

Then refresh the browser.

## Different file name

Example:

```txt
best-couple-art.jpg
```

Change both places:

```html
<div class="featured-frame" data-placeholder="Add your best artwork image here: best-couple-art.jpg">
  <img src="best-couple-art.jpg" alt="Featured MalayPaul Arts artwork" onerror="imageFallback(this)">
</div>
```

## Important

Keep this:

```html
onerror="imageFallback(this)"
```

It shows the premium placeholder when the image file is missing.

---

# 13. How To Edit Floating Hero Notes

Search:

```html
floating-note
```

You will see:

```html
<div class="floating-note note-one">
  <b>Not copied. Not printed.</b>
  <small>Every piece is patiently built by hand, thread by thread.</small>
</div>

<div class="floating-note note-two">
  <b>Gift-ready emotion.</b>
  <small>Perfect for birthdays, anniversaries, pets, couples, and family memories.</small>
</div>
```

Better versions:

```html
<div class="floating-note note-one">
  <b>Thread by thread.</b>
  <small>Each piece is built patiently by hand, not printed or mass-made.</small>
</div>

<div class="floating-note note-two">
  <b>Made to be gifted.</b>
  <small>Perfect for couples, families, pets, birthdays, and personal memories.</small>
</div>
```

Keep them short because floating notes have limited space.

---

# 14. How Gallery Filters Work

Your filter buttons look like:

```html
<button class="filter-btn active" data-filter="all">All</button>
<button class="filter-btn" data-filter="couple">Couple</button>
<button class="filter-btn" data-filter="pet">Pet</button>
<button class="filter-btn" data-filter="family">Family</button>
```

Gallery cards have categories like:

```html
data-category="couple portrait gift"
```

JavaScript checks this:

```js
const filter = button.dataset.filter;
const categories = card.dataset.category || "";
const shouldShow = filter === "all" || categories.includes(filter);
```

That means:

```txt
Button data-filter="pet"
shows cards that contain pet in data-category.
```

---

# 15. How To Add A New Filter Button

Search:

```html
<div class="filters">
```

Add a new button inside it.

Example: add `Logo` filter:

```html
<button class="filter-btn" data-filter="logo">Logo</button>
```

Now any gallery card with this:

```html
data-category="logo brand custom"
```

will show when Logo filter is clicked.

## Important

The `data-filter` word must match a word inside `data-category`.

Correct:

```html
<button class="filter-btn" data-filter="pet">Pet</button>
```

```html
<div class="gallery-card" data-category="pet portrait gift">
```

Wrong:

```html
<button class="filter-btn" data-filter="pets">Pet</button>
```

```html
<div class="gallery-card" data-category="pet portrait gift">
```

Here `pets` and `pet` do not match.

---

# 16. Good Filter Categories To Use

Recommended filters:

```html
<button class="filter-btn active" data-filter="all">All</button>
<button class="filter-btn" data-filter="couple">Couple</button>
<button class="filter-btn" data-filter="family">Family</button>
<button class="filter-btn" data-filter="pet">Pet</button>
<button class="filter-btn" data-filter="name">Name</button>
<button class="filter-btn" data-filter="logo">Logo</button>
<button class="filter-btn" data-filter="gift">Gift</button>
```

Recommended `data-category` examples:

```html
data-category="couple gift anniversary"
data-category="family gift portrait"
data-category="pet gift portrait"
data-category="name decor custom"
data-category="logo brand custom"
data-category="single portrait gift"
```

---

# 17. How To Edit Gallery Section Heading

Search:

```html
The Portfolio
```

You will see:

```html
<span class="section-kicker">The Portfolio</span>
<h2>Choose the kind of memory you want to frame forever.</h2>
<p>
  Use these pieces as inspiration. If you like a style, open it, send your photo,
  and we can create something with the same premium feeling for you.
</p>
```

Better version:

```html
<span class="section-kicker">The Portfolio</span>
<h2>Choose the memory you want to turn into art.</h2>
<p>
  Use these pieces as inspiration. Open any style, see the feeling, and start a similar custom artwork from your own photo.
</p>
```

More premium:

```html
<span class="section-kicker">Artwork Inspiration</span>
<h2>Every piece begins with a memory worth keeping.</h2>
<p>
  Browse couple portraits, pet artworks, family memories, names, logos, and custom ideas created for meaningful gifting.
</p>
```

---

# 18. How To Edit Filter Text

Search:

```html
Filter by what you are planning
```

You may see:

```html
<span>Filter by what you are planning to gift or keep.</span>
```

Change it to:

```html
<span>Choose the type of artwork you want to explore.</span>
```

or:

```html
<span>Filter by occasion, memory, or artwork style.</span>
```

---

# 19. How To Edit A Gallery Card

Search:

```html
gallery-card
```

A card will look like this:

```html
<div class="gallery-card reveal"
  data-category="couple gift"
  data-title="Couple Memory Portrait"
  data-type="Couple Artwork"
  data-description="A romantic artwork idea for anniversaries, birthdays, and personal gifting."
  onclick="openLightbox(0)"
  data-placeholder="Add artwork image: gallery-1.jpg">

  <img src="gallery-1.jpg" alt="Couple Memory Portrait" onerror="imageFallback(this)">

  <div class="open-cue">↗</div>

  <div class="card-content">
    <div class="card-pill">Couple Artwork</div>
    <h3>Couple Memory Portrait</h3>
    <p>A romantic artwork idea for anniversaries, birthdays, and personal gifting.</p>
  </div>
</div>
```

## Parts you can safely edit

```html
data-category="couple gift"
```

Controls filters.

```html
data-title="Couple Memory Portrait"
```

Controls lightbox title.

```html
data-type="Couple Artwork"
```

Controls lightbox small label.

```html
data-description="A romantic artwork idea..."
```

Controls lightbox paragraph.

```html
<img src="gallery-1.jpg">
```

Controls image file.

```html
<div class="card-pill">Couple Artwork</div>
```

Visible card label.

```html
<h3>Couple Memory Portrait</h3>
```

Visible card title.

```html
<p>A romantic artwork idea...</p>
```

Visible card description.

---

# 20. Gallery Card Editing Rule

When you change one card, update these together:

```html
data-title="..."
data-type="..."
data-description="..."
<img src="...">
alt="..."
<div class="card-pill">...</div>
<h3>...</h3>
<p>...</p>
```

Why?

Because:

- Card uses visible title
- Lightbox uses `data-title`
- Image alt helps accessibility
- Filter uses `data-category`

---

# 21. How To Change A Gallery Image

Example current image:

```html
<img src="gallery-1.jpg" alt="Couple Memory Portrait" onerror="imageFallback(this)">
```

Put your new image in the same folder:

```txt
couple-heart-art.jpg
```

Then change:

```html
<img src="couple-heart-art.jpg" alt="Couple Heart String Art" onerror="imageFallback(this)">
```

Also update placeholder:

```html
data-placeholder="Add artwork image: couple-heart-art.jpg"
```

And update lightbox title / card title:

```html
data-title="Couple Heart String Art"
<h3>Couple Heart String Art</h3>
```

---

# 22. Image File Naming Rules

Good file names:

```txt
gallery-1.jpg
couple-heart-art.jpg
family-portrait.jpg
pet-string-art.jpg
name-artwork.jpg
logo-string-art.jpg
```

Bad file names:

```txt
IMG_20260418 WhatsApp Final Photo (1).jpg
my image final final.jpg
Screenshot 2026-05-01 at 4.20.11 PM.png
```

Why bad?

Spaces and weird characters can cause hosting problems.

Best rule:

```txt
lowercase-words-with-dashes.jpg
```

---

# 23. Where To Put Image Files

Simple folder setup:

```txt
website-folder/
  index.html
  order.html
  gallery.html
  contact.html
  logo.png
  gallery-hero.jpg
  gallery-1.jpg
  gallery-2.jpg
  gallery-3.jpg
```

Better folder setup:

```txt
website-folder/
  index.html
  order.html
  gallery.html
  contact.html
  images/
    logo.png
    gallery-hero.jpg
    gallery-1.jpg
    gallery-2.jpg
```

When using an `images` folder, update code like this:

```html
<img src="images/gallery-1.jpg" alt="Couple Memory Portrait" onerror="imageFallback(this)">
```

---

# 24. Why Broken Images Still Look Nice

Your page has this function:

```js
function imageFallback(img) {
  const parent = img.closest(".gallery-card, .featured-frame, .memory-tile, .lightbox-image-wrap");
  if (parent) {
    parent.classList.add("image-missing");
  }
}
```

And images use:

```html
onerror="imageFallback(this)"
```

So when an image is missing, the parent gets:

```html
class="image-missing"
```

Then CSS shows a nice placeholder using:

```html
data-placeholder="Add artwork image: gallery-1.jpg"
```

## Do not remove this

```html
onerror="imageFallback(this)"
```

It keeps the page looking premium even before real images are added.

---

# 25. How To Change Placeholder Text

A gallery card may have:

```html
data-placeholder="Add artwork image: gallery-1.jpg"
```

Change it to:

```html
data-placeholder="Add your couple portrait artwork here"
```

or:

```html
data-placeholder="Replace with pet portrait photo"
```

Keep placeholder text short.

---

# 26. How To Add A New Gallery Card

Add this inside:

```html
<div class="gallery-grid">
```

Use this template:

```html
<div class="gallery-card reveal"
  data-category="couple gift anniversary"
  data-title="Couple Anniversary Portrait"
  data-type="Couple Artwork"
  data-description="A romantic handmade string art idea for anniversaries, birthdays, and emotional gifting."
  onclick="openLightbox(0)"
  data-placeholder="Add artwork image: couple-anniversary.jpg">

  <img src="couple-anniversary.jpg" alt="Couple Anniversary Portrait" onerror="imageFallback(this)">

  <div class="open-cue">↗</div>

  <div class="card-content">
    <div class="card-pill">Couple Artwork</div>
    <h3>Couple Anniversary Portrait</h3>
    <p>A romantic handmade string art idea for anniversaries, birthdays, and emotional gifting.</p>
  </div>
</div>
```

## Very important: update `openLightbox(index)`

If this is the first card:

```html
onclick="openLightbox(0)"
```

Second card:

```html
onclick="openLightbox(1)"
```

Third card:

```html
onclick="openLightbox(2)"
```

Fourth card:

```html
onclick="openLightbox(3)"
```

Counting starts from 0.

---

# 27. Better Way To Avoid Lightbox Index Mistakes

The current code uses:

```html
onclick="openLightbox(0)"
```

That means every card needs the correct number.

A safer setup is changing the JavaScript so cards automatically find their index.

Search this part near the script:

```js
const galleryCards = Array.from(document.querySelectorAll(".gallery-card"));
let activeIndex = 0;
```

Add this after it:

```js
galleryCards.forEach(function(card, index) {
  card.addEventListener("click", function() {
    openLightbox(index);
  });
});
```

Then remove `onclick="openLightbox(...)"` from all gallery cards.

Example card becomes:

```html
<div class="gallery-card reveal"
  data-category="couple gift anniversary"
  data-title="Couple Anniversary Portrait"
  data-type="Couple Artwork"
  data-description="A romantic handmade string art idea for anniversaries, birthdays, and emotional gifting."
  data-placeholder="Add artwork image: couple-anniversary.jpg">
```

This is cleaner because adding/removing cards will not break numbering.

---

# 28. How To Make A Card Wide

A normal card:

```html
<div class="gallery-card reveal">
```

Wide card:

```html
<div class="gallery-card wide reveal">
```

CSS:

```css
.gallery-card.wide {
  grid-column: span 8;
  min-height: 420px;
}
```

Use wide cards for your best photos.

---

# 29. How To Make A Card Tall

Normal card:

```html
<div class="gallery-card reveal">
```

Tall card:

```html
<div class="gallery-card tall reveal">
```

CSS:

```css
.gallery-card.tall {
  min-height: 480px;
}
```

Use tall cards for portrait-style artwork photos.

---

# 30. How To Make Cards Taller Or Shorter

Search:

```css
.gallery-card {
```

You may see:

```css
.gallery-card {
  grid-column: span 4;
  min-height: 390px;
}
```

Make normal cards taller:

```css
min-height: 430px;
```

Make normal cards shorter:

```css
min-height: 340px;
```

Tall cards:

```css
.gallery-card.tall {
  min-height: 480px;
}
```

Wide cards:

```css
.gallery-card.wide {
  grid-column: span 8;
  min-height: 420px;
}
```

---

# 31. How To Change Gallery Grid Layout

Search:

```css
.gallery-grid {
```

You will see:

```css
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 22px;
  max-width: 1190px;
  margin: auto;
}
```

This is a 12-column grid.

Normal card:

```css
grid-column: span 4;
```

So 3 normal cards fit in one row.

Wide card:

```css
grid-column: span 8;
```

So it takes 2/3 of row.

## Make cards bigger

Change normal card:

```css
grid-column: span 6;
```

This gives 2 cards per row.

## Make cards smaller

Keep:

```css
grid-column: span 4;
```

This gives 3 cards per row.

---

# 32. How To Make Gallery Text More Readable

Search:

```css
.gallery-card::after
```

You will see:

```css
background:
  linear-gradient(180deg, rgba(47,36,32,0.02), rgba(47,36,32,0.24) 42%, rgba(47,36,32,0.82)),
  radial-gradient(circle at top left, rgba(255,255,255,0.18), transparent 40%);
```

This dark overlay makes white text readable.

## Make bottom darker

```css
rgba(47,36,32,0.90)
```

## Make bottom lighter

```css
rgba(47,36,32,0.68)
```

Recommended:

```css
background:
  linear-gradient(180deg, rgba(47,36,32,0.02), rgba(47,36,32,0.24) 42%, rgba(47,36,32,0.82)),
  radial-gradient(circle at top left, rgba(255,255,255,0.18), transparent 40%);
```

---

# 33. How To Change Image Zoom On Hover

Search:

```css
.gallery-card:hover img
```

You will see:

```css
.gallery-card:hover img {
  transform: scale(1.08);
}
```

More zoom:

```css
transform: scale(1.13);
```

Less zoom:

```css
transform: scale(1.04);
```

No zoom:

```css
transform: none;
```

---

# 34. How To Edit Lightbox Popup

Search:

```html
<div class="lightbox" id="lightbox"
```

You will see:

```html
<div class="lightbox" id="lightbox" aria-hidden="true">
  <button class="lightbox-close" onclick="closeLightbox()" aria-label="Close gallery preview">×</button>
  <button class="lightbox-nav prev" onclick="moveLightbox(-1)" aria-label="Previous artwork">‹</button>
  <button class="lightbox-nav next" onclick="moveLightbox(1)" aria-label="Next artwork">›</button>
```

Lightbox opens when card runs:

```js
openLightbox(index)
```

Lightbox content comes from each card:

```js
document.getElementById("lightbox-title").innerText = card.dataset.title;
document.getElementById("lightbox-type").innerText = card.dataset.type;
document.getElementById("lightbox-description").innerText = card.dataset.description;
```

So to edit popup text, edit the card’s:

```html
data-title
data-type
data-description
```

---

# 35. How To Change Lightbox Buttons

Search:

```html
Create Similar →
```

You will see:

```html
<a href="order.html" class="btn btn-primary">Create Similar →</a>
<button class="btn btn-soft" onclick="closeLightbox()">Back to Gallery</button>
```

Better options:

```html
<a href="order.html" class="btn btn-primary">Create This Style →</a>
<button class="btn btn-soft" onclick="closeLightbox()">Back to Gallery</button>
```

```html
<a href="order.html" class="btn btn-primary">Start Similar Order →</a>
<button class="btn btn-soft" onclick="closeLightbox()">Keep Browsing</button>
```

Keep this:

```html
onclick="closeLightbox()"
```

The back button needs it.

---

# 36. How Lightbox Navigation Works

Your JS has:

```js
function moveLightbox(direction) {
  activeIndex = (activeIndex + direction + galleryCards.length) % galleryCards.length;
  openLightbox(activeIndex);
}
```

This means:

```txt
Next button moves forward.
Previous button moves backward.
When it reaches the last card, it loops to first card.
```

Keyboard controls:

```js
if (event.key === "ArrowRight") {
  moveLightbox(1);
}

if (event.key === "ArrowLeft") {
  moveLightbox(-1);
}
```

Escape closes lightbox:

```js
if (event.key === "Escape") {
  closeLightbox();
}
```

---

# 37. How To Edit Memory Strip Section

Search:

```html
memory-strip
```

You will find a dark premium section.

It usually has:

```html
<div class="memory-copy">
  <span class="section-kicker">...</span>
  <h2>...</h2>
  <p>...</p>
</div>
```

Better copy:

```html
<div class="memory-copy">
  <span class="section-kicker">Made from real moments</span>
  <h2>Every artwork starts with a photo that already means something.</h2>
  <p>
    The gallery is only inspiration. Your final piece is made from your own memory, your own person, your own pet, or your own story.
  </p>
</div>
```

---

# 38. How To Edit Memory Points

Search:

```html
memory-points
```

You may see:

```html
<div class="memory-point">...</div>
```

Better points:

```html
<div class="memory-point">Perfect for birthdays, anniversaries, proposals, and emotional surprises.</div>
<div class="memory-point">Made from real photos, not random templates.</div>
<div class="memory-point">Photo guidance helps the final artwork look cleaner.</div>
<div class="memory-point">Each artwork is built slowly with a handmade finish.</div>
```

Keep each point short.

---

# 39. How To Change Memory Collage Images

Search:

```html
memory-collage
```

You will see tiles like:

```html
<div class="memory-tile" data-placeholder="Add memory image: memory-1.jpg">
  <img src="memory-1.jpg" alt="Memory artwork" onerror="imageFallback(this)">
</div>
```

Change image file:

```html
<div class="memory-tile" data-placeholder="Add memory image: family-memory.jpg">
  <img src="family-memory.jpg" alt="Family memory artwork" onerror="imageFallback(this)">
</div>
```

Keep:

```html
onerror="imageFallback(this)"
```

---

# 40. How Memory Collage Layout Works

CSS:

```css
.memory-collage {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-auto-rows: 116px;
  gap: 14px;
}
```

Special tile sizes:

```css
.memory-tile:nth-child(1) {
  grid-column: span 3;
  grid-row: span 2;
}

.memory-tile:nth-child(4) {
  grid-column: span 2;
  grid-row: span 2;
}
```

Meaning:

- Tile 1 is big
- Tile 4 is big
- Others are smaller

Best images:

```txt
memory-1.jpg = strongest artwork
memory-4.jpg = second strongest artwork
```

---

# 41. How To Edit Emotional Cards

Search:

```html
emotion-grid
```

You will see cards like:

```html
<div class="emotion-card reveal">
  <div class="emotion-icon">♥</div>
  <h3>...</h3>
  <p>...</p>
</div>
```

Better cards:

```html
<div class="emotion-card reveal">
  <div class="emotion-icon">♥</div>
  <h3>For love stories</h3>
  <p>Couple portraits, anniversaries, birthdays, and photos that still feel special.</p>
</div>

<div class="emotion-card reveal">
  <div class="emotion-icon">🐾</div>
  <h3>For pets</h3>
  <p>Because pets are family, and their memories deserve more than a phone gallery.</p>
</div>

<div class="emotion-card reveal">
  <div class="emotion-icon">◆</div>
  <h3>For custom ideas</h3>
  <p>Names, logos, room decor, personal symbols, or anything that deserves a handmade touch.</p>
</div>
```

---

# 42. How To Edit Process Section

Search:

```html
process-road
```

You will see:

```html
<div class="process-step reveal">
  <div class="process-number">01</div>
  <h3>...</h3>
  <p>...</p>
</div>
```

Better version:

```html
<div class="process-road">
  <div class="process-step reveal">
    <div class="process-number">01</div>
    <h3>Choose style</h3>
    <p>Pick a gallery style that matches the feeling you want.</p>
  </div>

  <div class="process-step reveal">
    <div class="process-number">02</div>
    <h3>Send photo</h3>
    <p>Share your photo and notes so I can guide you properly.</p>
  </div>

  <div class="process-step reveal">
    <div class="process-number">03</div>
    <h3>Confirm details</h3>
    <p>We finalize size, concept, names, dates, and any custom ideas.</p>
  </div>

  <div class="process-step reveal">
    <div class="process-number">04</div>
    <h3>Handmade</h3>
    <p>The artwork is made carefully with a premium personal finish.</p>
  </div>
</div>
```

---

# 43. How To Edit CTA Section

Search:

```html
class="cta"
```

You may see:

```html
<section class="cta reveal">
  <div class="cta-inner">
    <h2>...</h2>
    <p>...</p>
    <div class="cta-row">
      <a href="order.html" class="btn btn-primary">...</a>
      <a href="contact.html" class="btn btn-soft">...</a>
    </div>
  </div>
</section>
```

Better CTA:

```html
<section class="cta reveal">
  <div class="cta-inner">
    <h2>Found a style you like? Let’s make it from your photo.</h2>
    <p>
      Pick a gallery style, send your reference photo, and I’ll guide you on the best size, layout, and final artwork direction.
    </p>

    <div class="cta-row">
      <a href="order.html" class="btn btn-primary">Start Custom Artwork →</a>
      <a href="contact.html" class="btn btn-soft">Ask Before Ordering</a>
    </div>
  </div>
</section>
```

---

# 44. How To Edit Footer

Search:

```html
premium-footer
```

You will see footer content.

Change footer brand:

```html
<h2 class="footer-brand">MalayPaul Arts</h2>
```

Change footer paragraph:

```html
<p class="footer-text">
  Premium handmade string art portraits crafted for memories, gifts, love stories, pets, families, and moments worth keeping forever.
</p>
```

Better:

```html
<p class="footer-text">
  Custom handmade string art portraits crafted for meaningful gifts, emotional memories, pets, families, love stories, and personal spaces.
</p>
```

Change footer note:

```html
<p class="footer-note">Handcrafted with care in India</p>
```

Better:

```html
<p class="footer-note">Made slowly. Remembered forever.</p>
```

---

# 45. How To Edit Mobile Sticky CTA

Search:

```html
mobile-sticky-cta
```

You will see:

```html
<a class="mobile-sticky-cta" href="order.html">Reserve Your Artwork Slot →</a>
```

Better:

```html
<a class="mobile-sticky-cta" href="order.html">Create From Your Photo →</a>
```

or:

```html
<a class="mobile-sticky-cta" href="order.html">Reserve Custom Artwork →</a>
```

Keep it short because it appears at the bottom of mobile screens.

---

# 46. How To Hide Mobile Sticky CTA

Search inside CSS:

```css
.mobile-sticky-cta {
```

On mobile it becomes visible here:

```css
.mobile-sticky-cta {
  position: fixed;
  left: 16px;
  right: 16px;
  bottom: calc(14px + env(safe-area-inset-bottom));
  display: inline-flex;
}
```

To hide it completely, set:

```css
.mobile-sticky-cta {
  display: none !important;
}
```

But keeping it is better for conversions.

---

# 47. How To Add WhatsApp Direct Button

Use this:

```html
<a href="https://wa.me/918087827454?text=Hi%20MalayPaul%20Arts%20I%20saw%20your%20gallery%20and%20want%20a%20custom%20string%20art" target="_blank" class="btn btn-primary">
  Message on WhatsApp →
</a>
```

Replace number:

```txt
918087827454
```

With your number using:

```txt
91XXXXXXXXXX
```

No plus sign, no spaces.

---

# 48. How To Add A New Section

Paste this before CTA:

```html
<section class="section">
  <div class="section-head reveal">
    <span class="section-kicker">Customer favourites</span>
    <h2>The most loved artwork styles.</h2>
    <p>
      These are the kinds of pieces people usually choose when they want the gift to feel personal and emotional.
    </p>
  </div>

  <div class="emotion-grid">
    <div class="emotion-card reveal">
      <div class="emotion-icon">♥</div>
      <h3>Couple portraits</h3>
      <p>Perfect for anniversaries, birthdays, long-distance gifts, and love stories.</p>
    </div>

    <div class="emotion-card reveal">
      <div class="emotion-icon">🐾</div>
      <h3>Pet memories</h3>
      <p>For the pets who became family and deserve a place on the wall.</p>
    </div>

    <div class="emotion-card reveal">
      <div class="emotion-icon">◆</div>
      <h3>Logo artwork</h3>
      <p>For brands, studios, rooms, cafes, creators, and personal spaces.</p>
    </div>
  </div>
</section>
```

---

# 49. How Reveal Animation Works

CSS:

```css
.reveal {
  opacity: 0;
  transform: translateY(28px);
  transition: 0.8s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

JavaScript:

```js
const revealElements = document.querySelectorAll(".reveal");

const revealObserver = new IntersectionObserver(function(entries) {
  entries.forEach(function(entry) {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
      revealObserver.unobserve(entry.target);
    }
  });
}, {
  threshold: 0.12
});
```

So for any new card or section to animate, add:

```html
reveal
```

Example:

```html
<div class="gallery-card reveal">
```

---

# 50. How To Make Reveal Animation Faster

Search:

```css
.reveal {
```

Change:

```css
transition: 0.8s ease;
```

to:

```css
transition: 0.55s ease;
```

Slower:

```css
transition: 1s ease;
```

More movement:

```css
transform: translateY(40px);
```

Less movement:

```css
transform: translateY(14px);
```

---

# 51. How To Edit Mobile Layout

Search:

```css
@media (max-width: 980px)
```

This controls tablet/mobile.

Search:

```css
@media (max-width: 540px)
```

This controls small phones.

Important mobile gallery rule:

```css
.gallery-card,
.gallery-card.tall,
.gallery-card.wide {
  min-height: 330px;
  border-radius: 28px;
}
```

Make mobile cards taller:

```css
min-height: 390px;
```

Make mobile cards shorter:

```css
min-height: 300px;
```

---

# 52. How To Fix Gallery Image Cropping

Gallery images use:

```css
.gallery-card img {
  object-fit: cover;
}
```

This fills the card but may crop edges.

## Show full image without cropping

```css
.gallery-card img {
  object-fit: contain;
  background: #fffaf3;
}
```

But this may leave empty space.

## Best for premium gallery

Keep:

```css
object-fit: cover;
```

Use properly cropped artwork photos.

---

# 53. How To Fix Lightbox Image Cropping

Search:

```css
.lightbox img
```

You may see:

```css
.lightbox img {
  max-width: 100%;
  width: 100%;
  height: 100%;
  max-height: 82vh;
  object-fit: cover;
}
```

To show full artwork in lightbox:

```css
.lightbox img {
  max-width: 100%;
  width: 100%;
  height: 100%;
  max-height: 82vh;
  object-fit: contain;
}
```

For gallery preview, `cover` looks premium.

For lightbox, `contain` can be better because customer can see full artwork.

Recommended lightbox version:

```css
.lightbox img {
  max-width: 100%;
  width: 100%;
  height: 100%;
  max-height: 82vh;
  object-fit: contain;
  background: #fffaf3;
}
```

---

# 54. How To Make Lightbox Wider Or Smaller

Search:

```css
.lightbox-shell {
```

You will see:

```css
.lightbox-shell {
  width: min(1080px, 96vw);
  max-height: 92vh;
  display: grid;
  grid-template-columns: minmax(0, 1fr) 340px;
}
```

Make info panel wider:

```css
grid-template-columns: minmax(0, 1fr) 400px;
```

Make lightbox bigger:

```css
width: min(1180px, 96vw);
```

Make lightbox smaller:

```css
width: min(940px, 94vw);
```

---

# 55. How To Change Mobile Menu

Search:

```html
<button class="hamburger"
```

Keep this:

```html
id="hamburger"
```

Search:

```html
<div class="menu" id="menu">
```

Keep this:

```html
id="menu"
```

Search:

```html
<div class="mobile-backdrop" id="mobileBackdrop"></div>
```

Keep this:

```html
id="mobileBackdrop"
```

JavaScript needs these IDs.

---

# 56. Common Mistakes And Fixes

## Mistake 1: Filter button not working

Check button:

```html
<button class="filter-btn" data-filter="logo">Logo</button>
```

Check card:

```html
data-category="logo brand custom"
```

The word must match.

---

## Mistake 2: Lightbox shows wrong card

You probably duplicated a card and forgot to change:

```html
onclick="openLightbox(3)"
```

Fix the number or use the safer automatic method from section 27.

---

## Mistake 3: Lightbox text does not match card

Update:

```html
data-title
data-type
data-description
```

and also visible:

```html
<div class="card-pill">
<h3>
<p>
```

---

## Mistake 4: Image not showing

Check file name.

These are different:

```txt
gallery-1.jpg
Gallery-1.jpg
gallery 1.jpg
gallery-1.JPG
```

Use exact names.

---

## Mistake 5: Placeholder not showing

Keep this on image:

```html
onerror="imageFallback(this)"
```

Keep this on card or frame:

```html
data-placeholder="Add artwork image: gallery-1.jpg"
```

---

## Mistake 6: New card does not animate

Add:

```html
reveal
```

Correct:

```html
<div class="gallery-card reveal">
```

---

## Mistake 7: New card not filtering correctly

Add the right category:

```html
data-category="pet portrait gift"
```

Button:

```html
data-filter="pet"
```

---

## Mistake 8: Gallery feels too crowded

Reduce cards per row:

```css
.gallery-card {
  grid-column: span 6;
}
```

Now there will be 2 cards per row on laptop instead of 3.

---

# 57. Best Gallery Card Templates

## Couple card

```html
<div class="gallery-card wide reveal"
  data-category="couple gift anniversary"
  data-title="Couple Anniversary Portrait"
  data-type="Couple Artwork"
  data-description="A romantic handmade string art idea for anniversaries, birthdays, proposals, and personal gifting."
  onclick="openLightbox(0)"
  data-placeholder="Add artwork image: couple-anniversary.jpg">

  <img src="couple-anniversary.jpg" alt="Couple Anniversary Portrait" onerror="imageFallback(this)">

  <div class="open-cue">↗</div>

  <div class="card-content">
    <div class="card-pill">Couple Artwork</div>
    <h3>Couple Anniversary Portrait</h3>
    <p>For anniversaries, birthdays, proposals, and love stories that deserve a wall.</p>
  </div>
</div>
```

## Pet card

```html
<div class="gallery-card tall reveal"
  data-category="pet gift portrait"
  data-title="Pet Memory Portrait"
  data-type="Pet Artwork"
  data-description="A handmade string art piece for the pet that became family."
  onclick="openLightbox(1)"
  data-placeholder="Add artwork image: pet-memory.jpg">

  <img src="pet-memory.jpg" alt="Pet Memory Portrait" onerror="imageFallback(this)">

  <div class="open-cue">↗</div>

  <div class="card-content">
    <div class="card-pill">Pet Artwork</div>
    <h3>Pet Memory Portrait</h3>
    <p>For pets that made the house warmer and the memories better.</p>
  </div>
</div>
```

## Family card

```html
<div class="gallery-card reveal"
  data-category="family gift portrait"
  data-title="Family Memory Artwork"
  data-type="Family Artwork"
  data-description="A handmade artwork idea for parents, grandparents, siblings, and family memories."
  onclick="openLightbox(2)"
  data-placeholder="Add artwork image: family-memory.jpg">

  <img src="family-memory.jpg" alt="Family Memory Artwork" onerror="imageFallback(this)">

  <div class="open-cue">↗</div>

  <div class="card-content">
    <div class="card-pill">Family Artwork</div>
    <h3>Family Memory Artwork</h3>
    <p>For photos that deserve to live outside the gallery app.</p>
  </div>
</div>
```

## Logo card

```html
<div class="gallery-card reveal"
  data-category="logo brand custom"
  data-title="Custom Logo String Art"
  data-type="Logo Artwork"
  data-description="A custom string art idea for brands, studios, cafes, rooms, and statement decor."
  onclick="openLightbox(3)"
  data-placeholder="Add artwork image: logo-art.jpg">

  <img src="logo-art.jpg" alt="Custom Logo String Art" onerror="imageFallback(this)">

  <div class="open-cue">↗</div>

  <div class="card-content">
    <div class="card-pill">Logo Artwork</div>
    <h3>Custom Logo String Art</h3>
    <p>For brands, studios, cafes, rooms, and decor with personality.</p>
  </div>
</div>
```

---

# 58. Recommended Gallery Image Names

Use these clean names:

```txt
gallery-hero.jpg
couple-anniversary.jpg
couple-heart-art.jpg
family-memory.jpg
pet-memory.jpg
single-portrait.jpg
name-artwork.jpg
logo-art.jpg
custom-artwork.jpg
memory-1.jpg
memory-2.jpg
memory-3.jpg
memory-4.jpg
memory-5.jpg
```

---

# 59. Full Testing Checklist

After editing, press:

```txt
Ctrl + S
```

Then refresh browser and check:

- [ ] Logo shows
- [ ] Navbar links work
- [ ] Gallery tab is highlighted
- [ ] Hero image shows
- [ ] Hero placeholder works when image is missing
- [ ] Explore Gallery button scrolls
- [ ] Create Similar button opens order page
- [ ] Filter buttons work
- [ ] All filter categories show correct cards
- [ ] Gallery images load
- [ ] Broken images show nice placeholders
- [ ] Card hover looks good on laptop
- [ ] Lightbox opens
- [ ] Lightbox title matches card
- [ ] Lightbox description matches card
- [ ] Next arrow works
- [ ] Previous arrow works
- [ ] Escape closes lightbox
- [ ] Clicking background closes lightbox
- [ ] Mobile menu opens
- [ ] Mobile menu closes
- [ ] Mobile sticky CTA works
- [ ] Memory collage images load
- [ ] Footer links work
- [ ] No sideways scrolling on mobile

---

# 60. Best Editing Workflow

Use this workflow:

```txt
Change one gallery card
Save
Refresh browser
Test card
Test filter
Test lightbox
Then edit next card
```

Do not edit 10 cards at once. Gallery pages break mostly because of small copy-paste mistakes.

---

# 61. Simple Mental Model

Think of the gallery page like this:

```txt
Hero
  ↓
Filters
  ↓
Gallery cards
  ↓
Lightbox popup
  ↓
Emotional proof
  ↓
Memory collage
  ↓
Process
  ↓
CTA
  ↓
Footer
```

Each gallery card is basically:

```txt
Image + visible card text + filter category + hidden lightbox text
```

When those four are correct, the gallery works beautifully.

---

# 62. Final Advice

Your gallery page is not just for showing photos.

It should make customers think:

```txt
“Oh, I can imagine my own photo becoming something like this.”
```

So every card should have:

- A strong image
- A clear category
- Emotional title
- Short premium description
- Working lightbox
- Clear CTA to order

That is what makes the gallery convert.
