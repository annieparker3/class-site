Role: Expert Frontend Developer & UI/UX Designer

Task: Create a workable, responsive e-commerce fashion UI using only HTML and CSS. No JavaScript allowed. Use modern CSS layouts (Flexbox and Grid). name it StyleUp

Design Aesthetic: Minimalist, elegant, and modern. Use a clean color palette (white backgrounds, deep purple/indigo accents for buttons/links, and sleek dark text).

Structure & Requirements:

    Header & Navigation Bar:

        Must be fully responsive. On desktop, show a horizontal menu with links: Home, Tops, Pants, Skirts, Shoes, Jewelry, Payment.

        Include a clean logo placeholder on the left and a shopping cart icon/placeholder on the right.

        On mobile screens, ensure the menu stacks neatly or uses a pure CSS dropdown/toggle method (like the checkbox hack or <details> tag) to keep it responsive without JS.

    Hero Section (Home Interface):

        A full-width or elegant split-screen hero section.

        Include a bold, stylish heading welcoming users to the fashion site, a short, catchy paragraph describing the brand's vibe, and a "Shop Now" call-to-action button.

    Product Categories Grid:

        Below the hero section, create a responsive CSS Grid showcasing card placeholders for the core categories: Tops, Pants, Skirts, Shoes, and Jewelry.

        Each card should have a placeholder box for an image and a stylish text label overlay or caption underneath.

    Payment Process Interface:

        A clean checkout/payment section placed lower on the page (or styled as a visible section) featuring a sleek summary box on one side and a stylized credit card/billing form on the other.

        Use standard HTML5 validation (required attributes) so the form feels functional when trying to submit.

Output: Provide clean, semantic, well-commented HTML5 and a single, organized CSS stylesheet containing fluid typography and media queries for flawless mobile responsiveness.


organize your files like this:
Plaintext

fashion-site/
│
├── css/
│   └── style.css       <-- One stylesheet to rule them all
│
├── index.html          <-- Home Interface (About the site)
├── tops.html           <-- Tops Category
├── pants.html          <-- Pants Category
├── skirts.html         <-- Skirts Category
├── shoes.html          <-- Shoes Category
├── jewelry.html        <-- Jewelry Category
└── payment.html        <-- Payment/Checkout Process

2. The Core Setup for Every Page

Every single HTML file needs to link to your central stylesheet in the <head> section.

Here is the starter template for your index.html (Home page). You can duplicate this structure for the other pages, just changing the content inside the <main> tag.
index.html (The Home Interface)
HTML

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sleek Fashion - Home</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

  <header class="site-header">
    <div class="logo">MODERN FASHION</div>
    
    <input type="checkbox" id="nav-toggle" class="nav-toggle">
    <label for="nav-toggle" class="nav-toggle-label">
      <span></span>
    </label>

    <nav class="navbar">
      <ul>
        <li><a href="index.html" class="active">Home</a></li>
        <li><a href="tops.html">Tops</a></li>
        <li><a href="pants.html">Pants</a></li>
        <li><a href="skirts.html">Skirts</a></li>
        <li><a href="shoes.html">Shoes</a></li>
        <li><a href="jewelry.html">Jewelry</a></li>
        <li><a href="payment.html">Payment</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero-section">
      <h1>Elegance In Every Detail</h1>
      <p>Welcome to Modern Fashion. We curate minimalist, high-quality wardrobe essentials designed to elevate your everyday style. Explore our collections or proceed straight to checkout.</p>
      <a href="tops.html" class="cta-button">Explore Collections</a>
    </section>
  </main>

</body>
</html>

3. How to Create the Other Pages

To build the rest of your site, copy the code above, create a new file (e.g., payment.html), and swap out the <main> section.
For payment.html:

Replace the <main> section with your checkout form layout:
HTML

  <main class="payment-container">
    <h2>Complete Your Purchase</h2>
    <form class="payment-form">
      <div class="form-group">
        <label for="card-name">Name on Card</label>
        <input type="text" id="card-name" required placeholder="John Doe">
      </div>
      <div class="form-group">
        <label for="card-num">Card Number</label>
        <input type="text" id="card-num" required placeholder="1234 5678 9101 1121">
      </div>
      <button type="submit" class="submit-btn">Pay Now</button>
    </form>
  </main>

