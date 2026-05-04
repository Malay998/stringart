# MalayPaul Arts — Contact Page Editing Guide

> Best file name: `CONTACT_PAGE_EDITING_GUIDE.md`  
> Keep this file in your website folder beside `contact.html`.

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

This is a Markdown file, so all the HTML, CSS, and JavaScript blocks will look colourful in VS Code preview.

---

# 1. What This Contact Page Controls

Your contact page controls:

- Contact page hero
- WhatsApp direct buttons
- Contact guidance card
- Premium strip cards
- Contact info panel
- WhatsApp form
- Quick message chips
- Form fields
- Occasion dropdown
- Live WhatsApp preview
- Character count
- Submit-to-WhatsApp logic
- FAQ accordion
- Final CTA
- Floating WhatsApp button
- Footer
- Navbar active state
- Mobile menu
- Reveal animations
- Mouse glow effect

This page is usually saved as:

```txt
contact.html
```

---

# 2. Quick Search Cheat Sheet

Use `Ctrl + F` in VS Code.

| What You Want To Edit | Search This |
|---|---|
| Browser tab title | `<title>` |
| Colours | `:root` |
| Navbar | `<nav class="navbar"` |
| Logo | `logo.png` |
| Page identity | `body data-page="contact"` |
| Hero section | `hero-shell` |
| Hero badge | `Private Artwork Guidance` |
| Hero headline | `gift they remember` |
| Hero WhatsApp button | `Start on WhatsApp` |
| Hero visual card | `lux-card` |
| Visual checklist | `visual-row` |
| Availability card | `availability-card` |
| Premium strip cards | `premium-strip` |
| Main contact form | `id="contact-form"` |
| Info panel | `info-panel` |
| Form panel | `form-panel` |
| Quick chips | `quick-chip` |
| WhatsApp form | `whatsappForm` |
| Name field | `id="name"` |
| Phone field | `id="phone"` |
| Email field | `id="email"` |
| Occasion field | `id="occasion"` |
| Message field | `id="message"` |
| Live preview | `previewText` |
| Character count | `charCount` |
| WhatsApp number | `phoneNumber` |
| Preview function | `updatePreview()` |
| FAQ section | `faq-wrap` |
| FAQ item | `faq-item` |
| FAQ toggle | `toggleFaq` |
| Final CTA | `final-cta` |
| Floating WhatsApp CTA | `floatingCta` |
| Footer | `premium-footer` |
| Reveal animation | `IntersectionObserver` |
| Mobile menu | `menu-open` |

---

# 3. Before Editing Anything

Always make a backup first.

In your website folder:

1. Right-click `contact.html`
2. Copy
3. Paste
4. Rename the copy:

```txt
contact-backup.html
```

Now edit only:

```txt
contact.html
```

If something breaks, open the backup and copy the working part back.

---

# 4. The Most Important Rule

The contact page is mainly powered by this chain:

```txt
Customer fills form
        ↓
updatePreview() creates live WhatsApp preview
        ↓
Customer clicks Send
        ↓
whatsappForm submit event runs
        ↓
JavaScript creates final WhatsApp message
        ↓
window.open() opens WhatsApp
```

So when editing form-related stuff, do **not randomly rename IDs** like:

```html
id="name"
id="phone"
id="email"
id="occasion"
id="message"
id="previewText"
id="charCount"
```

JavaScript depends on those IDs.

---

# 5. How To Change Browser Tab Title

Search:

```html
<title>
```

You will see:

```html
<title>Contact - MalayPaul Arts</title>
```

Better options:

```html
<title>Contact MalayPaul Arts | Custom String Art Guidance</title>
```

```html
<title>MalayPaul Arts Contact | Handmade Artwork Help</title>
```

```html
<title>Contact | MalayPaul Arts Premium String Art</title>
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
  --card-soft: rgba(255,250,243,0.78);
  --text: #2f2420;
  --muted: #7a6258;
  --gold: #b08968;
  --gold-dark: #8f5f3b;
  --line: #e8d7c4;
  --dark: #2f2420;
  --dark-soft: #473228;
  --cream: #fffaf3;
  --green: #567c55;
}
```

## What these mean

| Variable | Meaning |
|---|---|
| `--bg` | Main page background |
| `--card` | Cream card colour |
| `--text` | Main dark text |
| `--muted` | Paragraph text |
| `--gold` | Premium gold |
| `--gold-dark` | Dark gold / brown |
| `--line` | Soft border colour |
| `--dark` | Dark luxury sections |
| `--green` | Available status dot |
| `--red` | Error/warning style |

## Safe premium palette

```css
:root {
  --bg: #f5f1ea;
  --card: #fffaf3;
  --card-soft: rgba(255,250,243,0.78);
  --text: #2f2420;
  --muted: #7a6258;
  --gold: #b08968;
  --gold-dark: #8f5f3b;
  --line: #e8d7c4;
  --dark: #2f2420;
  --dark-soft: #473228;
  --cream: #fffaf3;
  --green: #567c55;
  --red: #9c5c48;
}
```

Avoid bright neon colours. Your contact page should feel calm, premium, and trustworthy.

---

# 7. How To Change Logo

Search:

```html
logo.png
```

You will find:

```html
<img src="logo.png" alt="MalayPaul Arts Logo">
```

This appears in:

- Navbar
- Hero visual card
- Footer

## Easiest method

Put your logo file in the same folder as `contact.html` and name it:

```txt
logo.png
```

No code change needed.

## If your logo file has another name

Example:

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

Do it everywhere `logo.png` appears.

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

## Change visible name

Example:

```html
<a href="contact.html" class="nav-link" data-page="contact">Contact</a>
```

to:

```html
<a href="contact.html" class="nav-link" data-page="contact">Help</a>
```

## Change destination

Change the `href`.

