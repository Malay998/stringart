# MalayPaul Arts — Order Page Editing Guide

> Best file name for this guide: `ORDER_PAGE_EDITING_GUIDE.md`  
> Keep this file in the same project folder as `order.html`, so whenever you forget something, you can open this guide in VS Code.

---

# 0. How To Use This Guide In VS Code

Open this file in VS Code.

To see it beautifully formatted:

```txt
Ctrl + Shift + V
```

Or open preview on the side:

```txt
Ctrl + K, then V
```

The colourful code blocks work because this is a `.md` file and the code is wrapped like this:

````md
```html
<p>This becomes colourful HTML code.</p>
```
````

---

# 1. The Most Important Rule

Your order page has 3 main parts:

| Area | What It Controls | What To Search |
|---|---|---|
| Size cards | Small / Medium / Large / XL prices | `name="size"` |
| Artwork add-ons | Single face, 2 face, pet, logo, custom, etc. | `name="artType"` |
| Coupon codes | Discount codes like `MALAY10` | `const COUPONS` |
| WhatsApp number | Where the order goes | `WHATSAPP_NUMBER` |
| Order total | Live price summary | `updateSummary()` |

The golden rule:

> If something affects price, change the **real price** and the **visible price**.

Real price looks like this:

```html
data-price="899"
```

Visible price looks like this:

```html
<strong>₹899</strong>
```

or this:

```html
<div class="art-price">+₹250</div>
```

If you change only one, your website may show one price but calculate another price.

---

# 2. How To Change Size Prices

## Step 1: Find the size cards

In VS Code, press:

```txt
Ctrl + F
```

Search:

```html
name="size"
```

You will see code like this:

```html
<label class="size-option featured-size">
  <input type="radio" name="size" value="Medium - 12 x 16 inch" data-price="899" checked onchange="updateSummary()">
  <span>
    <span class="popular-ribbon">★ Most Popular</span>
    <div>
      <b>Medium</b>
      <small>12 x 16 inch<br>Premium look, perfect balance.</small>
    </div>
    <strong>₹899</strong>
  </span>
</label>
```

## Step 2: Change both prices

Example: change Medium from ₹899 to ₹999.

Change this:

```html
data-price="899"
```

to this:

```html
data-price="999"
```

Then change this:

```html
<strong>₹899</strong>
```

to this:

```html
<strong>₹999</strong>
```

Final result:

```html
<label class="size-option featured-size">
  <input type="radio" name="size" value="Medium - 12 x 16 inch" data-price="999" checked onchange="updateSummary()">
  <span>
    <span class="popular-ribbon">★ Most Popular</span>
    <div>
      <b>Medium</b>
      <small>12 x 16 inch<br>Premium look, perfect balance.</small>
    </div>
    <strong>₹999</strong>
  </span>
</label>
```

---

# 3. Suggested Premium Pricing Setup

You can use this kind of pricing if you want the website to feel more premium:

| Size | Current Style | Suggested Price |
|---|---:|---:|
| Small | Starter | ₹699 |
| Medium | Most Popular | ₹999 |
| Large | Premium Wall Art | ₹1599 |
| XL | Statement Piece | ₹2199 |

Example:

```html
<label class="size-option">
  <input type="radio" name="size" value="Small - 8 x 10 inch" data-price="699" onchange="updateSummary()">
  <span>
    <div>
      <b>Small</b>
      <small>8 x 10 inch<br>Perfect for simple gifting.</small>
    </div>
    <strong>₹699</strong>
  </span>
</label>

<label class="size-option featured-size">
  <input type="radio" name="size" value="Medium - 12 x 16 inch" data-price="999" checked onchange="updateSummary()">
  <span>
    <span class="popular-ribbon">★ Most Popular</span>
    <div>
      <b>Medium</b>
      <small>12 x 16 inch<br>Premium look, perfect balance.</small>
    </div>
    <strong>₹999</strong>
  </span>
</label>

<label class="size-option">
  <input type="radio" name="size" value="Large - 16 x 20 inch" data-price="1599" onchange="updateSummary()">
  <span>
    <div>
      <b>Large</b>
      <small>16 x 20 inch<br>Best for detailed wall art.</small>
    </div>
    <strong>₹1599</strong>
  </span>
</label>

<label class="size-option">
  <input type="radio" name="size" value="XL - 18 x 24 inch" data-price="2199" onchange="updateSummary()">
  <span>
    <div>
      <b>XL</b>
      <small>18 x 24 inch<br>For a grand premium display.</small>
    </div>
    <strong>₹2199</strong>
  </span>
</label>
```

