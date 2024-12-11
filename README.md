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
