# MalayPaul Arts — Home Page Editing Guide

> Best file name: `HOME_PAGE_EDITING_GUIDE.md`  
> Keep this file in the same folder as your website files so you can open it anytime while editing `index.html`.

---

# 0. How To Use This Guide In VS Code

Open this file in VS Code.

To see it beautifully formatted:

```txt
Ctrl + Shift + V
```

Or open the Markdown preview on the side:

```txt
Ctrl + K, then V
```

This guide uses colourful code blocks like this:

````md
```html
<h1>Your headline here</h1>
```
````

Use this guide while editing your **home page**, usually named:

```txt
index.html
```

---

# 1. What This Page Is

This is your premium **home page** for MalayPaul Arts.

It controls:

- Navbar
- Logo
- Hero section
- Main emotional headline
- Hero buttons
- Trust badges
- Floating hero cards
- Hero artwork preview
- Emotional selling sections
- Premium difference cards
- Scarcity / FOMO strip
- Simple process timeline
- Artwork ideas
- Gallery preview placeholders
- Comparison section
- Final CTA
- Footer
- Mobile sticky CTA
- Reveal animations
- Mobile menu
- Mouse glow effect

This page does **not** control:

- Actual order prices
- Coupon codes
- Order form calculation
- WhatsApp order summary

Those belong to `order.html`.

---

# 2. Quick Search Cheat Sheet

Use `Ctrl + F` in VS Code.

| What You Want To Edit | Search This |
|---|---|
| Page title | `<title>` |
| Colours | `:root` |
| Navbar | `<nav class="navbar"` |
| Logo image | `logo.png` |
| Hero section | `<header class="hero"` |
| Main headline | `Your photo deserves` |
| Hero subtitle | `Turn one meaningful photo` |
| Main button | `Start Your Artwork` |
| Secondary button | `See Why It Feels Special` |
| Trust badges | `micro-trust` |
| Hero stats strip | `hero-proof-strip` |
| Floating cards | `float-card` |
| Hero artwork image | `portrait-inner` |
| Hero label | `portrait-label` |
| First emotional section | `Most gifts are forgotten` |
| Emotion cards | `emotion-card` |
| Premium cards | `premium-card` |
| Proof stats | `proof-row` |
| FOMO strip | `scarcity-strip` |
| Process timeline | `timeline` |
| Artwork ideas | `choice-grid` |
| Gallery preview | `gallery-showcase` |
| Comparison section | `comparison-wrap` |
| Final CTA | `final-cta` |
| Footer | `premium-footer` |
| Mobile sticky button | `mobile-sticky-cta` |
| Reveal animation | `revealObserver` |
| Mouse glow | `pointermove` |
| Mobile menu script | `openMenu` |

---

# 3. Before Editing Anything

Always make a backup first.

In your project folder:

1. Right-click `index.html`
2. Copy
3. Paste
4. Rename the copy:

```txt
index-backup.html
```

Now edit only:

```txt
index.html
```

If anything breaks, open backup and copy the working code back.

---

# 4. How To Change The Browser Tab Title

Search:

```html
<title>
```

You will see:

```html
<title>MalayPaul Arts | Premium Handmade String Art</title>
```

Change it to something like:

```html
<title>MalayPaul Arts | Custom Handmade String Art Gifts</title>
```

or more premium:

```html
<title>MalayPaul Arts | Premium Handmade Memory Portraits</title>
```

This title appears in the browser tab and Google search preview.

---

# 5. How To Change The Website Colours

Search:

```css
:root
```

You will see something like:

```css
:root {
  --bg: #f7f0e7;
  --cream: #fffaf3;
  --cream-soft: #fbf1e5;
  --text: #2f2420;
  --muted: #80685d;
  --gold: #b08968;
  --gold-light: #d7b38f;
  --gold-dark: #8f5f3b;
  --brown: #4b3328;
  --deep: #251a17;
}
```

These are your main design colours.

## What each colour does

| Variable | Meaning |
|---|---|
| `--bg` | Main warm background |
| `--cream` | Card / soft white background |
| `--text` | Main dark text |
| `--muted` | Paragraph text |
| `--gold` | Main premium gold |
| `--gold-light` | Light gold highlight |
| `--gold-dark` | Dark gold / brown button |
| `--deep` | Dark luxury section colour |

## Safe premium colour setup

```css
:root {
  --bg: #f7f0e7;
  --cream: #fffaf3;
  --cream-soft: #fbf1e5;
  --text: #2f2420;
  --muted: #80685d;
  --muted-2: #a08374;
  --gold: #b08968;
  --gold-light: #d7b38f;
  --gold-dark: #8f5f3b;
  --brown: #4b3328;
  --deep: #251a17;
  --line: #e5cfb9;
  --green: #567c55;
}
```

Do not use bright red, blue, purple, or neon colours here if you want it to stay premium.

---

# 6. How To Change The Logo

Search:

```html
logo.png
```

You will find logo usage in the navbar and footer.

Navbar logo:

```html
<img src="logo.png" alt="MalayPaul Arts Logo" />
```

Footer logo:

```html
<img src="logo.png" alt="MalayPaul Arts Logo" />
```

## Easiest way

Put your logo image in the same folder as `index.html` and name it:

```txt
logo.png
```

Then refresh the browser.

No code change needed.

## If your logo has another name

Example file:

```txt
my-premium-logo.png
```

Change:

```html
<img src="logo.png" alt="MalayPaul Arts Logo" />
```

to:

```html
<img src="my-premium-logo.png" alt="MalayPaul Arts Logo" />
```

Do this in both navbar and footer.

---

# 7. How To Make The Logo Bigger Or Smaller

Search:

```css
.nav-logo {
```

You may see:

```css
.nav-logo {
  width: 44px;
  height: 44px;
  padding: 6px;
}
```

Make navbar logo bigger:

```css
.nav-logo {
  width: 52px;
  height: 52px;
  padding: 6px;
}
```

Make it smaller:

```css
.nav-logo {
  width: 38px;
  height: 38px;
  padding: 5px;
}
```

## Footer logo size

Search:

```css
.footer-logo-space {
```

You may see:

```css
.footer-logo-space {
  width: 104px;
  height: 104px;
  padding: 12px;
}
```

Make footer logo bigger:

```css
.footer-logo-space {
  width: 120px;
  height: 120px;
  padding: 14px;
}
```

---

# 8. How To Change Brand Name Text

Search:

```html
<div class="logo">MalayPaul Arts</div>
```

Change to:

```html
<div class="logo">Malay Paul Arts</div>
```

or:

```html
<div class="logo">MalayPaul Art</div>
```

Footer brand:

```html
<h2 class="footer-brand">MalayPaul Arts</h2>
```

Change that too if you want the same name everywhere.

---

# 9. How To Edit Navbar Links

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

## Change visible tab name

Example:

```html
<a href="gallery.html" class="nav-link" data-page="gallery">Gallery</a>
```

to:

```html
<a href="gallery.html" class="nav-link" data-page="gallery">Works</a>
```

## Change where tab goes

Change the `href`.

Example:

```html
<a href="gallery.html" class="nav-link" data-page="gallery">Works</a>
```

`href="gallery.html"` controls where it goes.

## Do not randomly change `data-page`

This helps the active navbar highlight work.

Keep these:

```html
data-page="home"
data-page="order"
data-page="gallery"
data-page="contact"
```

---

# 10. How To Change Navbar CTA Button

Search:

```html
Reserve Slot
```

You will see:

```html
<a href="order.html" class="nav-cta">Reserve Slot</a>
```

Change button text:

```html
<a href="order.html" class="nav-cta">Start Order</a>
```

or:

```html
<a href="order.html" class="nav-cta">Create Yours</a>
```

If you want it to go to WhatsApp directly, replace `href`.

Example:

```html
<a href="https://wa.me/918087827454?text=Hi%20MalayPaul%20Arts%20I%20want%20to%20create%20a%20custom%20string%20art" class="nav-cta" target="_blank">WhatsApp Me</a>
```

---

# 11. How To Edit The Hero Section

Search:

```html
<header class="hero">
```

This is the top main section.

You will see something like:

```html
<div class="eyebrow"><span class="dot"></span> Premium handmade string art portraits</div>
<h1>Your photo deserves more than a <span>scroll.</span></h1>
<p class="hero-text">
  Turn one meaningful photo into a handcrafted artwork that feels personal, emotional, and impossible to ignore.
</p>
```

## Change eyebrow

```html
<div class="eyebrow"><span class="dot"></span> Premium handmade string art portraits</div>
```

Better options:

```html
<div class="eyebrow"><span class="dot"></span> Custom handmade gifts from real memories</div>
```

```html
<div class="eyebrow"><span class="dot"></span> Handmade string art crafted for emotional gifting</div>
```

```html
<div class="eyebrow"><span class="dot"></span> Personal portraits made with thread, time, and care</div>
```

---

# 12. How To Change The Main Hero Headline

Search:

```html
Your photo deserves
```

You will see:

```html
<h1>Your photo deserves more than a <span>scroll.</span></h1>
```

The `<span>` part gets gold highlight styling.

## Premium headline options

```html
<h1>Your photo deserves more than a <span>scroll.</span></h1>
```

```html
<h1>Turn their favourite photo into a <span>forever memory.</span></h1>
```

```html
<h1>A gift that feels personal before they even <span>open it.</span></h1>
```

```html
<h1>Some photos deserve a wall, not just a <span>gallery app.</span></h1>
```

```html
<h1>Make the memory feel impossible to <span>ignore.</span></h1>
```

## Rule

Keep the headline short and emotional.

Bad:

```html
<h1>We provide affordable custom handmade string art portraits with many sizes and offers.</h1>
```

Better:

```html
<h1>Some memories deserve more than a <span>scroll.</span></h1>
```

---

# 13. How To Edit Hero Paragraph

Search:

```html
class="hero-text"
```

You will see:

```html
<p class="hero-text">
  Turn one meaningful photo into a handcrafted artwork that feels personal, emotional, and impossible to ignore. Made slowly, guided personally, and created for the kind of memory people actually keep.
</p>
```

Better options:

```html
<p class="hero-text">
  Send one meaningful photo and turn it into a handcrafted string art piece made with patience, personal guidance, and the kind of detail that makes people pause.
</p>
```

```html
<p class="hero-text">
  A photo can stay hidden in a phone forever. Or it can become a handmade artwork they see every day, remember every day, and keep for years.
</p>
```

```html
<p class="hero-text">
  I help you choose the right photo, size, and idea so your gift feels personal, not random. Every artwork is made slowly, carefully, and with real emotional value.
</p>
```

---

# 14. How To Edit Hero Buttons

Search:

```html
hero-actions
```

You will see:

```html
<div class="hero-actions">
  <a href="order.html" class="btn btn-primary">Start Your Artwork →</a>
  <a href="#why" class="btn btn-soft">See Why It Feels Special</a>
</div>
```

## Change primary button text

```html
<a href="order.html" class="btn btn-primary">Start Your Artwork →</a>
```

Options:

```html
<a href="order.html" class="btn btn-primary">Reserve Your Artwork →</a>
```

```html
<a href="order.html" class="btn btn-primary">Create My Gift →</a>
```

```html
<a href="order.html" class="btn btn-primary">Start My Custom Piece →</a>
```

## Change secondary button

```html
<a href="#why" class="btn btn-soft">See Why It Feels Special</a>
```

Options:

```html
<a href="#why" class="btn btn-soft">Why It Feels Different</a>
```

```html
<a href="gallery.html" class="btn btn-soft">View Gallery</a>
```

```html
<a href="contact.html" class="btn btn-soft">Ask First</a>
```

## Important

Keep the `class` names:

```html
class="btn btn-primary"
class="btn btn-soft"
```

Those control the button styling.

---