```html
<a href="contact.html" class="nav-link" data-page="contact">Help</a>
```

## Do not break active highlight

Keep this:

```html
<body data-page="contact">
```

And keep this:

```html
data-page="contact"
```

Your active nav system uses those.

---

# 9. How To Change Navbar CTA

Search:

```html
Reserve Slot
```

You will see:

```html
<a href="order.html" class="nav-cta">Reserve Slot</a>
```

Change text:

```html
<a href="order.html" class="nav-cta">Start Order</a>
```

or:

```html
<a href="order.html" class="nav-cta">Create Yours</a>
```

Make it open WhatsApp directly:

```html
<a href="https://wa.me/918087827454?text=Hi%20MalayPaul%20Arts%20I%20want%20help%20with%20a%20custom%20artwork" target="_blank" class="nav-cta">WhatsApp Me</a>
```

---

# 10. How To Change The Main WhatsApp Number

Search:

```js
const phoneNumber
```

You will see:

```js
const phoneNumber = "918087827454";
```

Change only the number inside quotes.

Example:

```js
const phoneNumber = "919876543210";
```

Rules:

- Use country code
- No `+`
- No spaces
- No hyphen

Correct:

```js
const phoneNumber = "919876543210";
```

Wrong:

```js
const phoneNumber = "+91 98765 43210";
```

This number controls where the form sends the WhatsApp message.

---

# 11. How To Change Direct WhatsApp Links

Search:

```html
https://wa.me/918087827454
```

You may find direct buttons like:

```html
<a href="https://wa.me/918087827454?text=Hi%20MalayPaul%20Arts..." target="_blank" class="btn btn-primary">Start on WhatsApp →</a>
```

Change the number there too:

```html
https://wa.me/919876543210
```

## Important

Changing only this:

```js
const phoneNumber = "919876543210";
```

updates the form submit button.

But direct WhatsApp buttons with hardcoded links must also be changed manually.

Search and replace all:

```txt
918087827454
```

with your real number.

---

# 12. How To Edit Hero Section

Search:

```html
hero-shell
```

You will find:

```html
<span class="tag">Private Artwork Guidance</span>
<h1>Let’s turn your idea into a <span>gift they remember.</span></h1>
<p>
  Send your photo, occasion, or even a half-clear idea...
</p>
```

## Better hero options

```html
<span class="tag">Private Artwork Guidance</span>
<h1>Let’s turn your idea into a <span>gift they remember.</span></h1>
<p>
  Send your photo, occasion, or even a half-clear idea. I’ll help you choose the right artwork type, size, and gift plan before you place the final order.
</p>
```

```html
<span class="tag">Personal String Art Help</span>
<h1>Not sure what to order? I’ll help you choose.</h1>
<p>
  Share your photo, occasion, and idea. I’ll guide you on the best size, style, photo choice, and details before you confirm anything.
</p>
```

```html
<span class="tag">Custom Gift Guidance</span>
<h1>Start with one message. I’ll help shape the artwork.</h1>
<p>
  Whether it is a birthday, anniversary, pet memory, family gift, or custom logo, I’ll help you turn the idea into something clear and premium.
</p>
```

---

# 13. How To Edit Hero Buttons

Search:

```html
hero-actions
```

You will see:

```html
<div class="hero-actions">
  <a href="https://wa.me/918087827454?text=..." target="_blank" class="btn btn-primary">Start on WhatsApp →</a>
  <a href="#contact-form" class="btn btn-soft">Write a guided message</a>
</div>
```

## Change primary button

```html
<a href="https://wa.me/918087827454?text=..." target="_blank" class="btn btn-primary">Start on WhatsApp →</a>
```

Options:

```html
Start on WhatsApp →
```

```html
Get Photo Guidance →
```

```html
Ask Before Ordering →
```

```html
Message MalayPaul Arts →
```

## Change secondary button

```html
<a href="#contact-form" class="btn btn-soft">Write a guided message</a>
```

Options:

```html
Write a Guided Message
```

```html
Use Contact Form
```

```html
Send Details Properly
```

Keep:

```html
href="#contact-form"
```

That scrolls to the form.

---

# 14. How To Edit Hero Meta Pills

Search:

```html
hero-meta
```

You will see:

```html
<div class="hero-meta">
  <div class="meta-pill">✦ Photo guidance included</div>
  <div class="meta-pill">✦ Gift-ready planning</div>
  <div class="meta-pill">✦ Limited handmade slots</div>
</div>
```

Better options:

```html
<div class="hero-meta">
  <div class="meta-pill">✦ Photo selection help</div>
  <div class="meta-pill">✦ Size and style guidance</div>
  <div class="meta-pill">✦ Handmade slot planning</div>
</div>
```

or:

```html
<div class="hero-meta">
  <div class="meta-pill">✦ WhatsApp guidance</div>
  <div class="meta-pill">✦ Gift timeline support</div>
  <div class="meta-pill">✦ Custom concept help</div>
</div>
```

Keep each pill short.

---

# 15. How To Edit Hero Visual Card

Search:

```html
lux-card
```

Inside it you will see:

```html
<span>MalayPaul Arts Concierge</span>
<h3>Tell me the memory. I’ll help shape the artwork.</h3>
```

Better options:

```html
<span>MalayPaul Arts Concierge</span>
<h3>Tell me the memory. I’ll help shape the artwork.</h3>
```

```html
<span>Personal Artwork Help</span>
<h3>Send the idea. I’ll help make it clear.</h3>
```

```html
<span>Before You Order</span>
<h3>Choose the right photo, size, and style first.</h3>
```

---

# 16. How To Edit Visual Checklist Rows

Search:

```html
visual-row
```

You will see rows like:

```html
<div class="visual-row">
  <div class="visual-icon">📸</div>
  <div>
    <b>Send your best photo</b>
    <small>Not sure which one? Send 2-3 and I’ll help.</small>
  </div>
</div>
```

