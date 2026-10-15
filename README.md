# Peakline Fitness: gym website concept

A concept website for a neighbourhood gym: a live class board, membership plans, a weekly timetable, a protein and gym shop with a cart, and WhatsApp ordering.

**This is a portfolio concept project.** The business name, prices, hours, class times, products, address and coupon code are sample content. It is not a real gym or store.

**Live demo:** add your link here after you deploy (see "Put it online" below).

## What it does

- **Live class board in the hero.** Shows today's classes, whether the gym is open right now, which class is live, and a countdown to the next one. A day strip shows the classes laid out across opening hours with a marker for the current time. It updates every 30 seconds.
- **Membership plans** with a Monthly, 3-month and 12-month toggle. The per-month price, billed total and amount saved update, and the numbers animate. "Choose" on a plan fills the plan into the trial form.
- **Weekly timetable** with colour-coded class types and today's row highlighted. Tapping a class adds it to the free-trial request.
- **Protein and gym shop** with category filters, search and a flavour choice per product.
- **Cart drawer** with quantity controls, a free-delivery progress bar, a sample coupon (`FIRST10`), and a delivery rule (free above ₹1,500, otherwise ₹60). The cart is saved in the browser and survives a refresh.
- **WhatsApp checkout** that validates name, an Indian mobile number (10 digits, starting 6 to 9, `+91` and spaces accepted) and address, then opens WhatsApp with an itemised order message and a reference code.
- **Free-trial form** that opens WhatsApp with the details filled in.
- **Demo mode.** While no real WhatsApp number is set, the buttons show a message preview instead of opening a broken link. Visitors can see exactly what the gym would receive.
- **Visit and FAQ sections** with opening hours (today highlighted), address and a WhatsApp button.
- **Accessibility basics:** skip link, visible keyboard focus on every surface, labelled controls, the page behind the cart is locked while it is open, Escape closes the cart, text contrast of at least 4.5 to 1, and a layout that works down to phone width.
- **Motion kept small:** one entrance on load (headline and board), plus motion that answers a tap: price count, fly-to-cart, product tilt on hover. All of it is switched off for visitors who prefer reduced motion.

## Tech

One file: HTML, CSS and vanilla JavaScript. No framework, no build step, no dependencies. Product visuals are inline SVG illustrations. Fonts (Big Shoulders Display and Instrument Sans) load from Google Fonts, with system fallbacks if they cannot load.

## Make it your own

Everything you normally change is at the top of the `<script>` in `index.html`:

- `GYM.whatsapp`: the WhatsApp number that receives orders, country code first, digits only, for example `919876543210`. **This is the number used by every WhatsApp button.** Until you replace the `91XXXXXXXXXX` placeholder, the site stays in demo mode.
- `GYM.address` and `GYM.mapsUrl`: the address text, and an optional Google Maps link that adds a "Get directions" button.
- `P`: the product list (name, category, price, flavours, colour).
- `PLANS` and `OFF`: the membership plans and the 3-month and 12-month discounts.
- `A`, `B`, `SAT`, `SUN`, `HOURS`: the timetable and opening hours. Times are written as `S("18:00", "HIIT", "hiit")`.

The mobile number a customer types in the cart is their own number. It is not the gym's number.

## Put it online (free)

This is a static site, so it needs static hosting. It does not need Streamlit, which is for Python apps.

**GitHub Pages**

1. Create a new public repository, for example `peakline-fitness`.
2. Upload `index.html` and `README.md`. The file must be named exactly `index.html`.
3. Open Settings, then Pages. Under Build and deployment, choose "Deploy from a branch", branch `main`, folder `/ (root)`, and save.
4. After a minute or two the site is live at `https://YOUR-USERNAME.github.io/peakline-fitness/`.

**Netlify Drop (fastest)**

Put `index.html` in a folder, open app.netlify.com/drop and drag the folder in. You get a live link immediately.

## Limitations

- There is no payment gateway and no server. Orders are sent as WhatsApp messages, and payment is arranged separately.
- Products and prices are sample data. A real store needs accurate nutrition labels and the licences that food regulations require.
- A real shop with online payment and stock tracking would use a platform such as Shopify or WooCommerce, or a custom backend.

## Screenshots

Add screenshots to an `images` folder and link them here. Good ones to take: the hero with the live board, the plans section, the shop, and the cart drawer, plus one on a phone.