# 15. How To Edit Trust Badges

Search:

```html
micro-trust
```

You will see:

```html
<div class="micro-trust">
  <span>Photo guidance included</span>
  <span>Gift-ready planning</span>
  <span>Limited handmade slots</span>
</div>
```

Change the text inside each `<span>`.

Better options:

```html
<div class="micro-trust">
  <span>Photo selection help</span>
  <span>Made for emotional gifting</span>
  <span>Limited handmade slots</span>
</div>
```

```html
<div class="micro-trust">
  <span>WhatsApp guidance</span>
  <span>Custom size options</span>
  <span>Made with real thread work</span>
</div>
```

To add one more badge:

```html
<span>Personal design support</span>
```

Full example:

```html
<div class="micro-trust">
  <span>Photo selection help</span>
  <span>Gift-ready planning</span>
  <span>Limited handmade slots</span>
  <span>Personal design support</span>
</div>
```

---

# 16. How To Edit The Hero Proof Strip

Search:

```html
hero-proof-strip
```

You will see:

```html
<div class="hero-proof-strip premium-glow">
  <div class="hero-proof-item">
    <strong>Slow</strong>
    <span>handmade finish</span>
  </div>
  <div class="hero-proof-item">
    <strong>Gift</strong>
    <span>ready planning</span>
  </div>
  <div class="hero-proof-item">
    <strong>1:1</strong>
    <span>WhatsApp help</span>
  </div>
</div>
```

Better options:

```html
<div class="hero-proof-strip premium-glow">
  <div class="hero-proof-item">
    <strong>1:1</strong>
    <span>photo guidance</span>
  </div>
  <div class="hero-proof-item">
    <strong>Gift</strong>
    <span>ready emotion</span>
  </div>
  <div class="hero-proof-item">
    <strong>Slow</strong>
    <span>handmade detail</span>
  </div>
</div>
```

Keep each word very short so it looks clean.

---

# 17. How To Edit Floating Hero Cards

Search:

```html
float-card one
```

You will see:

```html
<div class="float-card one">
  <strong>Not printed.</strong>
  <span>Every line is placed with patience and detail.</span>
</div>
```

There are 3 floating cards:

```html
<div class="float-card one">...</div>
<div class="float-card two">...</div>
<div class="float-card three">...</div>
```

## Premium copy options

```html
<div class="float-card one">
  <strong>Not printed.</strong>
  <span>Made with real thread, nails, time, and patience.</span>
</div>

<div class="float-card two">
  <strong>Made for reactions.</strong>
  <span>The kind of gift people remember after the occasion ends.</span>
</div>

<div class="float-card three">
  <strong>Guided personally.</strong>
  <span>I help you choose the photo before the artwork starts.</span>
</div>
```

Keep them short. Floating cards look bad if text is too long.

---

# 18. How To Change Hero Preview Image

Search:

```css
.portrait-inner {
```

Inside it, you will see:

```css
.portrait-inner {
  background:
    linear-gradient(rgba(47,36,32,0.06), rgba(47,36,32,0.12)),
    url('https://images.unsplash.com/photo-1529336953121-a0c6f5f6f3f4?auto=format&fit=crop&w=1000&q=80');
  background-size: cover;
  background-position: center;
}
```

Replace the URL with your own image.

## Best way

Put your artwork image in the same folder and name it:

```txt
hero-artwork.jpg
```

Then change the CSS to:

```css
.portrait-inner {
  position: relative;
  height: 100%;
  border-radius: 41px;
  overflow: hidden;
  background:
    linear-gradient(rgba(47,36,32,0.06), rgba(47,36,32,0.12)),
    url('hero-artwork.jpg');
  background-size: cover;
  background-position: center;
}
```

## If image face gets cut

Change:

```css
background-position: center;
```

to:

```css
background-position: center top;
```

or:

```css
background-position: center 35%;
```

---

# 19. How To Edit Hero Preview Label

Search:

```html
portrait-label
```

You will see:

```html
<div class="portrait-label">
  <small>Custom memory piece</small>
  <h3>One photo. One story. One artwork.</h3>
  <p>Replace this hero photo with your best artwork image later for an even stronger premium feel.</p>
</div>
```

Better version:

```html
<div class="portrait-label">
  <small>Custom memory piece</small>
  <h3>One photo. One story. One handmade artwork.</h3>
  <p>Send your favourite photo and I’ll help turn it into a piece that feels personal, premium, and worth keeping.</p>
</div>
```

Shorter version:

```html
<div class="portrait-label">
  <small>Handmade string art</small>
  <h3>Made from one meaningful photo.</h3>
  <p>Personal, emotional, and crafted slowly with real detail.</p>
</div>
```

---

# 20. How To Edit The First Emotional Section

Search:

```html
Most gifts are forgotten
```

You will see:

```html
<h2>Most gifts are forgotten. The right memory stays.</h2>
<p>
  A normal gift is used for a few days. A personal artwork becomes part of their room, their wall, and their story.
</p>
```

Better options:

```html
<h2>Most gifts disappear. The right memory stays visible.</h2>
<p>
  A normal gift may be useful for a few days. A personal artwork becomes part of their room, their wall, and their story.
</p>
```

```html
<h2>They already have things. Give them a memory.</h2>
<p>
  A handmade artwork feels different because it is built from something real: a person, a photo, a moment, or a feeling.
</p>
```

---

# 21. How To Edit Emotion Cards

Search:

```html
emotion-card
```

You will see cards like:

```html
<div class="emotion-card reveal">
  <div class="icon-pill">♥</div>
  <h3>For love stories</h3>
  <p>Couple portraits, anniversaries, birthdays, proposals, or that one photo that still feels special.</p>
</div>
```

## Change icon

Edit this:

```html
<div class="icon-pill">♥</div>
```

Examples:

```html
<div class="icon-pill">✦</div>
<div class="icon-pill">◆</div>
<div class="icon-pill">♡</div>
<div class="icon-pill">🐾</div>
<div class="icon-pill">👨‍👩‍👧</div>
```

