# 🌳 T-Trees in Haskell

This readme is also available in [Español](README.es.md)

This project is an implementation of **T-Trees** (Trie-like trees) in **Haskell**, allowing for insertion, search, deletion, and key extraction using lists as compound keys. The tree is built to store keys as sequences and supports dictionary-like behavior through a typeclass.

---

## 🧠 Description

A `TTree` can be:

- A **Leaf**: a single key-value pair
- A **Node**: with a key, an optional value, and three subtrees:
  - Left: for keys less than the current
  - Middle: for continuation of compound keys
  - Right: for keys greater than the current
- Or **E**: an empty tree

The implementation supports:

- Searching for values by a list of keys (`search`)
- Inserting key-value pairs (`insert`)
- Deleting entries (`delete`)
- Retrieving all keys (`keys`)
- A **`Dic`** typeclass that abstracts these operations, treating `TTree` as a dictionary with `[k]` keys

---

## 🛠️ Technologies Used

- **Haskell**
- **GHC (Glasgow Haskell Compiler)**

---

## 📦 Project Structure

- `TTree k v`: Main data structure
- `search`: Looks up a value given a list of keys
- `insert`: Adds or updates a value at a path of keys
- `delete`: Removes a value from the tree
- `keys`: Returns all compound keys in the tree
- `Dic` typeclass: Provides a dictionary interface for `TTree`

---

## ✅ Project Status

- 🔧 Fully working core functionality  
- 📚 Well-structured for extension and testing  
- 🧪 Can be easily integrated into larger functional programs

---

## ▶️ How to Use

1. Make sure you have **GHC** installed.  
2. Save the code in a file, e.g., `TTree.hs`.
3. Load it in GHCi:
   ```bash
   ghci TTree.hs
   ```
