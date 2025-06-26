# 📦 Week 2 Express.js Assignment

This project is a fully functional **Express.js API** for managing a collection of products. It includes RESTful routes, custom middleware, validation, filtering, and pagination — all using an in-memory JavaScript array.

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-github-repo-url>
cd week-2-express-js-assignment
```

### 2. Install dependencies

```bash
npm install
```

### 3. Start the server

```bash
npm run dev      # Starts with nodemon (development)
# or
npm start        # Starts with node
```

Server runs on:

```
http://localhost:3000
```

---

## 📚 API Documentation

### ✅ Root Endpoint

* `GET /`

  * Returns welcome message.

### 📦 Products Endpoints

#### Get all products

* `GET /api/products`
* Optional Query:

  * `category`: filter by category
  * `page`, `limit`: pagination

#### Get product by ID

* `GET /api/products/:id`

#### Create a product

* `POST /api/products`
* Headers: `x-api-key: your_api_key`
* Body:

```json
{
  "name": "Product Name",
  "description": "Some description",
  "price": 123.45,
  "category": "electronics",
  "inStock": true
}
```

#### Update product

* `PUT /api/products/:id`
* Headers: `x-api-key: your_api_key`
* Body: Same as POST

#### Delete product

* `DELETE /api/products/:id`

#### Product statistics

* `GET /api/products/stats`
* Returns product count per category.

---

## 🔐 Middleware Used

### Logger Middleware

Logs HTTP method, URL, and timestamp of every request.

### Authentication Middleware

Checks for `x-api-key` in headers. Blocks unauthorized requests.

### Validation Middleware

Ensures product fields are valid before creation/update.

---

## 🧪 Testing Tools

* [Postman](https://www.postman.com/)
* [Insomnia](https://insomnia.rest/)
* `curl`

---

## 📁 Project Structure

```
week-2-express-js-assignment/
├── server.js
├── package.json
├── middleware/
│   ├── auth.js
│   ├── logger.js
│   └── validate.js
├── README.md
└── .env.example
```

---

## 🧩 Environment Variables

Create a `.env` file based on this example:

**.env.example**

```
API_KEY=your_api_key
PORT=3000
```

---

## 👨‍🏫 Instructor Notes

* Built using Express.js and in-memory data.
* API is secure, validated, and production-friendly.

---

## 🧠 Author

Norman Wayaya (Sci-Norman)