## Add a new emotion card

Paste this inside the `emotion-grid`:

```html
<div class="emotion-card reveal">
  <div class="icon-pill">🎁</div>
  <h3>For unforgettable gifts</h3>
  <p>When you want the gift to feel personal, emotional, and clearly made just for them.</p>
</div>
```

## Important

Keep this class:

```html
reveal
```

That makes the card animate on scroll.

---

# 22. How To Edit Premium Difference Cards

Search:

```html
premium-grid
```

You will see 3 cards:

```html
<div class="premium-card reveal">
  ...
</div>

<div class="premium-card featured reveal">
  ...
</div>

<div class="premium-card reveal">
  ...
</div>
```

The middle card is dark because it has:

```html
featured
```

## Move dark featured card

If you want the first card to be dark, change:

```html
<div class="premium-card reveal">
```

to:

```html
<div class="premium-card featured reveal">
```

Then remove `featured` from the old dark card.

Only one should have:

```html
featured
```

unless you intentionally want multiple dark cards.

## Better premium card copy

```html
<div class="premium-card reveal">
  <div class="mini-label">01 / Photo clarity</div>
  <h3>I help you choose the right photo</h3>
  <p>Some photos look beautiful in your gallery but may not work well as string art. I help you choose the one that will look clean, sharp, and premium.</p>
</div>

<div class="premium-card featured reveal">
  <div class="mini-label">02 / Handmade attention</div>
  <h3>No mass-produced feeling</h3>
  <p>Your artwork is made slowly and personally, so it feels intentional — not like a random last-minute gift.</p>
</div>

<div class="premium-card reveal">
  <div class="mini-label">03 / Gift-ready emotion</div>
  <h3>Made around their memory</h3>
  <p>Name, date, quote, heart shape, pet portrait, couple portrait, or family concept — the details make it feel made only for them.</p>
</div>
```

---

# 23. How To Edit Proof Cards

Search:

```html
proof-row
```

You will see:

```html
<div class="proof-card reveal">
  <strong>1:1</strong>
  <h3>Personal guidance</h3>
  <p>Customers do not feel lost. They get help choosing photo, style, size, and occasion details.</p>
</div>
```

Better options:

```html
<div class="proof-card reveal">
  <strong>1:1</strong>
  <h3>Personal guidance</h3>
  <p>I help customers choose photo, style, size, and details before the artwork starts.</p>
</div>

<div class="proof-card reveal">
  <strong>0</strong>
  <h3>Generic gifting feel</h3>
  <p>The whole website reminds them this is made from their real memory, not random decor.</p>
</div>

<div class="proof-card reveal">
  <strong>∞</strong>
  <h3>Memory value</h3>
  <p>Unlike a normal gift, this keeps living on their wall, shelf, or room corner.</p>
</div>
```

---

# 24. How To Edit FOMO / Scarcity Strip

Search:

```html
scarcity-strip
```

You will see:

```html
<h2>Handmade work needs time. Last-minute gifts rarely feel this personal.</h2>
<p>
  I take limited custom requests at a time so each piece gets proper attention.
</p>
```

Better versions:

```html
<h2>Handmade work needs time. The best gifts don’t feel rushed.</h2>
<p>
  I take limited custom requests at a time so each artwork gets proper attention. If this is for a birthday, anniversary, farewell, proposal, or surprise gift, starting early gives us time to choose the best photo and make it feel right.
</p>
```

More emotional:

```html
<h2>If the memory matters, don’t leave it for the last moment.</h2>
<p>
  A handmade artwork needs time, attention, and the right photo. Reserving early gives us space to make the final piece feel personal instead of rushed.
</p>
```

## Change slot box

Search:

```html
Few slots
```

You will see:

```html
<span>Limited order flow</span>
<strong>Few slots</strong>
```

Change to:

```html
<span>Handmade capacity</span>
<strong>Limited slots</strong>
```

or:

```html
<span>Custom requests</span>
<strong>Open now</strong>
```

---

# 25. How To Edit The Process Timeline

Search:

```html
timeline
```

You will see 4 process steps:

```html
<div class="step reveal">
  <div class="number">01</div>
  <h3>Choose size</h3>
  <p>Pick the artwork size that fits your budget, wall space, and occasion.</p>
</div>
```

## Better process copy

```html
<div class="timeline">
  <div class="step reveal">
    <div class="number">01</div>
    <h3>Choose size</h3>
    <p>Pick a size that fits your budget, wall space, and gifting plan.</p>
  </div>

  <div class="step reveal">
    <div class="number">02</div>
    <h3>Choose style</h3>
    <p>Single face, couple, family, pet, name, logo, or something fully custom.</p>
  </div>

  <div class="step reveal">
    <div class="number">03</div>
    <h3>Send photo</h3>
    <p>Share your reference photo and notes. I’ll guide you if another photo will work better.</p>
  </div>

  <div class="step reveal">
    <div class="number">04</div>
    <h3>Handcrafted</h3>
    <p>Your artwork is made carefully and prepared with a premium personal feel.</p>
  </div>
</div>
```

## Add a fifth step

Paste this inside the timeline:

```html
<div class="step reveal">
  <div class="number">05</div>
  <h3>Gift moment</h3>
  <p>Give them something that feels made from their story, not picked randomly.</p>
</div>
```

If you add 5 steps, update CSS:

Search:

```css
.timeline {
```

If it says:

```css
grid-template-columns: repeat(4, 1fr);
```

Change to:

```css
grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
```

---

# 26. How To Edit Artwork Ideas Cards

Search:

```html
choice-grid
```

You will see cards like:

```html
<div class="choice-card reveal">
  <div class="icon-pill">👤</div>
  <h3>Single portrait</h3>
  <p>Clean, elegant, and perfect when one face carries the whole memory.</p>
</div>
```

## Better options