For Category Pages (tops.html, pants.html, etc.):

Replace the <main> section with a clean CSS Grid to display your products:
HTML

  <main>
    <h2 class="page-title">Shop Tops</h2>
    <div class="product-grid">
      <div class="product-card">
        <div class="image-placeholder"></div>
        <h3>Classic Silk Blouse</h3>
        <p>$85.00</p>
      </div>
      <div class="product-card">
        <div class="image-placeholder"></div>
        <h3>Oversized Linen Shirt</h3>
        <p>$60.00</p>
      </div>
    </div>
  </main>

4. The Global CSS Starter (css/style.css)

Here is a foundational blueprint for your CSS to handle the layout, a modern dark-purple/indigo color scheme, and the responsive navigation bar without using JavaScript.
CSS

/* --- Global Styles & Variables --- */
:root {
  --bg-color: #ffffff;
  --text-color: #111111;
  --accent-purple: #4B0082; /* Deep Indigo/Purple */
  --accent-hover: #310054;
  --gray-light: #f8f9fa;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
  background-color: var(--bg-color);
  color: var(--text-color);
}

/* --- Header & Responsive Navbar (Flexbox) --- */
.site-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 5%;
  background-color: #fff;
  border-bottom: 1px solid #eee;
  position: sticky;
  top: 0;
  z-index: 1000;
}

.logo {
  font-weight: 700;
  font-size: 1.5rem;
  letter-spacing: 2px;
}

.navbar ul {
  display: flex;
  list-style: none;
  gap: 20px;
}

.navbar a {
  text-decoration: none;
  color: var(--text-color);
  font-weight: 500;
  transition: color 0.3s;
}

.navbar a:hover, .navbar a.active {
  color: var(--accent-purple);
}

/* Hide mobile toggle elements by default */
.nav-toggle, .nav-toggle-label {
  display: none;
}

/* --- Hero Section Styling --- */
.hero-section {
  max-width: 800px;
  margin: 100px auto;
  text-align: center;
  padding: 0 20px;
}

.hero-section h1 {
  font-size: 3rem;
  margin-bottom: 20px;
}

.hero-section p {
  font-size: 1.2rem;
  color: #555;
  margin-bottom: 40px;
  line-height: 1.6;
}

.cta-button, .submit-btn {
  display: inline-block;
  background-color: var(--accent-purple);
  color: #fff;
  padding: 12px 30px;
  text-decoration: none;
  border-radius: 4px;
  font-weight: 600;
  transition: background-color 0.3s;
  border: none;
  cursor: pointer;
}

.cta-button:hover, .submit-btn:hover {
  background-color: var(--accent-hover);
}

/* --- Responsive Media Query (The Mobile Magic) --- */
@media (max-width: 768px) {
  .nav-toggle-label {
    display: block;
    cursor: pointer;
  }

  .nav-toggle-label span,
  .nav-toggle-label span::before,
  .nav-toggle-label span::after {
    display: block;
    background: var(--text-color);
    height: 2px;
    width: 25px;
    position: relative;
    transition: all 0.3s;
  }

  .nav-toggle-label span::before { content: ''; top: -8px; }
  .nav-toggle-label span::after { content: ''; top: 6px; }

  /* Hide the navbar off-screen on mobile */
  .navbar {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: #fff;
    transform: scale(1, 0);
    transform-origin: top;
    transition: transform 0.3s ease-in-out;
    border-bottom: 1px solid #eee;
  }

  .navbar ul {
    flex-direction: column;
    padding: 20px;
    gap: 15px;
  }

  /* When the hidden checkbox is checked, reveal the menu */
  .nav-toggle:checked ~ .navbar {
    transform: scale(1, 1);
  }
}

now i want you to pick mock images from pixabay to fit all the pages so if its tops, get tops from pixabay for the tops pages, same goes for all

preview the interface