Better version:

```html
<div class="visual-row">
  <div class="visual-icon">📸</div>
  <div>
    <b>Send photo options</b>
    <small>Not sure which one works? Send 2-3 and I’ll help choose.</small>
  </div>
</div>

<div class="visual-row">
  <div class="visual-icon">🎁</div>
  <div>
    <b>Tell me the occasion</b>
    <small>Birthday, anniversary, farewell, parents, pet memory, or surprise gift.</small>
  </div>
</div>

<div class="visual-row">
  <div class="visual-icon">✨</div>
  <div>
    <b>Get personal guidance</b>
    <small>I’ll suggest the cleanest size, style, and details.</small>
  </div>
</div>
```

---

# 17. How To Edit Availability Card

Search:

```html
availability-card
```

You will see:

```html
<div class="availability-card">
  <b><span class="pulse-dot"></span> Accepting custom requests</b>
  <p>Handmade orders are limited so every piece gets proper attention.</p>
</div>
```

Options:

```html
<div class="availability-card">
  <b><span class="pulse-dot"></span> Custom slots open</b>
  <p>Message early if this is for a birthday, anniversary, or surprise gift.</p>
</div>
```

```html
<div class="availability-card">
  <b><span class="pulse-dot"></span> Taking limited orders</b>
  <p>I keep slots limited so each artwork gets proper time and attention.</p>
</div>
```

The green pulsing dot is:

```html
<span class="pulse-dot"></span>
```

Keep it if you want the “available now” feeling.

---

# 18. How To Edit Floating Note

Search:

```html
Before you order
```

You will see:

```html
<div class="floating-note">
  <strong>Before you order</strong>
  <span>A quick WhatsApp chat can save you from choosing the wrong photo or size.</span>
</div>
```

Better options:

```html
<div class="floating-note">
  <strong>Before you order</strong>
  <span>Send your photo first. I’ll guide you if another one will look cleaner.</span>
</div>
```

```html
<div class="floating-note">
  <strong>Small guidance. Better artwork.</strong>
  <span>Choosing the right photo and size makes the final piece feel more premium.</span>
</div>
```

Keep it short, because this card is small.

---

# 19. How To Edit Premium Strip Cards

Search:

```html
premium-strip
```

You will see four cards:

```html
<div class="strip-card">
  <strong>Photo Selection Help</strong>
  <span>Send multiple photos and I’ll help pick the one that will look most premium.</span>
</div>
```

Better setup:

```html
<div class="premium-strip">
  <div class="strip-card">
    <strong>Photo Selection Help</strong>
    <span>Send multiple photos and I’ll help pick the one that will look most premium.</span>
  </div>

  <div class="strip-card">
    <strong>Gift Timeline</strong>
    <span>I’ll guide you early so your handmade order does not feel rushed later.</span>
  </div>

  <div class="strip-card">
    <strong>Style Direction</strong>
    <span>Portrait, couple, pet, family, text, logo, or custom concept — we decide cleanly.</span>
  </div>

  <div class="strip-card">
    <strong>Direct WhatsApp</strong>
    <span>No cold forms. Your request reaches me personally with all details ready.</span>
  </div>
</div>
```

---

# 20. How To Edit Main Contact Section Heading

Search:

```html
Start with the right message
```

You will see:

```html
<h2>Start with the right message</h2>
<p>
  Choose what you need, fill the details, and it will open WhatsApp with a clean premium message already prepared.
</p>
```

Better options:

```html
<h2>Start with the right message</h2>
<p>
  Choose what you need, add your details, and the page will prepare a clean WhatsApp message for you.
</p>
```

```html
<h2>Tell me what you’re planning</h2>
<p>
  The form helps you explain your photo, occasion, and artwork idea clearly before it opens WhatsApp.
</p>
```

```html
<h2>Send the details without overthinking it</h2>
<p>
  Use the guided form below and I’ll receive a clean message with your name, occasion, and artwork idea.
</p>
```

---

# 21. How To Edit Info Panel

Search:

```html
info-panel
```

Inside it you will find:

```html
<section class="info-panel">
```

The info panel is the dark left card in the contact section.

It usually includes:

- Contact heading
- Contact paragraph
- WhatsApp info
- Instagram info
- Email or location info
- Availability status
- Action buttons

Change text carefully, but keep class names.

---

# 22. How To Edit Contact Info Boxes

Search:

```html
info-box
```

You will see boxes like:

```html
<div class="info-box">
  <strong>WhatsApp</strong>
  <a href="https://wa.me/918087827454">+91 80878 27454</a>
</div>
```

## WhatsApp box example

```html
<div class="info-box">
  <strong>💬 WhatsApp</strong>
  <a href="https://wa.me/918087827454" target="_blank">+91 80878 27454</a>
</div>
```

Change number in both:

```html
href="https://wa.me/919876543210"
```

and visible text:

```html
+91 98765 43210
```

## Instagram box example

```html
<div class="info-box">
  <strong>📸 Instagram</strong>
  <a href="https://instagram.com/yourusername" target="_blank">@yourusername</a>
</div>
```

## Email box example

```html
<div class="info-box">
  <strong>✉ Email</strong>
  <a href="mailto:yourmail@gmail.com">yourmail@gmail.com</a>
</div>
```

---

# 23. How To Edit Info Action Buttons

Search:

```html
info-actions
```

You may see buttons like:

```html
<div class="info-actions">
  <a href="https://wa.me/918087827454" target="_blank" class="btn whatsapp">Message on WhatsApp</a>
  <a href="https://instagram.com/yourusername" target="_blank" class="btn instagram">Open Instagram</a>
</div>
```

Change WhatsApp number:

```html
https://wa.me/919876543210
```