```html
<div class="choice-card reveal">
  <div class="icon-pill">👤</div>
  <h3>Single portrait</h3>
  <p>Clean, elegant, and perfect when one face carries the whole memory.</p>
</div>

<div class="choice-card reveal">
  <div class="icon-pill">♥</div>
  <h3>Couple portrait</h3>
  <p>Made for anniversaries, birthdays, love stories, and heart-shape concepts.</p>
</div>

<div class="choice-card reveal">
  <div class="icon-pill">👨‍👩‍👧</div>
  <h3>Family artwork</h3>
  <p>For parents, siblings, grandparents, or a photo that deserves permanence.</p>
</div>

<div class="choice-card reveal">
  <div class="icon-pill">🐾</div>
  <h3>Pet portrait</h3>
  <p>For the pet that made the house warmer and the photos better.</p>
</div>
```

## Add logo artwork idea

```html
<div class="choice-card reveal">
  <div class="icon-pill">◆</div>
  <h3>Logo artwork</h3>
  <p>For studios, cafes, rooms, business gifts, or brand decor with personality.</p>
</div>
```

---

# 27. How To Edit Gallery Preview Cards

Search:

```html
gallery-showcase
```

You will see:

```html
<div class="gallery-card" style="--img: linear-gradient(135deg, #3a2923, #b08968);">
  <small>Signature piece</small>
  <h3>Couple memory portrait</h3>
  <p>A romantic portrait concept for anniversaries, birthdays, and gifts that need to feel personal.</p>
</div>
```

Right now these are gradient placeholders.

## Replace gradient with real image

Put your image in the same folder:

```txt
couple-art.jpg
```

Change:

```html
style="--img: linear-gradient(135deg, #3a2923, #b08968);"
```

to:

```html
style="--img: url('couple-art.jpg');"
```

Full example:

```html
<div class="gallery-card" style="--img: url('couple-art.jpg');">
  <small>Signature piece</small>
  <h3>Couple memory portrait</h3>
  <p>A romantic portrait concept for anniversaries, birthdays, and gifts that need to feel personal.</p>
</div>
```

## Add more gallery cards

Copy this:

```html
<div class="gallery-card reveal" style="--img: url('your-image.jpg');">
  <small>Category label</small>
  <h3>Your artwork title</h3>
  <p>Short emotional description of this artwork idea.</p>
</div>
```

Paste inside either:

```html
<div class="gallery-stack">
```

or create a new layout section.

---

# 28. How To Make Gallery Images Brighter Or Darker

Search:

```css
.gallery-card::after
```

You will see:

```css
background:
  linear-gradient(180deg, rgba(47,36,32,0.05), rgba(47,36,32,0.70)),
  var(--img);
```

This overlay makes text readable.

## Make image lighter

Change:

```css
rgba(47,36,32,0.70)
```

to:

```css
rgba(47,36,32,0.52)
```

## Make image darker

Change:

```css
rgba(47,36,32,0.70)
```

to:

```css
rgba(47,36,32,0.80)
```

Do not remove the overlay completely, or white text may become unreadable.

---

# 29. How To Edit Comparison Section

Search:

```html
comparison-wrap
```

You will see two cards:

```html
<div class="compare-card normal reveal">
  <h3>Normal gift</h3>
  <ul>
    <li><span>•</span> Often chosen quickly because the date is close.</li>
  </ul>
</div>

<div class="compare-card premium reveal">
  <h3>Handmade memory</h3>
  <ul>
    <li><span>•</span> Built from a real photo and a real story.</li>
  </ul>
</div>
```

## Better version

```html
<div class="comparison-wrap">
  <div class="compare-card normal reveal">
    <h3>Normal gift</h3>
    <ul>
      <li><span>•</span> Often chosen quickly because the date is close.</li>
      <li><span>•</span> Useful maybe, but not always emotional.</li>
      <li><span>•</span> Can feel generic if it is not connected to a memory.</li>
      <li><span>•</span> Easy to forget once the moment passes.</li>
    </ul>
  </div>

  <div class="compare-card premium reveal">
    <h3>Handmade memory</h3>
    <ul>
      <li><span>•</span> Built from a real photo and a real story.</li>
      <li><span>•</span> Feels personal before they even open it.</li>
      <li><span>•</span> Stays visible on a wall, shelf, or room corner.</li>
      <li><span>•</span> Makes the gift-giver look thoughtful, not random.</li>
    </ul>
  </div>
</div>
```

The right card looks premium because it has:

```html
premium
```

---

# 30. How To Edit Final CTA

Search:

```html
final-cta
```

You will see:

```html
<section class="final-cta reveal">
  <div class="final-cta-inner">
    <span class="section-kicker" style="color:#f3d6b5;">Reserve your artwork</span>
    <h2>The photo is already in your gallery. Let’s turn it into something they can keep.</h2>
    <p>
      Start with the order form, choose the basic details, and send your request on WhatsApp.
    </p>
    <a href="order.html" class="btn btn-primary">Create Yours Now →</a>
    <div class="cta-note">Best for birthdays, anniversaries, farewell gifts, couple gifts, family memories, and pet portraits.</div>
  </div>
</section>
```

## Better final CTA copy

```html
<section class="final-cta reveal">
  <div class="final-cta-inner">
    <span class="section-kicker" style="color:#f3d6b5;">Reserve your artwork</span>
    <h2>The photo is already in your gallery. Let’s turn it into something they can keep.</h2>
    <p>
      Start with the order form, choose the basic details, and send your request on WhatsApp. If you are confused about photo, size, or style, I’ll guide you personally.
    </p>
    <a href="order.html" class="btn btn-primary">Create Yours Now →</a>
    <div class="cta-note">Best for birthdays, anniversaries, farewell gifts, couple gifts, family memories, and pet portraits.</div>
  </div>
</section>
```

## More aggressive CTA

```html
<h2>If this gift matters, don’t make it feel last-minute.</h2>
<p>
  Reserve your custom artwork slot now and I’ll help you choose the right photo, size, and style before starting.
</p>
<a href="order.html" class="btn btn-primary">Reserve My Slot →</a>
```

