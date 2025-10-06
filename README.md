# TechStore - E-Commerce Shopping Cart

A minimal **e-commerce application** built with **React (frontend)** and **Node.js + Express + TypeScript (backend)**.  
Users can browse products, add them to a cart, and checkout. Cart state persists in `localStorage`.

---

## Table of Contents
- [Project Goal](#project-goal)
- [Core Features](#core-features)
- [Bonus Features](#bonus-features-%e2%9c%a8)
- [Tech Stack](#tech-stack)
- [Setup & Installation](#setup--installation)
- [Running the Application](#running-the-application)
- [Running Tests](#running-tests)
- [Design Choices](#design-choices)
- [Screenshots](#screenshots)
- [License](#license)

---

## Project Goal

A minimal e-commerce site to list products and manage a shopping cart.  
The backend provides APIs for products and checkout, while the frontend displays products, manages cart state, and communicates with the backend.

---

## Core Features

### Backend
1. `/api/products` - Returns a hardcoded list of products (id, name, price, imageUrl, description).  
2. `/api/checkout` - Accepts a list of product IDs and quantities, logs the order, and returns a success response.  

### Frontend
1. Fetch and display products in a grid.  
2. "Add to Cart" functionality for each product.  
3. Manage cart state on the client side.  
4. Cart modal showing items, quantities, and total price.  
5. "Checkout" button sends cart data to backend endpoint.  

---

## Bonus Features ✨
- Change quantity of items in cart.  
- Persist cart contents in `localStorage`.  
- Backend test cases for `/products` and `/checkout` endpoints.  

---

## Tech Stack

- **Frontend:** React, TypeScript, TailwindCSS, Lucide React Icons  
- **Backend:** Node.js, Express, TypeScript, Jest, Supertest  
- **Tools:** npm, ts-node-dev  

---

## Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/techstore.git
cd techstore
```
### Backend Setup
```bash
cd backend
npm install
```
### Frontend Setup
```bash
cd ../frontend
npm install
```