Change Instagram link:

```html
https://instagram.com/malaypaularts
```

---

# 24. How To Edit The Form Fields

Search:

```html
<form
```

or:

```html
whatsappForm
```

You will see:

```html
<form id="whatsappForm">
```

Important IDs used by JavaScript:

```html
id="name"
id="phone"
id="email"
id="occasion"
id="message"
```

## Safe thing to edit

You can change placeholder text:

```html
<input id="name" type="text" placeholder="Your name">
```

to:

```html
<input id="name" type="text" placeholder="Your full name">
```

## Dangerous thing to edit

Do not change:

```html
id="name"
```

unless you also update JavaScript.

For example, if you change:

```html
id="name"
```

to:

```html
id="customerName"
```

then this JavaScript breaks:

```js
document.getElementById("name").value.trim();
```

---

# 25. How To Make A Field Required

Example:

```html
<input id="name" type="text" placeholder="Your name">
```

Make it required:

```html
<input id="name" type="text" placeholder="Your name" required>
```

Recommended required fields:

- Name
- Message / artwork idea

Optional fields:

- Phone
- Email
- Occasion

Your JavaScript already checks:

```js
if (name === "" || message === "") {
  alert("Please add your name and artwork idea before sending.");
  return;
}
```

So name and message are already required by logic.

---

# 26. How To Edit Occasion Dropdown

Search:

```html
id="occasion"
```

You may see:

```html
<select id="occasion" onchange="updatePreview()">
  <option>Birthday Gift</option>
  <option>Anniversary Gift</option>
  <option>Pet Memory</option>
</select>
```

Add new option:

```html
<option>Farewell Gift</option>
```

Better full setup:

```html
<select id="occasion" onchange="updatePreview()">
  <option>Birthday Gift</option>
  <option>Anniversary Gift</option>
  <option>Couple Gift</option>
  <option>Pet Memory</option>
  <option>Family Memory</option>
  <option>Logo / Brand Artwork</option>
  <option>Room Decor</option>
  <option>Farewell Gift</option>
  <option>Something Custom</option>
</select>
```

Keep:

```html
id="occasion"
onchange="updatePreview()"
```

---

# 27. How To Edit Quick Message Chips

Search:

```html
quick-chip
```

You will see buttons like:

```html
<button type="button" class="quick-chip" data-message="I want to create a custom portrait from a photo.">
  Portrait Help
  <span>For single face or personal portrait</span>
</button>
```

## What quick chips do

When customer clicks a quick chip:

1. It becomes active
2. It fills the message box with `data-message`
3. It updates the live preview
4. It focuses the message textarea

JavaScript:

```js
document.querySelectorAll(".quick-chip").forEach(function(chip) {
  chip.addEventListener("click", function() {
    document.querySelectorAll(".quick-chip").forEach(function(item) {
      item.classList.remove("active");
    });

    chip.classList.add("active");
    document.getElementById("message").value = chip.dataset.message;
    updatePreview();
    document.getElementById("message").focus();
  });
});
```

---

# 28. How To Add A New Quick Chip

Add inside the quick chip grid:

```html
<button type="button" class="quick-chip" data-message="I want to create a custom pet portrait. Please guide me with the best photo, size, and price.">
  Pet Portrait
  <span>For dog, cat, or pet memory</span>
</button>
```

More examples:

```html
<button type="button" class="quick-chip" data-message="I want to create a couple portrait for an anniversary gift. Please guide me with photo selection, size, and price.">
  Couple Gift
  <span>For anniversary or love story</span>
</button>

<button type="button" class="quick-chip" data-message="I want to create a family artwork from a photo. Please guide me with the best size and details.">
  Family Artwork
  <span>For parents, siblings, or grandparents</span>
</button>

<button type="button" class="quick-chip" data-message="I want to create a custom logo string art for decor or branding. Please guide me with size and pricing.">
  Logo Artwork
  <span>For brand, studio, or room decor</span>
</button>
```

## Important

Keep:

```html
type="button"
```

Without it, the chip may accidentally submit the form.

---

# 29. How To Change Quick Chip Layout

Search:

```css
.quick-grid
```

You may see:

```css
.quick-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
}
```

## 3 chips per row

```css
grid-template-columns: repeat(3, 1fr);
```

## 2 chips per row

```css
grid-template-columns: repeat(2, 1fr);
```

## Automatic layout

```css
grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
```

Recommended if you add many chips:

```css
.quick-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 12px;
  margin: 20px 0 22px;
}
```

---

# 30. How Live Preview Works

Search:

```js
function updatePreview()
```

You will see:

```js
function updatePreview() {
  const name = document.getElementById("name").value.trim();
  const phone = document.getElementById("phone").value.trim();
  const email = document.getElementById("email").value.trim();
  const occasion = document.getElementById("occasion").value;
  const message = document.getElementById("message").value.trim();
  const preview = document.getElementById("previewText");
  const charCount = document.getElementById("charCount");

  charCount.innerText = message.length + " chars";

  const whatsappMessage =
    "Hi MalayPaul Arts 👋\n\n" +
    "I am interested in a custom handmade artwork.\n\n" +
    "CUSTOMER DETAILS\n" +
    "Name: " + (name || "Not added yet") + "\n" +
    "WhatsApp Number: " + (phone || "Not added") + "\n" +
    "Email: " + (email || "Not provided") + "\n" +
    "Occasion: " + occasion + "\n\n" +
    "ARTWORK IDEA\n" +
    (message || "Not written yet") + "\n\n" +
    "Please guide me with the best photo, size, artwork style, price, and next steps.";

  preview.innerText = whatsappMessage;
}
```

This creates the message customers see before sending.

---

# 31. How To Edit Live Preview Message

Inside `updatePreview()`, change the message text.

Better version:

```js
const whatsappMessage =
  "Hi MalayPaul Arts 👋\n\n" +
  "I want guidance for a custom handmade string art piece.\n\n" +
  "CUSTOMER DETAILS\n" +
  "Name: " + (name || "Not added yet") + "\n" +
  "WhatsApp Number: " + (phone || "Not added") + "\n" +
  "Email: " + (email || "Not provided") + "\n" +
  "Occasion: " + occasion + "\n\n" +
  "ARTWORK IDEA\n" +
  (message || "Not written yet") + "\n\n" +
  "Please guide me with the best photo, size, artwork style, timeline, price, and next steps.";
```

Do not remove:

```js
+ name +
+ phone +
+ email +
+ occasion +
+ message +
```

Those insert customer details.

---

# 32. How Character Count Works

Search:

```js
charCount
```

You will see:

```js
charCount.innerText = message.length + " chars";
```

It displays how many characters are typed in the message box.

If you want a nicer text:

```js
charCount.innerText = message.length + " characters written";
```

If you do not want character count, hide it in HTML or CSS, but do not remove it from JavaScript unless you also remove the line above.

---

# 33. How To Make Preview Update While Typing

Inputs should have events like:

```html
oninput="updatePreview()"
```

Example:

```html
<input id="name" type="text" placeholder="Your name" oninput="updatePreview()">
```

Textarea:

```html
<textarea id="message" placeholder="Tell me your idea" oninput="updatePreview()"></textarea>
```

Dropdown:

```html
<select id="occasion" onchange="updatePreview()">
```

If the preview is not updating, check that these are present.

---

# 34. How Form Submit Works

Search:

```js
whatsappForm
```

You will see:

```js
document.getElementById("whatsappForm").addEventListener("submit", function(e) {
  e.preventDefault();

  const name = document.getElementById("name").value.trim();
  const phone = document.getElementById("phone").value.trim();
  const email = document.getElementById("email").value.trim();
  const occasion = document.getElementById("occasion").value;
  const message = document.getElementById("message").value.trim();

  if (name === "" || message === "") {
    alert("Please add your name and artwork idea before sending.");
    return;
  }

  const whatsappMessage =
    "Hi MalayPaul Arts 👋\n\n" +
    "I am interested in a custom handmade artwork.\n\n" +
    "CUSTOMER DETAILS\n" +
    "Name: " + name + "\n" +
    "WhatsApp Number: " + (phone || "Not provided") + "\n" +
    "Email: " + (email || "Not provided") + "\n" +
    "Occasion: " + occasion + "\n\n" +
    "ARTWORK IDEA\n" +
    message + "\n\n" +
    "Please guide me with the best photo, size, artwork style, price, and next steps.";

  const whatsappURL = "https://wa.me/" + phoneNumber + "?text=" + encodeURIComponent(whatsappMessage);
  window.open(whatsappURL, "_blank");
});
```

Meaning:

```txt
Form does not send email.
It creates a WhatsApp message and opens WhatsApp.
```

---

# 35. How To Change Required Alert

Search:

```js
Please add your name and artwork idea before sending.
```

You will see:

```js
alert("Please add your name and artwork idea before sending.");
```

Change to:

```js
alert("Please add your name and artwork idea first, bro.");
```

or more professional:

```js
alert("Please add your name and artwork idea before sending your request.");
```

---

# 36. How To Require Phone Number Too

Current check:

```js
if (name === "" || message === "") {
  alert("Please add your name and artwork idea before sending.");
  return;
}
```

If you want phone required too:

```js
if (name === "" || phone === "" || message === "") {
  alert("Please add your name, WhatsApp number, and artwork idea before sending.");
  return;
}
```

Also make the input required:

```html
<input id="phone" type="tel" placeholder="Your WhatsApp number" required oninput="updatePreview()">
```

---

# 37. How To Change Final WhatsApp Message

There are two WhatsApp messages:

## Message 1: Preview message

Inside:

```js
function updatePreview()
```

## Message 2: Actual sent message

Inside:

```js
document.getElementById("whatsappForm").addEventListener("submit", function(e) {
```

The actual sent message is the one that matters most.

Better actual message:

```js
const whatsappMessage =
  "Hi MalayPaul Arts 👋\n\n" +
  "I want to discuss a custom handmade string art order.\n\n" +
  "CUSTOMER DETAILS\n" +
  "Name: " + name + "\n" +
  "WhatsApp Number: " + (phone || "Not provided") + "\n" +
  "Email: " + (email || "Not provided") + "\n" +
  "Occasion: " + occasion + "\n\n" +
  "ARTWORK IDEA\n" +
  message + "\n\n" +
  "Please guide me with photo selection, size, artwork style, price, timeline, and next steps.";
```

Keep:

```js
encodeURIComponent(whatsappMessage)
```

This makes spaces and emojis work correctly in WhatsApp URL.

---

# 38. How To Add A New Field To The Form

Example: add budget field.

## Step 1: Add HTML field

Inside the form grid:

```html
<div class="input-group">
  <label class="floating-label" for="budget">Budget Range</label>
  <input id="budget" type="text" placeholder="Example: ₹1000 - ₹2000" oninput="updatePreview()">
</div>
```

## Step 2: Add it in updatePreview()

Add:

```js
const budget = document.getElementById("budget").value.trim();
```

Then add to preview message:

```js
"Budget: " + (budget || "Not provided") + "\n" +
```

Example:

```js
"CUSTOMER DETAILS\n" +
"Name: " + (name || "Not added yet") + "\n" +
"WhatsApp Number: " + (phone || "Not added") + "\n" +
"Email: " + (email || "Not provided") + "\n" +
"Occasion: " + occasion + "\n" +
"Budget: " + (budget || "Not provided") + "\n\n" +
```

## Step 3: Add it in submit function too