---

# 31. How To Edit Footer

Search:

```html
premium-footer
```

You will see:

```html
<footer class="premium-footer">
  <div class="footer-inner">
    <div class="footer-logo-space">
      <img src="logo.png" alt="MalayPaul Arts Logo" />
    </div>

    <h2 class="footer-brand">MalayPaul Arts</h2>

    <p class="footer-text">
      Premium handmade string art portraits crafted for memories, gifts, love stories, pets, families, and moments worth keeping forever.
    </p>

    <div class="footer-links">
      <a href="index.html">Home</a>
      <a href="order.html">Order</a>
      <a href="gallery.html">Gallery</a>
      <a href="contact.html">Contact</a>
    </div>

    <div class="footer-bottom">
      <p>© 2026 MalayPaul Arts. All rights reserved.</p>
      <p class="footer-note">Handcrafted with care in India</p>
    </div>
  </div>
</footer>
```

## Change footer text

```html
<p class="footer-text">
  Premium handmade string art portraits crafted for memories, gifts, love stories, pets, families, and moments worth keeping forever.
</p>
```

Better:

```html
<p class="footer-text">
  Custom handmade string art portraits crafted for memories, gifts, love stories, pets, families, and moments worth keeping close.
</p>
```

## Change footer note

```html
<p class="footer-note">Handcrafted with care in India</p>
```

Options:

```html
<p class="footer-note">Made slowly. Gifted forever.</p>
```

```html
<p class="footer-note">Handmade with patience in India</p>
```

```html
<p class="footer-note">Crafted for memories worth keeping</p>
```

---

# 32. How To Edit Mobile Sticky CTA

Search:

```html
mobile-sticky-cta
```

You will see:

```html
<a class="mobile-sticky-cta" href="order.html">Reserve Your Artwork Slot →</a>
```

Change text:

```html
<a class="mobile-sticky-cta" href="order.html">Create Your Artwork →</a>
```

or:

```html
<a class="mobile-sticky-cta" href="order.html">Reserve Slot Before It’s Late →</a>
```

Keep it short because it appears on mobile bottom screen.

## Hide mobile sticky CTA

Search CSS:

```css
.mobile-sticky-cta {
```

To hide it completely, change:

```css
display: inline-flex;
```

to:

```css
display: none;
```

But I recommend keeping it because it helps conversions.

---

# 33. How To Add A New Section

Copy this basic section structure:

```html
<section class="section">
  <div class="section-head reveal">
    <span class="section-kicker">Your small label</span>
    <h2>Your main section headline.</h2>
    <p class="section-subtitle">
      Your short paragraph that explains the section.
    </p>
  </div>

  <div class="premium-grid">
    <div class="premium-card reveal">
      <div class="mini-label">01 / Detail</div>
      <h3>Card title</h3>
      <p>Card description goes here.</p>
    </div>

    <div class="premium-card featured reveal">
      <div class="mini-label">02 / Premium</div>
      <h3>Featured card title</h3>
      <p>Featured card description goes here.</p>
    </div>

    <div class="premium-card reveal">
      <div class="mini-label">03 / Trust</div>
      <h3>Card title</h3>
      <p>Card description goes here.</p>
    </div>
  </div>
</section>
```

Place it before final CTA if you want it near the bottom.

---

# 34. New Section Idea: Customer Reactions

Add this before final CTA:

```html
<section class="section">
  <div class="section-head reveal">
    <span class="section-kicker">What it feels like</span>
    <h2>The reaction is the real gift.</h2>
    <p class="section-subtitle">
      A handmade artwork does not just decorate a room. It reminds them who thought of them, what the photo means, and why that moment mattered.
    </p>
  </div>

  <div class="proof-row">
    <div class="proof-card reveal">
      <strong>Pause</strong>
      <h3>They notice it</h3>
      <p>It feels different from a normal gift because it is clearly made from their own memory.</p>
    </div>

    <div class="proof-card reveal">
      <strong>Smile</strong>
      <h3>They feel it</h3>
      <p>The personal photo, name, date, or story makes the moment more emotional.</p>
    </div>

    <div class="proof-card reveal">
      <strong>Keep</strong>
      <h3>They remember it</h3>
      <p>It stays visible long after the birthday, anniversary, farewell, or special day ends.</p>
    </div>
  </div>
</section>
```

---

# 35. New Section Idea: Photo Guidance

Add this before process timeline:

```html
<section class="section">
  <div class="section-head reveal">
    <span class="section-kicker">Photo guidance</span>
    <h2>Not every good photo becomes good string art.</h2>
    <p class="section-subtitle">
      That is why I help you choose the right photo before starting, so the final artwork looks clean, balanced, and premium.
    </p>
  </div>

  <div class="premium-grid">
    <div class="premium-card reveal">
      <div class="mini-label">01 / Clear face</div>
      <h3>Good lighting matters</h3>
      <p>Photos with visible facial details usually become cleaner and more premium-looking artworks.</p>
    </div>

    <div class="premium-card featured reveal">
      <div class="mini-label">02 / Better angle</div>
      <h3>I help you choose</h3>
      <p>Send 2-3 photo options and I’ll guide you on which one will work best before starting.</p>
    </div>

    <div class="premium-card reveal">
      <div class="mini-label">03 / Final feel</div>
      <h3>Details make it personal</h3>
      <p>Names, dates, quotes, heart shapes, pet details, and custom ideas can make the gift more emotional.</p>
    </div>
  </div>
</section>
```

---

# 36. How To Remove A Section

A section usually starts with:

```html
<section class="section">
```

or:

```html
<section class="final-cta reveal">
```

and ends with:

```html
</section>
```

To remove a section, delete from the opening `<section...>` to the matching closing `</section>`.

Do not delete only half of the section.

Tip: Click near `<section`, then use VS Code bracket/indent guides to find the end.

---

# 37. How To Change Animations

Search:

```css
.reveal {
```

You will see:

```css
.reveal {
  opacity: 0;
  transform: translateY(26px);
  transition: opacity 0.75s ease, transform 0.75s ease;
}

.reveal.show {
  opacity: 1;
  transform: translateY(0);
}
```

## Make reveal animation slower

```css
transition: opacity 1s ease, transform 1s ease;
```

## Make reveal movement stronger

```css
transform: translateY(40px);
```

## Make animation subtle

```css
transform: translateY(14px);
transition: opacity 0.55s ease, transform 0.55s ease;
```

---

# 38. How Reveal Animation Works

Search:

```js
revealObserver
```

You will see JavaScript like:

```js
const revealItems = document.querySelectorAll('.reveal');

if ('IntersectionObserver' in window) {
  const revealObserver = new IntersectionObserver(function(entries) {
    entries.forEach(function(entry) {
      if (entry.isIntersecting) {
        entry.target.classList.add('show');
        revealObserver.unobserve(entry.target);
      }
    });
  }, {
    threshold: 0.14,
    rootMargin: '0px 0px -40px 0px'
  });

  revealItems.forEach(function(item) {
    revealObserver.observe(item);
  });
}
```

This means:

- Every element with `class="reveal"` starts hidden
- When customer scrolls to it, JS adds `show`
- CSS animates it into view

If a new card is not animating, make sure it has:

```html
class="reveal"
```

or:

```html
class="premium-card reveal"
```

---

# 39. How To Edit Mouse Glow Effect

Search:

```js
pointermove
```

You will see:

```js
window.addEventListener('pointermove', function(event) {
  if (window.matchMedia('(max-width: 980px)').matches) return;
  if (!ticking) {
    window.requestAnimationFrame(function() {
      document.documentElement.style.setProperty('--mx', event.clientX + 'px');
      document.documentElement.style.setProperty('--my', event.clientY + 'px');
      ticking = false;
    });
    ticking = true;
  }
});
```

This controls the soft glow that follows the mouse on laptop.

The glow is controlled by:

```css
body::after {
  background:
    radial-gradient(circle at var(--mx, 50%) var(--my, 22%), rgba(255,255,255,0.38), transparent 25%);
}
```

## Make glow stronger

```css
rgba(255,255,255,0.52)
```

## Make glow softer

```css
rgba(255,255,255,0.24)
```

## Make glow bigger

Change:

```css
transparent 25%
```

to:

```css
transparent 34%
```

---

# 40. How Mobile Menu Works

The navbar uses:

```js
const body = document.body;
const menu = document.getElementById('menu');
const hamburger = document.getElementById('hamburger');
const mobileBackdrop = document.getElementById('mobileBackdrop');
```

Opening menu adds:

```js
body.classList.add('menu-open');
```

Closing menu removes:

```js
body.classList.remove('menu-open');
```

The CSS watches for:

```css
body.menu-open .menu {
  opacity: 1;
  transform: translateY(0) scale(1);
  pointer-events: auto;
}
```

Do not remove:

```html
id="menu"
id="hamburger"
id="mobileBackdrop"
```

JavaScript needs them.

---

# 41. How To Change Mobile Breakpoints

Search:

```css
@media (max-width: 980px)
```

This controls tablet/mobile layout.

Search:

```css
@media (max-width: 540px)
```

This controls small phone layout.

## Example: make mobile menu start earlier

Change:

```css
@media (max-width: 980px)
```

to:

```css
@media (max-width: 1050px)
```

This makes the hamburger menu appear on slightly bigger screens.

---

# 42. How To Make Hero Section Smaller

Search:

```css
.hero {
```

You will see:

```css
.hero {
  min-height: calc(100svh - var(--nav-h));
  padding: 58px max(22px, 6vw) 70px;
}
```

Make it shorter:

```css
.hero {
  min-height: auto;
  padding: 48px max(22px, 6vw) 56px;
}
```

Use this if the hero feels too tall.

---

# 43. How To Make Sections Closer Together

Search:

```css
.section {
```

You will see:

```css
.section {
  padding: 92px max(22px, 6vw);
}
```

Reduce spacing:

```css
.section {
  padding: 72px max(22px, 6vw);
}
```

For mobile, search inside:

```css
@media (max-width: 980px)
```

You may see:

```css
.section {
  padding: 72px 22px;
}
```

Change to:

```css
.section {
  padding: 58px 22px;
}
```

---

# 44. How To Make Cards More Premium

Most cards share this styling:

```css
.emotion-card,
.premium-card,
.step,
.gallery-card,
.choice-card,
.faq-card,
.proof-card {
  background:
    linear-gradient(135deg, rgba(255,250,243,0.88), rgba(255,250,243,0.58));
  border: 1.5px solid rgba(229,207,185,0.86);
  border-radius: var(--radius-lg);
  box-shadow:
    var(--shadow-soft),
    inset 0 1px 0 rgba(255,255,255,0.68);
}
```

## Make cards softer

```css
box-shadow:
  0 18px 42px rgba(62,47,47,0.08),
  inset 0 1px 0 rgba(255,255,255,0.68);
```

## Make cards more premium / lifted

```css
box-shadow:
  0 28px 70px rgba(62,47,47,0.14),
  inset 0 1px 0 rgba(255,255,255,0.72);
```

## Make cards rounder

Change:

```css
border-radius: var(--radius-lg);
```

to:

```css
border-radius: 34px;
```

---

# 45. How To Change Button Style

Search:

```css
.btn-primary {
```

You will see:

```css
.btn-primary {
  background: linear-gradient(135deg, var(--gold), var(--gold-dark));
  color: white;
  box-shadow: 0 22px 52px rgba(143,95,59,0.30);
}
```

Darker luxury button:

```css
.btn-primary {
  background: linear-gradient(135deg, var(--deep), var(--gold-dark));
  color: white;
  box-shadow: 0 22px 52px rgba(47,36,32,0.28);
}
```

More golden button:

