# TechStore - E-Commerce Shopping Cart

A minimal **e-commerce application** built with **React (frontend)** and **Node.js + Express + TypeScript (backend)**.  
Users can browse products, add them to a cart, and checkout. Cart state persists in `localStorage`.

---

## GitHub Repository

You can find the full source code and project repository at:  
https://github.com/yourusername/techstore

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

---

## Running the Application

### Backend
```bash
cd backend
npm run dev
```
Runs the backend server with hot reload on port 3000 by default.

### Frontend
```bash
cd frontend
npm run dev
```
Runs the frontend development server with hot reload on port 5173 by default.

---

## Running Tests

### Backend Tests
```bash
cd backend
npm test
```
Runs Jest tests for backend API endpoints including `/products` and `/checkout`.

### Frontend Tests
Currently, no frontend tests are included.

---

## Design Choices

- The backend uses hardcoded product data for simplicity and demonstration purposes.
- Cart state is managed on the client side and persisted in `localStorage` to maintain state across sessions.
- The checkout endpoint logs orders but does not process payments or persist orders.
- The frontend uses React with TailwindCSS for styling and Lucide React Icons for UI icons.
- The backend is built with Express and TypeScript, with Jest and Supertest for testing.
- The project is structured to separate frontend and backend concerns clearly.

---

## Screenshots

![Screenshot 1](https://drive.google.com/uc?export=view&id=1u_-mVHQoGWFuhVdC5oL1DLZyfxCpLzfY)

![Screenshot 2](https://drive.google.com/uc?export=view&id=1r4OUAWCLRI6oMnJevKQGketH1TZMxoYj)

---

## License

This project is licensed under the MIT License.
