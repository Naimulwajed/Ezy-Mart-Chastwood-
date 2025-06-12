<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ezy Mart Chastwood</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
    }
    header {
      background-color: #004aad;
      color: white;
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    header img {
      height: 50px;
    }
    nav a {
      color: white;
      margin-left: 20px;
      text-decoration: none;
      font-weight: bold;
    }
    .hero {
      background-color: #fff;
      text-align: center;
      padding: 3rem 1rem;
    }
    .hero h1 {
      color: #ff9900;
      font-size: 2.5rem;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
      padding: 2rem;
    }
    .product {
      background-color: white;
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 1rem;
      text-align: center;
    }
    .product h3 {
      color: #004aad;
    }
    .product button {
      margin-top: 10px;
      padding: 8px 16px;
      background-color: #004aad;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    .contact, .store-locator, .cart {
      background-color: white;
      margin: 2rem;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    .contact form input, .contact form textarea {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .contact form button {
      padding: 10px 20px;
      background-color: #004aad;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    .cart ul {
      list-style: none;
      padding: 0;
    }
    .cart li {
      margin-bottom: 10px;
    }
    footer {
      background-color: #004aad;
      color: white;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }
  </style>
</head>
<body>
  <header>
    <img src="Screenshot_2025-06-13-00-34-01-37_6012fa4d4ddec268fc5c7112cbb265e7.jpg" alt="Ezy Mart Logo" />
    <nav>
      <a href="#">Home</a>
      <a href="#products">Products</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
      <a href="#store-locator">Store Locator</a>
      <a href="#cart">Cart</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Welcome to Ezy Mart Chastwood</h1>
    <p>Your friendly neighborhood convenience store</p>
  </section>

  <section class="products" id="products">
    <div class="product">
      <h3>Snacks</h3>
      <p>Big Takis $13.99</p>
      <p>Small Takis $7.50</p>
      biscuits, chocolates & more!</p>
      <button onclick="addToCart('Snacks')">Add to Cart</button>
    </div>
    <div class="product">
      <h3>Drinks</h3>
      <p>Soft drinks, juices, bottled water, etc.</p>
      <button onclick="addToCart('Drinks')">Add to Cart</button>
    </div>
    <div class="product">
      <h3>Groceries</h3>
      <p>Daily essentials and pantry items.</p>
      <button onclick="addToCart('Groceries')">Add to Cart</button>
    </div>
    <div class="product">
      <h3>Personal Care</h3>
      <p>Toiletries and hygiene products.</p>
      <button onclick="addToCart('Personal Care')">Add to Cart</button>
    </div>
  </section>

  <section class="contact" id="contact">
    <h2>Contact Us 0493289550</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea rows="4" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <section class="store-locator" id="store-locator">
    <h2>Store Locator</h2>
    <p>Find your nearest Ezy Mart store on Google Maps:</p>
    <iframe src="[https://www.google.com/maps/embed/v1/search?key=YOUR_GOOGLE_MAPS_API_KEY&q=Ezy+Mart+Chastwood](https://g.co/kgs/G7ojQPM)" width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
  </section>

  <section class="cart" id="cart">
    <h2>Your Cart</h2>
    <ul id="cart-items"></ul>
    <p id="empty-cart">Your shopping cart is currently empty.</p>
  </section>

  <footer>
    <p>&copy; 2025 Ezy Mart Chastwood. All rights reserved.</p>
  </footer>

  <script>
    const cart = [];

    function addToCart(item) {
      cart.push(item);
      updateCart();
    }

    function updateCart() {
      const cartItems = document.getElementById('cart-items');
      const emptyCartMsg = document.getElementById('empty-cart');
      cartItems.innerHTML = '';

      if (cart.length === 0) {
        emptyCartMsg.style.display = 'block';
      } else {
        emptyCartMsg.style.display = 'none';
        cart.forEach((item, index) => {
          const li = document.createElement('li');
          li.textContent = item;
          cartItems.appendChild(li);
        });
      }
    }
  </script>
</body>
</html>