```css
.btn-primary {
  background: linear-gradient(135deg, var(--gold-light), var(--gold), var(--gold-dark));
  color: white;
  box-shadow: 0 22px 52px rgba(143,95,59,0.30);
}
```

---

# 46. How To Add WhatsApp Direct Button

You can add this anywhere:

```html
<a href="https://wa.me/918087827454?text=Hi%20MalayPaul%20Arts%20I%20want%20to%20create%20a%20custom%20string%20art" target="_blank" class="btn btn-primary">
  Message on WhatsApp →
</a>
```

Change the number here:

```txt
918087827454
```

Format:

- Country code first
- No plus
- No spaces

Correct:

```txt
919876543210
```

Wrong:

```txt
+91 98765 43210
```

---

# 47. How To Make All Buttons Go To Order Page

Search:

```html
href="order.html"
```

These links go to the order page:

```html
<a href="order.html" class="btn btn-primary">Start Your Artwork →</a>
<a href="order.html" class="nav-cta">Reserve Slot</a>
<a class="mobile-sticky-cta" href="order.html">Reserve Your Artwork Slot →</a>
```

If your order page has another filename, change all `order.html`.

Example:

```html
href="reserve.html"
```

---

# 48. How To Fix Broken Images

If image does not show:

Check file name.

These are different:

```txt
logo.png
Logo.png
LOGO.png
logo.PNG
```

On hosting, letter case matters.

If your code says:

```html
<img src="logo.png">
```

Then file must be exactly:

```txt
logo.png
```

Same folder rule:

```txt
project-folder/
  index.html
  logo.png
  hero-artwork.jpg
```

If images are in an images folder:

```txt
project-folder/
  index.html
  images/
    logo.png
```

Then code should be:

```html
<img src="images/logo.png">
```

---

# 49. Best Home Page Copy Setup

Use this if you want the page to feel extra premium and emotional.

## Hero

```html
<div class="eyebrow"><span class="dot"></span> Handmade string art crafted from real memories</div>
<h1>Some photos deserve more than a <span>scroll.</span></h1>
<p class="hero-text">
  Turn one meaningful photo into a handmade string art piece that feels personal, emotional, and impossible to ignore. I help you choose the right photo, size, and idea before starting.
</p>
```

## Hero buttons

```html
<a href="order.html" class="btn btn-primary">Reserve Your Artwork →</a>
<a href="gallery.html" class="btn btn-soft">View Gallery</a>
```

## Trust badges

```html
<div class="micro-trust">
  <span>Photo guidance included</span>
  <span>Gift-ready planning</span>
  <span>Limited handmade slots</span>
</div>
```

## First emotional section

```html
<h2>They already have things. Give them a memory.</h2>
<p>
  A normal gift is used for a few days. A personal artwork becomes part of their room, their wall, and their story.
</p>
```

## Final CTA

```html
<h2>If this gift matters, don’t make it feel last-minute.</h2>
<p>
  Start with the order form, send your photo, and I’ll guide you personally on the best size, style, and design direction.
</p>
<a href="order.html" class="btn btn-primary">Reserve My Slot →</a>
```

---

# 50. Testing Checklist After Editing

After every edit:

```txt
Ctrl + S
```

Then refresh browser.

Check:

- [ ] Navbar logo appears
- [ ] Navbar links work
- [ ] Active page highlight works
- [ ] Hero headline looks good
- [ ] Hero buttons go to correct pages
- [ ] Hero image loads
- [ ] Floating cards are not overlapping badly
- [ ] Trust badges are not too long
- [ ] All sections have correct spacing
- [ ] Gallery images load
- [ ] Final CTA button works
- [ ] Footer links work
- [ ] Mobile hamburger opens
- [ ] Mobile hamburger closes
- [ ] Mobile sticky CTA works
- [ ] No horizontal scrolling on phone
- [ ] Reveal animations work
- [ ] Page still feels premium, not crowded

---

# 51. Common Problems And Fixes

## Problem: Logo not showing

Check:

```html
<img src="logo.png">
```

Your file must be exactly:

```txt
logo.png
```

Same folder.

---

## Problem: Button does nothing

Check if `href` exists:

```html
<a href="order.html" class="btn btn-primary">Create Yours Now →</a>
```

If `href=""` is empty, it will not go anywhere.

---

## Problem: Mobile menu does not open

Check these IDs exist:

```html
<div class="menu" id="menu">
<button class="hamburger" id="hamburger">
<div class="mobile-backdrop" id="mobileBackdrop"></div>
```

And script exists:

```js
hamburger.addEventListener('click', function() {
  body.classList.contains('menu-open') ? closeMenu() : openMenu();
});
```

---

## Problem: New card does not animate

Add `reveal`.

Wrong:

```html
<div class="premium-card">
```

Correct:

```html
<div class="premium-card reveal">
```

---

## Problem: Gallery image too dark

Search:

```css
.gallery-card::after
```

Change overlay opacity lower:

```css
rgba(47,36,32,0.52)
```

---

## Problem: Text looks cramped on mobile

Search:

```css
@media (max-width: 540px)
```

Reduce font sizes or spacing there.

Example:

```css
.hero h1 {
  font-size: 40px;
}
```

---

# 52. Editing Workflow I Recommend

Do not edit everything at once.

Use this workflow:

```txt
1. Change one section
2. Save
3. Refresh browser
4. Check desktop
5. Check mobile
6. Then edit next section
```

This way if something breaks, you know exactly what caused it.

---

# 53. Simple Mental Model Of This Page

Think of the home page like this:

```txt
Navbar
  ↓
Hero section
  ↓
Emotional reason to care
  ↓
Premium difference
  ↓
Scarcity / FOMO
  ↓
Simple process
  ↓
Artwork ideas
  ↓
Gallery preview
  ↓
Normal gift vs handmade memory
  ↓
Final CTA
  ↓
Footer
```

The page is not just showing art.

It is selling this feeling:

```txt
“This is not a random gift. This is their memory, made permanent.”
```

Keep that feeling in every line you edit.
