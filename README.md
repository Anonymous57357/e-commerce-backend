# e-commerce-backend

# Step 1: Project Initialization

## Objective
Set up the project structure and connect to MongoDB.

## Steps
1. **Initialize the Project**:
   - Run `npm init -y` to create a new Node.js project.
   - Install necessary dependencies:
     ```
     npm install express mongoose dotenv body-parser cookie-parser express-session
     ```

2. **Create Folder Structure**:
e-commerce-backend/
├── config/
│   └── db.js
├── models/
│   ├── user.js
│   └── product.js
├── routes/ 
│   ├── userRoutes.js
│   └── productRoutes.js
├── controllers/
│   ├── userController.js
│   └── productController.js
├── app.js
└── .env



3. **Database Connection**:
- Use Mongoose to connect to MongoDB in `config/db.js`.

4. **Environment Variables**:
- Add `.env` file to store sensitive configuration.

5. **Setup `app.js`**:
- Configure middleware for body parsing, cookies, and sessions.
- Import routes and start the server.

## Outcome
- A running Express server connected to MongoDB.
- Ready to add features like User Management and Product Management.

## Commands
To start the server:
```bash
node app.js

# Step 2: User Management

## Objective
Implement user registration, login, and logout using session-based authentication.

## Steps

### 1. Install Dependencies
Install bcrypt for secure password hashing:
```bash
npm install bcrypt

# Step 3: Product Management

## Objective
Implement CRUD operations for products.

## Steps

### 1. Create Product Model
Define the `Product` schema in `models/product.js`:
- Fields: `name`, `description`, `price`, `stock`.
- Include validation and default timestamps.

---

### 2. Create Product Controller
In `controllers/productController.js`, implement:
- **Create Product**:
  - Validate input fields.
  - Save the product to the database.
- **Get All Products**:
  - Fetch all products from the database.
- **Get Product by ID**:
  - Fetch a product using its unique ID.
- **Update Product**:
  - Update a product’s details by ID.
- **Delete Product**:
  - Remove a product from the database by ID.

---

### 3. Create Product Routes
Define the routes in `routes/productRoutes.js`:
- `POST /`: Create a new product.
- `GET /`: Get all products.
- `GET /:id`: Get a single product by ID.
- `PUT /:id`: Update a product by ID.
- `DELETE /:id`: Delete a product by ID.

---

### 4. Test the APIs
Use tools like **Postman** to test the following:
1. **Create Product**:
   - URL: `/api/products`
   - Method: `POST`
   - Body:
     ```json
     {
       "name": "Laptop",
       "description": "A powerful gaming laptop",
       "price": 1500,
       "stock": 10
     }
     ```
   - Expected Response:
     ```json
     {
       "message": "Product created successfully",
       "product": { /* product details */ }
     }
     ```

2. **Get All Products**:
   - URL: `/api/products`
   - Method: `GET`
   - Expected Response: List of products.

3. **Get Product by ID**:
   - URL: `/api/products/:id`
   - Method: `GET`
   - Expected Response: Product details.

4. **Update Product**:
   - URL: `/api/products/:id`
   - Method: `PUT`
   - Body:
     ```json
     {
       "price": 1200,
       "stock": 15
     }
     ```
   - Expected Response:
     ```json
     {
       "message": "Product updated successfully",
       "product": { /* updated product details */ }
     }
     ```

5. **Delete Product**:
   - URL: `/api/products/:id`
   - Method: `DELETE`
   - Expected Response:
     ```json
     {
       "message": "Product deleted successfully"
     }
     ```

---

## Outcome
- Product CRUD APIs are functional.
- Products can be added, updated, retrieved, and deleted.