---

# 4. How To Move “Most Popular” To Another Size

Your popular card is controlled by two things:

```html
featured-size
```

and:

```html
<span class="popular-ribbon">★ Most Popular</span>
```

## Example: Move “Most Popular” from Medium to Large

### Step 1: Remove from Medium

Before:

```html
<label class="size-option featured-size">
  <input type="radio" name="size" value="Medium - 12 x 16 inch" data-price="899" checked onchange="updateSummary()">
  <span>
    <span class="popular-ribbon">★ Most Popular</span>
```

After:

```html
<label class="size-option">
  <input type="radio" name="size" value="Medium - 12 x 16 inch" data-price="899" onchange="updateSummary()">
  <span>
```

What changed:

- Removed `featured-size`
- Removed the `popular-ribbon`
- Removed `checked`, because Large will become default now

### Step 2: Add to Large

Before:

```html
<label class="size-option">
  <input type="radio" name="size" value="Large - 16 x 20 inch" data-price="1499" onchange="updateSummary()">
  <span>
    <div>
      <b>Large</b>
```

After:

```html
<label class="size-option featured-size">
  <input type="radio" name="size" value="Large - 16 x 20 inch" data-price="1499" checked onchange="updateSummary()">
  <span>
    <span class="popular-ribbon">★ Most Popular</span>
    <div>
      <b>Large</b>
```

## Important

Only one size should have this:

```html
checked
```

If two sizes have `checked`, the browser may behave weirdly.

---

# 5. How To Change The Default Selected Size

The default selected size is the one with:

```html
checked
```

Example:

```html
<input type="radio" name="size" value="Medium - 12 x 16 inch" data-price="899" checked onchange="updateSummary()">
```

To make XL selected by default, remove `checked` from Medium and add it to XL.

XL example:

```html
<input type="radio" name="size" value="XL - 18 x 24 inch" data-price="1999" checked onchange="updateSummary()">
```

Again:

> Only one size gets `checked`.

---

# 6. How To Add A New Size

Search:

```html
<div class="size-grid">
```

Inside that grid, paste a new size card.

Example: Add XXL.

```html
<label class="size-option">
  <input type="radio" name="size" value="XXL - 24 x 30 inch" data-price="2999" onchange="updateSummary()">
  <span>
    <div>
      <b>XXL</b>
      <small>24 x 30 inch<br>Luxury wall statement piece.</small>
    </div>
    <strong>₹2999</strong>
  </span>
</label>
```

## If you add more than 4 sizes

Your layout may become tight on laptop.

Search:

```css
.size-grid
```

You may see something like:

```css
.size-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  margin-bottom: 28px;
}
```

Replace only the `grid-template-columns` line with this:

```css
grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
```

Better final version:

```css
.size-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
  gap: 16px;
  margin-bottom: 28px;
}
```

This makes your size cards automatically adjust for 4, 5, or 6 sizes.

---

# 7. How To Remove A Size

Find the full size block:

```html
<label class="size-option">
  ...
</label>
```

Delete the whole block.

Do not delete only the text inside it.

A size card always starts with:

```html
<label class="size-option">
```

or:

```html
<label class="size-option featured-size">
```

and ends with:

```html
</label>
```

---

# 8. How To Change Artwork Add-On Prices

## Step 1: Find artwork options

Press:

```txt
Ctrl + F
```

Search:

```html
name="artType"
```

You will see cards like this:

```html
<label class="art-option">
  <input type="radio" name="artType" value="2 Face Portrait" data-price="250" onchange="updateSummary()">
  <span>
    <div class="art-icon">👥</div>
    <div class="art-copy">
      <b>2 Face Portrait</b>
      <small>For couples, siblings, friends, or parents.</small>
    </div>
    <div class="art-price">+₹250</div>
  </span>
</label>
```

## Step 2: Change both add-on prices

Example: change 2 Face Portrait from +₹250 to +₹350.

Change:

```html
data-price="250"
```

to:

```html
data-price="350"
```

Then change:

```html
<div class="art-price">+₹250</div>
```

to:

```html
<div class="art-price">+₹350</div>
```

Final:

```html
<label class="art-option">
  <input type="radio" name="artType" value="2 Face Portrait" data-price="350" onchange="updateSummary()">
  <span>
    <div class="art-icon">👥</div>
    <div class="art-copy">
      <b>2 Face Portrait</b>
      <small>For couples, siblings, friends, or parents.</small>
    </div>
    <div class="art-price">+₹350</div>
  </span>
</label>
```

---

# 9. Suggested Artwork Add-On Pricing

| Artwork Type | Suggested Add-On |
|---|---:|
| Single Face Portrait | Base |
| 2 Face Portrait | +₹350 |
| 3 Face Portrait | +₹550 |
| 4 Face Portrait | +₹750 |
| Couple Heart Portrait | +₹450 |
| Pet Portrait | +₹350 |
| Name / Text Artwork | +₹200 |
| Logo / Brand Artwork | +₹700 |
| Something Custom | +₹400 |

Example setup:

```html
<label class="art-option">
  <input type="radio" name="artType" value="Single Face Portrait" data-price="0" checked onchange="updateSummary()">
  <span>
    <div class="art-icon">👤</div>
    <div class="art-copy">
      <b>Single Face Portrait</b>
      <small>Best for one person, clean and elegant.</small>
    </div>
    <div class="art-price">Base</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="2 Face Portrait" data-price="350" onchange="updateSummary()">
  <span>
    <div class="art-icon">👥</div>
    <div class="art-copy">
      <b>2 Face Portrait</b>
      <small>For couples, siblings, friends, or parents.</small>
    </div>
    <div class="art-price">+₹350</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="3 Face Portrait" data-price="550" onchange="updateSummary()">
  <span>
    <div class="art-icon">👨‍👩‍👧</div>
    <div class="art-copy">
      <b>3 Face Portrait</b>
      <small>Great for small family or trio artwork.</small>
    </div>
    <div class="art-price">+₹550</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="4 Face Portrait" data-price="750" onchange="updateSummary()">
  <span>
    <div class="art-icon">👨‍👩‍👧‍👦</div>
    <div class="art-copy">
      <b>4 Face Portrait</b>
      <small>Family style artwork with more detailing.</small>
    </div>
    <div class="art-price">+₹750</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="Couple Portrait in Heart Shape" data-price="450" onchange="updateSummary()">
  <span>
    <div class="art-icon">♥</div>
    <div class="art-copy">
      <b>Couple Heart Portrait</b>
      <small>Romantic heart-shape concept for couples.</small>
    </div>
    <div class="art-price">+₹450</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="Pet Portrait" data-price="350" onchange="updateSummary()">
  <span>
    <div class="art-icon">🐾</div>
    <div class="art-copy">
      <b>Pet Portrait</b>
      <small>For dog, cat, or any pet memory.</small>
    </div>
    <div class="art-price">+₹350</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="Name / Text Artwork" data-price="200" onchange="updateSummary()">
  <span>
    <div class="art-icon">✦</div>
    <div class="art-copy">
      <b>Name / Text Artwork</b>
      <small>Name, date, quote, initials, or message.</small>
    </div>
    <div class="art-price">+₹200</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="Logo / Brand Artwork" data-price="700" onchange="updateSummary()">
  <span>
    <div class="art-icon">◆</div>
    <div class="art-copy">
      <b>Logo / Brand Artwork</b>
      <small>For business, studio, cafe, or room decor.</small>
    </div>
    <div class="art-price">+₹700</div>
  </span>
</label>

<label class="art-option">
  <input type="radio" name="artType" value="Something Custom / Creative" data-price="400" onchange="updateSummary()">
  <span>
    <div class="art-icon">✨</div>
    <div class="art-copy">
      <b>Something Custom</b>
      <small>Have a unique idea? Share it with me.</small>
    </div>
    <div class="art-price">+₹400</div>
  </span>
</label>
```

---

# 10. How To Add A New Artwork Option

Copy an existing artwork option and change 4 things:

1. `value`
2. `data-price`
3. Visible title
4. Visible price

Example: Add “Car / Bike Artwork”.

