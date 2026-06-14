# Smart Inventory Management System
## MongoDB Atlas + Node.js Backend

✅ **Backend created successfully!**

---

## 🚀 Quick Start

### If Someone Wants To Connect Their Own Database

1. Copy `.env.example` to `.env`
2. Set `DISABLE_MONGODB=false`
3. Set your own `MONGODB_URI`
4. Set your own `JWT_SECRET`
5. Run `npm start`

The app will then connect to that person's MongoDB database.

### 1. Setup MongoDB Atlas

1. Go to https://www.mongodb.com/cloud/atlas
2. Create a **FREE** account
3. Create a new cluster (choose Free M0 tier)
4. Create database user with username & password
5. Add your IP to whitelist (or use 0.0.0.0/0 for testing)
6. Get your connection string

### 2. Configure Connection

Edit the `.env` file and add your MongoDB Atlas connection string:

```env
MONGODB_URI=mongodb+srv://YOUR_USERNAME:YOUR_PASSWORD@YOUR_CLUSTER.mongodb.net/smart_inventory?retryWrites=true&w=majority
```

Replace:
- `YOUR_USERNAME` - your MongoDB username
- `YOUR_PASSWORD` - your MongoDB password  
- `YOUR_CLUSTER` - your cluster URL (e.g., cluster0.abc123)

### 3. Start the Server

```bash
npm start
```

The server will:
- ✅ Connect to MongoDB Atlas
- ✅ Create sample data automatically
- ✅ Start on http://localhost:3000

### 4. Access the Application

Open your browser: **http://localhost:3000**

Create your own account from the **Create one here** link on the login page.

---

## 📁 What Was Created

```
y:\new\
├── server.js              # Express + MongoDB backend server
├── package.json           # Node.js dependencies
├── .env                   # MongoDB connection config (EDIT THIS!)
├── .env.example           # Example environment file
├── API_DOCUMENTATION.md   # Complete API docs
├── SETUP_INSTRUCTIONS.md  # Detailed setup guide
├── app.js                 # Original frontend (localStorage)
├── index.html             # Frontend HTML
└── styles.css             # Frontend CSS
```

---

## 🔧 Features

✅ **MongoDB Atlas Integration** - Cloud database storage  
✅ **User Authentication** - JWT-based login system  
✅ **RESTful API** - Complete CRUD operations  
✅ **Password Hashing** - Secure bcrypt encryption  
✅ **Activity Logging** - Track all user actions  
✅ **Sample Data** - Pre-loaded demo products & users  
✅ **Persistent Storage** - Data survives server restart  

---

## 📊 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login and get JWT token

### Products
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Add new product
- `PUT /api/products/:id` - Update product
- `DELETE /api/products/:id` - Delete product

### Sales
- `GET /api/sales` - Get all sales
- `POST /api/sales` - Record new sale

### Activities
- `GET /api/activities` - Get user activities

### Users
- `GET /api/users` - Get all users (admin only)
- `GET /api/users/me` - Get current user profile

See `API_DOCUMENTATION.md` for full details.

---

## 🔐 Credentials & Secrets

- This repository does **not** include personal API keys or personal credentials.
- Keep your real values only in `.env` (never commit `.env`).
- Share `.env.example` as the template for other users.

---

## 💡 Next Steps

The frontend still uses localStorage. To connect it to MongoDB:

1. Update `app.js` to use `fetch()` API calls
2. Replace `localStorage.getItem()` with `fetch('/api/products')`
3. Add JWT token to all requests
4. Handle async operations with `async/await`

Or I can create the updated frontend for you!

---

## 🛠️ Tech Stack

- **Backend:** Node.js + Express.js
- **Database:** MongoDB Atlas (Cloud)
- **Authentication:** JWT + bcrypt
- **Frontend:** HTML/CSS/JavaScript + Bootstrap
- **Charts:** Chart.js

---

## 📝 Environment Variables

Create/edit `.env` file:

```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_long_random_secret
PORT=3000
DISABLE_MONGODB=false

# Optional: customize initial seeded users
SEED_ADMIN_USERNAME=admin
SEED_ADMIN_PASSWORD=ChangeMeAdmin123!
SEED_ADMIN_NAME=Admin User
SEED_ADMIN_EMAIL=admin@example.com
```

Recommended:
- Use a long random value for `JWT_SECRET` (32+ chars).
- Use your own MongoDB Atlas user/password in `MONGODB_URI`.
- Set `DISABLE_MONGODB=true` if you want to temporarily run without any MongoDB connection.

---

## 🐛 Troubleshooting

**Can't connect to MongoDB?**
- Check your `.env` file
- Verify IP whitelist in MongoDB Atlas
- Ensure username/password are correct

**Port already in use?**
- Change PORT in `.env` to 3001 or 3002
- Or stop other applications using port 3000

**Module not found?**
- Run `npm install` again

---

## 📚 Documentation

- `SETUP_INSTRUCTIONS.md` - Complete setup guide
- `API_DOCUMENTATION.md` - API reference
- `README.md` - This file

---

**Ready to go! Just configure MongoDB Atlas and run `npm start`** 🚀