Inside submit function, add:

```js
const budget = document.getElementById("budget").value.trim();
```

Then add it to actual WhatsApp message:

```js
"Budget: " + (budget || "Not provided") + "\n\n" +
```

---

# 39. Useful New Fields You Can Add

## Deadline field

```html
<div class="input-group">
  <label class="floating-label" for="deadline">Needed By</label>
  <input id="deadline" type="text" placeholder="Example: 18 May / next week / flexible" oninput="updatePreview()">
</div>
```

Add in JavaScript:

```js
const deadline = document.getElementById("deadline").value.trim();
```

Add in WhatsApp message:

```js
"Needed By: " + (deadline || "Not provided") + "\n" +
```

## Artwork size field

```html
<div class="input-group">
  <label class="floating-label" for="sizeIdea">Size Preference</label>
  <select id="sizeIdea" onchange="updatePreview()">
    <option>Not sure yet</option>
    <option>Small</option>
    <option>Medium</option>
    <option>Large</option>
    <option>XL</option>
  </select>
</div>
```

Add in JavaScript:

```js
const sizeIdea = document.getElementById("sizeIdea").value;
```

Add in message:

```js
"Size Preference: " + sizeIdea + "\n" +
```

---

# 40. How To Edit Submit Button

Search:

```html
submit-btn
```

You will see:

```html
<button type="submit" class="submit-btn">Send Guided Message on WhatsApp →</button>
```

Better options:

```html
<button type="submit" class="submit-btn">Send to WhatsApp →</button>
```

```html
<button type="submit" class="submit-btn">Send My Artwork Request →</button>
```

```html
<button type="submit" class="submit-btn">Get Personal Guidance →</button>
```

Keep:

```html
type="submit"
```

And keep:

```html
class="submit-btn"
```

---

# 41. How To Edit Mini Text Under Submit Button

Search:

```html
mini-text
```

You may see:

```html
<p class="mini-text">This will open WhatsApp with your message ready to send.</p>
```

Better options:

```html
<p class="mini-text">This opens WhatsApp with your message prepared. You can still edit it before sending.</p>
```

```html
<p class="mini-text">No payment here. This only starts the guidance conversation on WhatsApp.</p>
```

```html
<p class="mini-text">Your request opens in WhatsApp so you can attach photos and continue the conversation.</p>
```

---

# 42. How To Edit Trust Box

Search:

```html
trust
```

You may see:

```html
<div class="trust">
  Your details are only used to understand your artwork request and guide you properly.
</div>
```

Better:

```html
<div class="trust">
  Your details are only used to understand your artwork request, suggest the right size/style, and continue the conversation on WhatsApp.
</div>
```

---

# 43. How To Edit Preview Box Text

Search:

```html
preview-box
```

You will find:

```html
<div class="preview-box">
  <strong>WhatsApp preview</strong>
  <div class="preview-text" id="previewText"></div>
</div>
```

Change label:

```html
<strong>Message preview</strong>
```

or:

```html
<strong>Your WhatsApp message preview</strong>
```

Do not change:

```html
id="previewText"
```

JavaScript uses it.

---

# 44. How To Edit FAQ Section

Search:

```html
faq-wrap
```

You will see FAQ items like:

```html
<div class="faq-item active">
  <button type="button" class="faq-question" onclick="toggleFaq(this)">
    <span>What should I send first?</span>
    <span>+</span>
  </button>
  <div class="faq-answer">
    <p>Send your photo, occasion, and the date you need it by.</p>
  </div>
</div>
```

## Change question

```html
<span>What should I send first?</span>
```

## Change answer

```html
<p>Send your photo, occasion, and the date you need it by.</p>
```

## Keep this

```html
onclick="toggleFaq(this)"
```

That makes FAQ open and close.

---

# 45. How To Add A New FAQ

Paste this inside:

```html
<div class="faq-wrap">
```

New FAQ:

```html
<div class="faq-item">
  <button type="button" class="faq-question" onclick="toggleFaq(this)">
    <span>Can I send multiple photos?</span>
    <span>+</span>
  </button>
  <div class="faq-answer">
    <p>Yes. Send 2-3 photos and I’ll guide you on which one will look best as string art.</p>
  </div>
</div>
```

Another good FAQ:

```html
<div class="faq-item">
  <button type="button" class="faq-question" onclick="toggleFaq(this)">
    <span>Can I ask the price before ordering?</span>
    <span>+</span>
  </button>
  <div class="faq-answer">
    <p>Yes. You can message first with your idea and I’ll guide you with size, price, and timeline before you confirm.</p>
  </div>
</div>
```

---

# 46. How FAQ JavaScript Works

Search:

```js
function toggleFaq
```

You will see:

```js
function toggleFaq(button) {
  const item = button.closest(".faq-item");
  item.classList.toggle("active");
}
```

This means:

```txt
Click question
        ↓
Find closest FAQ item
        ↓
Add/remove active class
        ↓
CSS opens/closes answer
```

CSS:

```css
.faq-item.active .faq-answer {
  max-height: 160px;
}
```

If your answer is long and gets cut, increase it:

```css
.faq-item.active .faq-answer {
  max-height: 260px;
}
```

---

# 47. How To Make Only One FAQ Open At A Time

Replace the current function:

```js
function toggleFaq(button) {
  const item = button.closest(".faq-item");
  item.classList.toggle("active");
}
```

With this:

```js
function toggleFaq(button) {
  const item = button.closest(".faq-item");
  const isOpen = item.classList.contains("active");

  document.querySelectorAll(".faq-item").forEach(function(faq) {
    faq.classList.remove("active");
  });

  if (!isOpen) {
    item.classList.add("active");
  }
}
```

Now opening one FAQ closes the others.

---

# 48. How To Edit Luxury Band Section

Search:

```html
luxury-band
```

