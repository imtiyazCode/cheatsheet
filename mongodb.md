# 🍃 MongoDB Cheatsheet for Beginners

> Learn the most useful MongoDB commands to manage databases, collections, and documents easily.

---

## 📌 What is MongoDB?

MongoDB is a **NoSQL database**. It stores data in **collections** (like tables), and data is in **documents** (like JSON).

---

## ▶️ Starting MongoDB (Locally)

### If using MongoDB installed on your computer:
```bash
mongod       # Start MongoDB server
mongo        # Open MongoDB shell
```

---

## 🧱 Databases

### 📄 Show all databases
```bash
show dbs
```

### ➕ Create or switch to a database
```bash
use myDatabase
```

### ❌ Delete a database
```bash
db.dropDatabase()
```

---

## 📁 Collections

A collection is like a table (holds documents).

### 📄 Show all collections
```bash
show collections
```

### ➕ Create a collection
```bash
db.createCollection("users")
```

### ❌ Delete a collection
```bash
db.users.drop()
```

---

## 📦 Documents

Documents are like rows in SQL — stored as JSON-like objects.

### ➕ Insert data
```bash
db.users.insertOne({ name: "Imtiyaz", age: 23 })
db.users.insertMany([{ name: "Ali" }, { name: "Sara" }])
```

### 🔍 Find data
```bash
db.users.find()                  # Show all
db.users.find({ name: "Ali" })   # Filter by field
db.users.findOne({ age: 23 })    # Return one document
```

### ✏️ Update data
```bash
db.users.updateOne(
  { name: "Ali" },
  { $set: { age: 25 } }
)

db.users.updateMany(
  { age: { $lt: 18 } },
  { $set: { status: "minor" } }
)
```

### ❌ Delete data
```bash
db.users.deleteOne({ name: "Sara" })
db.users.deleteMany({ age: { $gt: 50 } })
```

---

## 🔍 Query Operators

| Operator     | Description             |
|--------------|-------------------------|
| `$gt`        | Greater than            |
| `$lt`        | Less than               |
| `$gte`       | Greater than or equal   |
| `$lte`       | Less than or equal      |
| `$ne`        | Not equal               |
| `$in`        | Match values in array   |

```bash
db.users.find({ age: { $gt: 18 } })
```

---

## 🔄 Aggregation (Basic)

Aggregation is used to process data (like SQL GROUP BY).

### 🧮 Group by Field
```bash
db.users.aggregate([
  { $group: { _id: "$age", total: { $sum: 1 } } }
])
```

### 🔍 Filter with `$match`
```bash
db.users.aggregate([
  { $match: { age: { $gte: 18 } } }
])
```

### 📊 Sort with `$sort`
```bash
db.users.aggregate([
  { $sort: { age: -1 } }   # -1 for descending, 1 for ascending
])
```

---

## 🔐 User Management (Optional)

```bash
use admin

db.createUser({
  user: "admin",
  pwd: "mypassword",
  roles: ["userAdminAnyDatabase", "readWriteAnyDatabase"]
})
```

---

## 🧹 Clean Up

```bash
db.users.remove({})            # Remove all documents
db.dropDatabase()              # Drop current DB
db.users.drop()                # Drop specific collection
```

---

## 🧪 Useful Shell Commands

```bash
show dbs                         # List all databases
show collections                 # List all collections
db.collection.find().pretty()   # Nicely format output
```

---

## 🌍 MongoDB with Node.js (Mongoose)

Install:
```bash
npm install mongoose
```

Basic usage:
```js
const mongoose = require("mongoose");

mongoose.connect("mongodb://localhost/myDB", {
  useNewUrlParser: true,
  useUnifiedTopology: true,
});

// Define schema
const userSchema = new mongoose.Schema({
  name: { type: String, required: true },
  age: { type: Number, required: false },
  email: { type: String, required: true, unique: true }
});

// Create model
const User = mongoose.model("User", userSchema);

// Create and save user
const user = new User({ name: "Imtiyaz", email: "imtiyaz@example.com" });
user.save();
```

---

## 📚 Resources

- 📘 [MongoDB Docs](https://www.mongodb.com/docs/)
- 💡 [MongoDB University (Free Courses)](https://university.mongodb.com/)
- 🪰 [Mongoose Docs (Node.js)](https://mongoosejs.com/docs/)

---

> ✅ **Pro Tip**: Think of MongoDB as flexible — you don't need to define structure upfront like SQL. Start inserting and querying right away!