```html
<label class="art-option">
  <input type="radio" name="artType" value="Car / Bike Artwork" data-price="500" onchange="updateSummary()">
  <span>
    <div class="art-icon">🏍️</div>
    <div class="art-copy">
      <b>Car / Bike Artwork</b>
      <small>For vehicle lovers, riders, and statement decor.</small>
    </div>
    <div class="art-price">+₹500</div>
  </span>
</label>
```

---

# 11. How To Add More Coupon Codes

## Step 1: Find coupon code section

Search:

```js
const COUPONS
```

You will see this kind of code:

```js
const COUPONS = {
  "MALAY10": {
    type: "percent",
    value: 10,
    message: "10% discount applied."
  },
  "ART100": {
    type: "flat",
    value: 100,
    message: "₹100 discount applied."
  },
  "GIFT15": {
    type: "percent",
    value: 15,
    message: "15% discount applied."
  }
};
```

## Coupon type 1: Percentage discount

Example: 20% off.

```js
"PREMIUM20": {
  type: "percent",
  value: 20,
  message: "20% premium discount applied."
}
```

## Coupon type 2: Flat rupee discount

Example: ₹200 off.

```js
"SAVE200": {
  type: "flat",
  value: 200,
  message: "₹200 discount applied."
}
```

## Full example with new coupons added

```js
const COUPONS = {
  "MALAY10": {
    type: "percent",
    value: 10,
    message: "10% discount applied."
  },
  "ART100": {
    type: "flat",
    value: 100,
    message: "₹100 discount applied."
  },
  "GIFT15": {
    type: "percent",
    value: 15,
    message: "15% discount applied."
  },
  "PREMIUM20": {
    type: "percent",
    value: 20,
    message: "20% premium discount applied."
  },
  "SAVE200": {
    type: "flat",
    value: 200,
    message: "₹200 discount applied."
  }
};
```

## Important comma rule

Every coupon except the last one needs a comma after it.

Correct:

```js
"MALAY10": {
  type: "percent",
  value: 10,
  message: "10% discount applied."
},
"SAVE200": {
  type: "flat",
  value: 200,
  message: "₹200 discount applied."
}
```

Wrong:

```js
"MALAY10": {
  type: "percent",
  value: 10,
  message: "10% discount applied."
}
"SAVE200": {
  type: "flat",
  value: 200,
  message: "₹200 discount applied."
}
```

The wrong version is missing a comma.

---

# 12. Best Coupon Ideas For Your Website

| Coupon Code | Type | Value | Meaning |
|---|---|---:|---|
| `MALAY10` | percent | 10 | Simple welcome discount |
| `GIFT15` | percent | 15 | Gift-based discount |
| `PREMIUM20` | percent | 20 | Strong festival/special offer |
| `SAVE200` | flat | 200 | Easy flat discount |
| `FIRST100` | flat | 100 | First order discount |
| `COUPLE15` | percent | 15 | Couples/anniversary orders |
| `PETLOVE10` | percent | 10 | Pet portraits |
| `FAMILY250` | flat | 250 | Family portraits |

Code version:

```js
const COUPONS = {
  "MALAY10": {
    type: "percent",
    value: 10,
    message: "10% discount applied."
  },
  "GIFT15": {
    type: "percent",
    value: 15,
    message: "15% gift discount applied."
  },
  "PREMIUM20": {
    type: "percent",
    value: 20,
    message: "20% premium discount applied."
  },
  "SAVE200": {
    type: "flat",
    value: 200,
    message: "₹200 discount applied."
  },
  "FIRST100": {
    type: "flat",
    value: 100,
    message: "₹100 first order discount applied."
  },
  "COUPLE15": {
    type: "percent",
    value: 15,
    message: "15% couple artwork discount applied."
  },
  "PETLOVE10": {
    type: "percent",
    value: 10,
    message: "10% pet portrait discount applied."
  },
  "FAMILY250": {
    type: "flat",
    value: 250,
    message: "₹250 family artwork discount applied."
  }
};
```

---

# 13. How Coupon Calculation Works

Your code calculates subtotal like this:

```js
function getSubtotal() {
  return getSizePrice() + getAddonPrice();
}
```

That means:

```txt
Subtotal = Size Price + Artwork Add-On Price
```

Then it applies discount.

For percentage coupon:

```js
discountAmount = Math.round((subtotal * activeCoupon.value) / 100);
```

For flat coupon:

```js
discountAmount = activeCoupon.value;
```

Then final total becomes:

```js
return getSubtotal() - discountAmount;
```

Meaning:

```txt
Final Total = Size Price + Add-On Price - Coupon Discount
```

---

# 14. How To Change WhatsApp Number

Search:

```js
WHATSAPP_NUMBER
```

You will see:

```js
const WHATSAPP_NUMBER = "918087827454";
```

Change only the number inside the quotes.

Example:

```js
const WHATSAPP_NUMBER = "919876543210";
```

Rules:

- Use country code
- No `+`
- No spaces
- No hyphen

Correct:

```js
const WHATSAPP_NUMBER = "919876543210";
```

Wrong:

```js
const WHATSAPP_NUMBER = "+91 98765 43210";
```

---

# 15. How To Edit The WhatsApp Message

Search:

```js
const message =
```

or:

```js
whatsappMessage
```

You will find the code that creates the WhatsApp text.

It may look like this:

```js
const message =
  "Hi MalayPaul Arts 👋%0A%0A" +
  "I want to reserve a handmade string art slot.%0A%0A" +
  "Name: " + name + "%0A" +
  "Phone: " + phone + "%0A" +
  "Email: " + email + "%0A" +
  "Size: " + getSelectedSize() + "%0A" +
  "Artwork: " + getSelectedArt() + "%0A" +
  "Total: ₹" + getTotal() + "%0A%0A" +
  "Notes: " + notes;
```

You can make it more premium like this:

```js
const message =
  "Hi MalayPaul Arts 👋%0A%0A" +
  "I want to reserve a premium handmade string art slot.%0A%0A" +
  "CUSTOMER DETAILS%0A" +
  "Name: " + name + "%0A" +
  "Phone: " + phone + "%0A" +
  "Email: " + email + "%0A%0A" +
  "ARTWORK DETAILS%0A" +
  "Size: " + getSelectedSize() + "%0A" +
  "Artwork Type: " + getSelectedArt() + "%0A" +
  "Interest: " + getInterest() + "%0A" +
  "Coupon: " + (activeCoupon ? activeCoupon.code : "No coupon") + "%0A" +
  "Estimated Total: ₹" + getTotal() + "%0A%0A" +
  "NOTES%0A" +
  (notes || "No extra notes added yet.") + "%0A%0A" +
  "Please guide me with the best photo, size, final design, and next steps.";
```

---

# 16. How To Change Customer Input Fields

Customer fields may look like this:

```html
<input id="customerName" type="text" placeholder="Your name">
<input id="customerPhone" type="tel" placeholder="WhatsApp number">
<input id="customerEmail" type="email" placeholder="Email address">
```

You can change only the placeholder text safely.

Example:

```html
<input id="customerName" type="text" placeholder="Your full name">
```

Do not randomly change the `id`, because JavaScript uses the `id`.

For example, this JavaScript depends on the same ID:

```js
const name = document.getElementById("customerName").value.trim();
```

If you change:

```html
id="customerName"
```

to:

```html
id="name"
```

then you must also change the JavaScript.

So safest rule:

> Change placeholder text, not IDs.

---

# 17. How To Make A Field Required

Example:

```html
<input id="customerName" type="text" placeholder="Your name">
```

Add `required`:

```html
<input id="customerName" type="text" placeholder="Your name" required>
```

For textarea:

```html
<textarea id="notes" placeholder="Add your notes" required></textarea>
```

Use required only for fields you really need.

Good required fields:

- Name
- WhatsApp number

Optional fields:

- Email
- Notes
- Coupon

---

# 18. How To Edit The Photo Upload Text

Search:

```html
referenceFile
```

You may see:

```html
<input id="referenceFile" type="file" onchange="updateSummary()">
```

You can edit text around it, but avoid changing this:

```html
id="referenceFile"
```

Because JavaScript uses it here:

```js
const fileInput = document.getElementById("referenceFile");
const fileName = fileInput.files.length > 0 ? fileInput.files[0].name : "No file selected yet";
```

Safe thing to edit:

```html
<p class="section-text">
  Upload your photo reference so I can understand the artwork better.
</p>
```

---

# 19. How To Change The Live Summary Text

