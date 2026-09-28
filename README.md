# 🛍️ Shop — React Context Practice

A modern single-page shopping application built with **React 19, Vite, and Tailwind CSS**. This project was created primarily to practice **React Context**, `useContext`, `useState`, and custom Hooks while building a realistic e-commerce interface.

## 🚀 Live Demo

[View Live Demo](#)

## 📂 Repository

[View on GitHub](#)

---

## ✨ Features

* 🛍️ Product browsing
* 🛒 Add products to cart
* 🗑️ Remove products from cart
* 🧹 Clear the entire cart
* 💰 Automatic cart total
* 🔢 Cart item count
* 📱 Responsive design
* 🛒 Slide-out shopping cart
* 🎨 Modern Tailwind CSS interface
* ⚛️ React Context for shared cart state
* 🪝 Custom `useCart()` Hook
* 📄 Single-page application

---

## 🧠 React Concepts Practiced

The main purpose of this project is practicing **React Context**.

### Context

The shopping cart state is managed by `CartProvider`:

```jsx
<CartProvider>
  <App />
</CartProvider>
```

The provider makes the following values available to descendant components:

```js
{
  cart,
  addToCart,
  removeFromCart,
  clearCart,
  cartCount,
  cartTotal
}
```

### Custom Hook

Components access the Context through:

```jsx
const { cart, addToCart } = useCart();
```

instead of repeatedly writing:

```jsx
useContext(CartContext);
```

### Shared State

Different components consume the same cart state:

```text
CartProvider
     │
     ▼
 CartContext
     │
 ┌───┼─────────────┐
 ▼   ▼             ▼
Header ProductCard CartDrawer
                  │
                  ▼
               CartItem
```

This allows components at different levels of the component tree to communicate without passing cart-related props through every intermediate component.

---

## 🛠️ Technologies

* **React 19**
* **Vite**
* **Tailwind CSS v4**
* **JavaScript (JSX)**
* **React Context API**
* **React Hooks**

---

## 📁 Project Structure

```text
src/
├── components/
│   ├── Header.jsx
│   ├── Hero.jsx
│   ├── ProductCard.jsx
│   ├── ProductGrid.jsx
│   ├── CartDrawer.jsx
│   ├── CartItem.jsx
│   └── Footer.jsx
│
├── context/
│   └── CartContext.jsx
│
├── data/
│   └── products.js
│
├── App.jsx
├── index.css
└── main.jsx
```

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project

```bash
cd shop
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
npm run dev
```

Open the local URL provided by Vite in your browser.

---

## 🎯 Learning Goal

This project is intentionally designed as a **React Context practice project** rather than a production e-commerce application.

The main learning objectives are:

* Understand `createContext()`
* Understand Context providers
* Understand `useContext()`
* Share state between components
* Avoid unnecessary prop drilling
* Create and use custom Hooks
* Understand how state changes propagate through Context
* Combine Context with `useState()`

---

## 🔮 Possible Future Improvements

* Product search
* Product filtering
* Product categories
* Quantity controls
* Persistent cart with `localStorage`
* Product details
* Checkout page
* Authentication
* Backend API
* Database integration
* Payment processing

---

## 👨‍💻 Author

**Shukrullah Shirzad**

Learning and building with React, JavaScript, Tailwind CSS, and modern web technologies.