This section explains why contacting first matters.

You may see:

```html
<div class="band-dark">
  <h2>...</h2>
  <p>...</p>
</div>
```

Better copy:

```html
<div class="band-dark">
  <h2>A quick message can make the final artwork much better.</h2>
  <p>
    Photo choice, size, deadline, and occasion matter a lot. Before you order, I can help you avoid weak photos, rushed decisions, and unclear ideas.
  </p>
</div>
```

---

# 49. How To Edit Psychology Cards

Search:

```html
psych-card
```

You will see cards like:

```html
<div class="psych-card">
  <h3>Confused about the photo?</h3>
  <p>Bad photo choice can make even a good artwork feel weak.</p>
</div>
```

Better cards:

```html
<div class="psych-card">
  <h3>Confused about the photo?</h3>
  <p>Bad photo choice can make even a good artwork feel weak. Send options and I’ll help you choose the strongest one.</p>
</div>

<div class="psych-card">
  <h3>Buying for a deadline?</h3>
  <p>Mention your date clearly. I’ll guide you honestly about what can be done smoothly without rushing the handmade quality.</p>
</div>

<div class="psych-card">
  <h3>Not sure about size?</h3>
  <p>Tell me where you want to keep or gift it. I’ll suggest a size that feels right for the space and budget.</p>
</div>

<div class="psych-card">
  <h3>Want it to feel emotional?</h3>
  <p>Names, dates, quotes, heart shapes, and small personal details can make the artwork feel made only for them.</p>
</div>
```

---

# 50. How To Edit Final CTA

Search:

```html
final-cta
```

You will see:

```html
<section class="final-cta reveal">
  <div class="final-inner">
    <h2>The best gifts don’t feel expensive. They feel personal.</h2>
    <p>
      Start with one message. Share the memory, the person, or the occasion — and I’ll help you turn it into something worth keeping.
    </p>
    <a href="https://wa.me/918087827454?text=..." target="_blank" class="btn btn-primary">Message MalayPaul Arts</a>
  </div>
</section>
```

Better options:

```html
<h2>The best gifts don’t feel expensive. They feel personal.</h2>
<p>
  Start with one message. Share the memory, the person, or the occasion — and I’ll help you turn it into something worth keeping.
</p>
```

```html
<h2>Not sure what to order? Start with the photo.</h2>
<p>
  Send me the photo and occasion. I’ll guide you with the best style, size, price, and timeline before you decide.
</p>
```

```html
<h2>One message can turn the idea into something clear.</h2>
<p>
  You do not need to know everything before contacting. Share the memory and I’ll help shape the artwork.
</p>
```

---

# 51. How To Edit Floating WhatsApp CTA

Search:

```html
floatingCta
```

You will see:

```html
<a href="https://wa.me/918087827454?text=Hi%20MalayPaul%20Arts%20%F0%9F%91%8B%0A%0AI%20want%20help%20with%20a%20custom%20artwork." target="_blank" class="floating-cta" id="floatingCta">💬 WhatsApp Now</a>
```

Change text:

```html
💬 WhatsApp Now
```

to:

```html
💬 Ask on WhatsApp
```

or:

```html
💬 Get Guidance
```

Change number:

```html
https://wa.me/919876543210
```

Keep:

```html
id="floatingCta"
```

JavaScript uses it.

---

# 52. When Floating CTA Appears

Search:

```js
window.scrollY > 560
```

You will see:

```js
window.addEventListener("scroll", function() {
  if (window.scrollY > 560) {
    floatingCta.classList.add("show");
  } else {
    floatingCta.classList.remove("show");
  }
});
```

This means:

```txt
After user scrolls 560px, WhatsApp floating button appears.
```

## Show earlier

```js
if (window.scrollY > 300)
```

## Show later

```js
if (window.scrollY > 800)
```

---

# 53. How To Keep Floating CTA Always Visible

Remove the scroll condition and add `show` directly in HTML:

```html
<a href="https://wa.me/918087827454?text=Hi..." target="_blank" class="floating-cta show" id="floatingCta">💬 WhatsApp Now</a>
```

Then remove or ignore this script:

```js
window.addEventListener("scroll", function() {
  if (window.scrollY > 560) {
    floatingCta.classList.add("show");
  } else {
    floatingCta.classList.remove("show");
  }
});
```

But I recommend keeping it scroll-based so it feels less aggressive.

---

# 54. How To Edit Footer

Search:

```html
premium-footer
```

You will see:

```html
<footer class="premium-footer">
```

Change footer brand:

```html
<h2 class="footer-brand">MalayPaul Arts</h2>
```

Change footer text:

```html
<p class="footer-text">
  Premium handmade string art portraits crafted for memories, gifts, love stories, and moments worth keeping forever.
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

# 55. How Reveal Animation Works

Search:

```css
.reveal
```

CSS:

```css
.reveal {
  opacity: 0;
  transform: translateY(22px);
  transition: 0.7s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

JavaScript:

```js
const observer = new IntersectionObserver(function(entries) {
  entries.forEach(function(entry) {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
    }
  });
}, { threshold: 0.14 });

document.querySelectorAll(".reveal").forEach(function(element) {
  observer.observe(element);
});
```

If you add a new section and want it to animate, add:

```html
class="section reveal"
```

or:

```html
<div class="psych-card reveal">
```

---

# 56. How To Edit Mouse Glow Effect

Search:

```js
pointermove
```

You will see code that updates:

```css
--mx
--my
```

CSS uses it here:

```css
body::after {
  background:
    radial-gradient(circle at var(--mx, 50%) var(--my, 18%), rgba(255,255,255,0.35), transparent 24%);
}
```

## Make glow stronger

```css
rgba(255,255,255,0.48)
```

## Make glow softer

```css
rgba(255,255,255,0.22)
```

## Make glow bigger

```css
transparent 34%
```

---

# 57. How Mobile Menu Works

Important elements:

```html
<div class="mobile-backdrop" id="mobileBackdrop"></div>
<div class="menu" id="menu">
<button class="hamburger" id="hamburger">
```

JavaScript:

```js
function openMenu() {
  body.classList.add("menu-open");
  hamburger.setAttribute("aria-expanded", "true");
}

function closeMenu() {
  body.classList.remove("menu-open");
  hamburger.setAttribute("aria-expanded", "false");
}
```

Do not remove:

```html
id="menu"
id="hamburger"
id="mobileBackdrop"
```

---

# 58. Common Mistakes And Fixes

## Mistake 1: WhatsApp opens wrong number

Search all:

```txt
918087827454
```

Replace every instance with your number.

Also check:

```js
const phoneNumber = "918087827454";
```

---

## Mistake 2: Form button not working

Check form ID:

```html
<form id="whatsappForm">
```

Check submit button:

```html
<button type="submit" class="submit-btn">
```

Check JavaScript:

```js
document.getElementById("whatsappForm").addEventListener("submit", function(e) {
```

All three must exist.

---

## Mistake 3: Preview not updating

Check input has:

```html
oninput="updatePreview()"
```

Dropdown should have:

```html
onchange="updatePreview()"
```

Message textarea should have:

```html
oninput="updatePreview()"
```

---

## Mistake 4: Quick chip does nothing

Check chip has:

```html
class="quick-chip"
```

and:

```html
data-message="..."
```

Also keep:

```html
type="button"
```

---

## Mistake 5: FAQ not opening

Check question button has:

```html
onclick="toggleFaq(this)"
```

Check FAQ item structure:

```html
<div class="faq-item">
  <button type="button" class="faq-question" onclick="toggleFaq(this)">
    <span>Question</span>
    <span>+</span>
  </button>
  <div class="faq-answer">
    <p>Answer</p>
  </div>
</div>
```

---

## Mistake 6: FAQ answer gets cut

Search:

```css
.faq-item.active .faq-answer
```

Change:

```css
max-height: 160px;
```

to:

```css
max-height: 260px;
```

---

## Mistake 7: New field not appearing in WhatsApp

Adding HTML field is not enough.

You must add it in:

```js
updatePreview()
```

and in:

```js
whatsappForm submit
```

---

## Mistake 8: Navbar active page not showing

Check:

```html
<body data-page="contact">
```

Check nav link:

```html
<a href="contact.html" class="nav-link" data-page="contact">Contact</a>
```

---

# 59. Best Contact Page Copy Setup

Use this if you want a clean premium contact page.

## Hero

```html
<span class="tag">Private Artwork Guidance</span>
<h1>Let’s turn your idea into a <span>gift they remember.</span></h1>
<p>
  Send your photo, occasion, or even a half-clear idea. I’ll help you choose the right artwork type, size, and gift plan before you place the final order.
</p>
```

## Hero buttons

```html
<a href="https://wa.me/918087827454?text=Hi%20MalayPaul%20Arts%20I%20want%20help%20with%20a%20custom%20artwork" target="_blank" class="btn btn-primary">Start on WhatsApp →</a>
<a href="#contact-form" class="btn btn-soft">Write a Guided Message</a>
```

## Premium strip

```html
<div class="strip-card">
  <strong>Photo Selection Help</strong>
  <span>Send multiple photos and I’ll help pick the one that will look most premium.</span>
</div>
```

## Form heading

```html
<h2>Start with the right message</h2>
<p>
  Choose what you need, fill the details, and it will open WhatsApp with a clean premium message already prepared.
</p>
```

## Final CTA

```html
<h2>The best gifts don’t feel expensive. They feel personal.</h2>
<p>
  Start with one message. Share the memory, the person, or the occasion — and I’ll help you turn it into something worth keeping.
</p>
```

---

# 60. Testing Checklist

After every edit, press:

```txt
Ctrl + S
```

Then refresh browser and check:

- [ ] Logo appears
- [ ] Navbar links work
- [ ] Contact tab is active
- [ ] Hero WhatsApp button opens correct number
- [ ] Hero scroll button goes to form
- [ ] Premium strip cards look clean
- [ ] Info WhatsApp link opens correct number
- [ ] Instagram link works
- [ ] Name field works
- [ ] Phone field works
- [ ] Email field works
- [ ] Occasion dropdown works
- [ ] Message box works
- [ ] Character count updates
- [ ] Live preview updates while typing
- [ ] Quick chips fill the message
- [ ] Submit button opens WhatsApp
- [ ] WhatsApp message contains correct details
- [ ] Empty name/message shows alert
- [ ] FAQ opens and closes
- [ ] Floating WhatsApp button appears after scroll
- [ ] Mobile menu opens
- [ ] Mobile menu closes
- [ ] Footer links work
- [ ] No horizontal scroll on phone

---

# 61. Best Editing Workflow

Do not edit everything at once.

Use this:

```txt
Change one thing
Save
Refresh browser
Test it
Then edit next thing
```

Especially for this page, test after editing:

- WhatsApp number
- Form IDs
- Quick chips
- Preview message
- Submit message
- FAQ

Small JavaScript mistakes can stop the form from working.

---

# 62. Simple Mental Model

Think of this contact page like this:

```txt
Hero
  ↓
Trust / guidance cards
  ↓
Contact info
  ↓
Guided WhatsApp form
  ↓
Live preview
  ↓
WhatsApp submit
  ↓
FAQ
  ↓
Final CTA
  ↓
Floating WhatsApp button
  ↓
Footer
```

The page is not just a contact page.

It sells this feeling:

```txt
“You don’t need to know exactly what to order. Send the memory, and I’ll guide you.”
```

Keep that feeling in every line.