Search:

```js
function updateSummary()
```

Inside this function, you will see:

```js
let summaryHtml =
  '<div class="summary-row"><b>Size</b><span>' + size + '</span></div>' +
  '<div class="summary-row"><b>Artwork</b><span>' + art + '</span></div>' +
  '<div class="summary-row"><b>Interest</b><span>' + interest + '</span></div>' +
  '<div class="summary-row"><b>Coupon</b><span>' + (activeCoupon ? activeCoupon.code : "No coupon") + '</span></div>';
```

You can change labels like this:

```js
let summaryHtml =
  '<div class="summary-row"><b>Selected Size</b><span>' + size + '</span></div>' +
  '<div class="summary-row"><b>Artwork Style</b><span>' + art + '</span></div>' +
  '<div class="summary-row"><b>Customer Intent</b><span>' + interest + '</span></div>' +
  '<div class="summary-row"><b>Offer Code</b><span>' + (activeCoupon ? activeCoupon.code : "No coupon") + '</span></div>';
```

Do not remove `+ size +`, `+ art +`, or similar values unless you know what you are doing.

---

# 20. How To Change The Summary Prices

Search:

```js
sizePrice
```

You will see:

```js
document.getElementById("sizePrice").innerText = "₹" + getSizePrice();
document.getElementById("addonPrice").innerText = "₹" + getAddonPrice();
document.getElementById("finalPrice").innerText = "Total: ₹" + total;
```

You can change the wording:

```js
document.getElementById("finalPrice").innerText = "Estimated Total: ₹" + total;
```

Or:

```js
document.getElementById("finalPrice").innerText = "Approx Total: ₹" + total;
```

Do not remove:

```js
+ total
```

That is what displays the actual calculated price.

---

# 21. How To Change “Send To WhatsApp” Button Text

Search:

```html
Send to WhatsApp
```

You may see:

```html
<button class="main-btn" onclick="orderNow()">Send to WhatsApp</button>
```

Change it to:

```html
<button class="main-btn" onclick="orderNow()">Reserve My Artwork Slot</button>
```

or:

```html
<button class="main-btn" onclick="orderNow()">Send My Premium Request</button>
```

Keep this part:

```html
onclick="orderNow()"
```

Without it, the button will stop working.

---

# 22. How To Change The FOMO Text

Search:

```html
premium-fomo
```

You may see something like:

```html
<div class="premium-fomo">
  If this is for a gift, don’t wait till the last moment. Handmade work needs time, and early requests get smoother guidance.
</div>
```

Better version:

```html
<div class="premium-fomo">
  Handmade slots are limited because every artwork needs time. If this is for a birthday, anniversary, farewell, or surprise gift, reserving early makes the final piece feel more thoughtful.
</div>
```

Or more emotional:

```html
<div class="premium-fomo">
  The best gifts do not feel rushed. If this memory matters, start early so we can choose the right photo, size, and details properly.
</div>
```

---

# 23. How To Change The Logo

Your page uses:

```html
<img src="logo.png" alt="MalayPaul Arts Logo">
```

So the easiest way:

1. Rename your logo file to:

```txt
logo.png
```

2. Put it in the same folder as `order.html`.

3. Refresh the browser.

Do not change code if your file is named `logo.png`.

If your logo is named something else, for example:

```txt
my-logo.png
```

then change:

```html
<img src="logo.png" alt="MalayPaul Arts Logo">
```

to:

```html
<img src="my-logo.png" alt="MalayPaul Arts Logo">
```

---

# 24. How To Change Support QR Image

Search:

```html
support-qr.png
```

You will see:

```html
<img src="support-qr.png" alt="Support QR Code">
```

To change QR:

1. Put your QR image in the same folder.
2. Rename it:

```txt
support-qr.png
```

No code change needed.

If your QR file has a different name, change the `src`.

Example:

```html
<img src="my-upi-qr.png" alt="Support QR Code">
```

---

# 25. How To Edit Navbar Links

Search:

```html
<div class="menu"
```

You will see links like:

```html
<a href="index.html">Home</a>
<a href="order.html">Order</a>
<a href="gallery.html">Gallery</a>
<a href="contact.html">Contact</a>
```

To rename a tab:

```html
<a href="gallery.html">Gallery</a>
```

to:

```html
<a href="gallery.html">Works</a>
```

To change where it goes, edit `href`.

Example:

```html
<a href="gallery.html">Works</a>
```

The visible word is between the tags:

```html
Works
```

The destination is inside:

```html
href="gallery.html"
```

---

# 26. How To Change Fonts

Your fonts are loaded near the top:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=Playfair+Display:wght@500;600;700;800&display=swap" rel="stylesheet">
```

And used like this:

```css
font-family: 'Poppins', sans-serif;
```

and:

```css
font-family: 'Playfair Display', serif;
```

For your current premium style, keep these. They already match the website.

---

# 27. How To Change Colours

Search:

```css
:root
```

You will see colour variables like:

```css
:root {
  --cream: #fffaf3;
  --text: #2f2420;
  --muted: #7a6258;
  --gold: #b08968;
  --gold-dark: #8f5f3b;
}
```

Change colours here instead of changing 100 places.

Example: make gold darker:

```css
--gold: #9f724e;
```

Make text darker:

```css
--text: #211713;
```

Do not overdo colours. Your current palette is already premium.

---

# 28. How To Make The Popular Badge Look Cleaner

Search:

```css
.popular-ribbon
```

If the badge is too big or badly aligned, use this safer version:

```css
.popular-ribbon {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 8px 14px;
  border-radius: 999px;
  background: linear-gradient(135deg, #fff7ea 0%, #d2a06f 42%, #7f4f2f 100%);
  color: white;
  text-shadow: 0 1px 6px rgba(47,36,32,0.28);
  font-size: 11px;
  font-weight: 900;
  letter-spacing: 0.35px;
  white-space: nowrap;
  box-shadow: 0 12px 28px rgba(143,95,59,0.24);
  z-index: 3;
}
```

If it still feels too high, change:

```css
top: 0;
```

to:

```css
top: 6px;
```

and remove the `-50%` vertical lift:

```css
transform: translateX(-50%);
```

---

# 29. How To Make Cards More Spacious

Search:

```css
.size-option > span
```

You may see:

```css
.size-option > span {
  min-height: 166px;
  padding: 28px 20px 22px;
}
```

To make cards taller:

```css
min-height: 185px;
```

To make cards less cramped:

```css
padding: 34px 22px 24px;
```

Better:

```css
.size-option > span {
  position: relative;
  display: block;
  min-height: 185px;
  padding: 34px 22px 24px;
  border-radius: 28px;
}
```

---

# 30. How To Make The Website Safer From Mistakes

Before editing:

1. Right click `order.html`
2. Click copy
3. Paste in same folder
4. Rename backup:

```txt
order-backup.html
```

Then edit only:

```txt
order.html
```

If something breaks, open backup and copy the working part back.

---

# 31. Common Mistakes And Fixes

## Mistake 1: Total not changing after price edit

You probably changed only visible price:

```html
<strong>₹999</strong>
```

but forgot:

```html
data-price="999"
```

Fix both.

---

## Mistake 2: Coupon breaks the page

Most likely missing comma.

Wrong:

```js
"GIFT15": {
  type: "percent",
  value: 15,
  message: "15% discount applied."
}
"SAVE200": {
  type: "flat",
  value: 200,
  message: "₹200 discount applied."
}
```

Correct:

```js
"GIFT15": {
  type: "percent",
  value: 15,
  message: "15% discount applied."
},
"SAVE200": {
  type: "flat",
  value: 200,
  message: "₹200 discount applied."
}
```

---

## Mistake 3: WhatsApp button stopped working

You probably removed:

```html
onclick="orderNow()"
```

Button should look like:

```html
<button class="main-btn" onclick="orderNow()">Send to WhatsApp</button>
```

---

## Mistake 4: Popular badge not showing

You need both:

```html
<label class="size-option featured-size">
```

and:

```html
<span class="popular-ribbon">★ Most Popular</span>
```

If one is missing, it will not look right.

---

## Mistake 5: Page opens with wrong default size

Find all size inputs and make sure only one has:

```html
checked
```

---

## Mistake 6: Artwork add-on total wrong

You changed:

```html
<div class="art-price">+₹500</div>
```

but forgot:

```html
data-price="500"
```

Change both.

---

# 32. Testing Checklist After Every Edit

After editing, save:

```txt
Ctrl + S
```

Then open `order.html` in browser and test:

- [ ] Page loads without broken layout
- [ ] Size selection works
- [ ] Artwork add-on selection works
- [ ] Total updates correctly
- [ ] Coupon works
- [ ] Wrong coupon shows error
- [ ] WhatsApp opens
- [ ] WhatsApp message includes correct details
- [ ] Mobile view still looks good
- [ ] Popular badge is aligned
- [ ] Only one size is selected by default

---

# 33. Quick Search Cheat Sheet

| What You Want To Edit | Search This |
|---|---|
| Size cards | `name="size"` |
| Popular badge | `popular-ribbon` |
| Featured popular style | `featured-size` |
| Size price | `data-price` |
| Artwork options | `name="artType"` |
| Coupon codes | `const COUPONS` |
| WhatsApp number | `WHATSAPP_NUMBER` |
| WhatsApp message | `orderNow()` |
| Live summary | `updateSummary()` |
| Final price text | `finalPrice` |
| Upload input | `referenceFile` |
| Support QR | `support-qr.png` |
| Logo | `logo.png` |
| Navbar | `<nav` |
| Main button | `main-btn` |

---

# 34. My Recommended Final Setup

If you want a premium but not overpriced setup, use this:

## Sizes

```txt
Small  - ₹699
Medium - ₹999  Most Popular
Large  - ₹1599
XL     - ₹2199
```

## Add-ons

```txt
Single Face        Base
2 Face Portrait    +₹350
3 Face Portrait    +₹550
4 Face Portrait    +₹750
Couple Heart       +₹450
Pet Portrait       +₹350
Name/Text          +₹200
Logo/Brand         +₹700
Custom             +₹400
```

## Coupons

```txt
MALAY10    10% off
GIFT15     15% off
SAVE200    ₹200 off
FIRST100   ₹100 off
COUPLE15   15% off
```

## Popular size

Use Medium as most popular if you want more orders.

Use Large as most popular if you want higher average order value.

---

# 35. Tiny Mental Model

Think of your order page like this:

```txt
Customer clicks size
        ↓
Website reads data-price from size
        ↓
Customer clicks artwork type
        ↓
Website reads data-price from artwork
        ↓
Customer enters coupon
        ↓
JavaScript checks const COUPONS
        ↓
updateSummary() refreshes the total
        ↓
orderNow() sends everything to WhatsApp
```

So whenever something goes wrong, check the exact part in that chain.

---

# 36. Emergency Fix: Reset Coupon Section

If coupons break badly, replace your coupon section with this clean version:

```js
const COUPONS = {
  "MALAY10": {
    type: "percent",
    value: 10,
    message: "10% discount applied."
  },
  "ART100": {
    type: "flat",
    value: 100,
    message: "₹100 discount applied."
  },
  "GIFT15": {
    type: "percent",
    value: 15,
    message: "15% discount applied."
  }
};
```

Then save and refresh.

---

# 37. Emergency Fix: Reset One Size Card

If one size card breaks, replace it with this:

```html
<label class="size-option">
  <input type="radio" name="size" value="Large - 16 x 20 inch" data-price="1499" onchange="updateSummary()">
  <span>
    <div>
      <b>Large</b>
      <small>16 x 20 inch<br>Best for detailed wall art.</small>
    </div>
    <strong>₹1499</strong>
  </span>
</label>
```

If you want it popular:

```html
<label class="size-option featured-size">
  <input type="radio" name="size" value="Large - 16 x 20 inch" data-price="1499" checked onchange="updateSummary()">
  <span>
    <span class="popular-ribbon">★ Most Popular</span>
    <div>
      <b>Large</b>
      <small>16 x 20 inch<br>Best for detailed wall art.</small>
    </div>
    <strong>₹1499</strong>
  </span>
</label>
```

---

# 38. Emergency Fix: Reset WhatsApp Number

```js
const WHATSAPP_NUMBER = "918087827454";
```

Replace with your real number using this format:

```js
const WHATSAPP_NUMBER = "91XXXXXXXXXX";
```

---

# 39. Final Advice

Do not edit too many things at once.

Best workflow:

```txt
Change one thing
Save
Refresh browser
Test
Then change next thing
```

That way if something breaks, you know exactly what caused it.
