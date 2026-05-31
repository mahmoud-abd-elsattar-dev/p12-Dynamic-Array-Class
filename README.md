# 🗃️ clsDynamicArray — Dynamic Array Library

A generic C++ dynamic array implementation using templates, supporting resizable storage with full insertion, deletion, search, and traversal operations.

---

## 📖 Overview

`clsDynamicArray` is a reusable template-based C++ class that implements a dynamic array from scratch using raw pointers and heap memory. Unlike `std::vector`, this class manually manages memory allocation and resizing, making it a great learning example for how dynamic arrays work under the hood.

---

## ✨ Features

- **Dynamic Resizing**: Resize the array to any size while preserving existing data
- **Insert Anywhere**: Insert at a specific index, beginning, end, before, or after a position
- **Delete Anywhere**: Delete by index, by value, first item, or last item
- **Search**: Find an item's index by value
- **Reverse**: Reverse the array in-place
- **Utility Methods**: Size, IsEmpty, Clear, GetItem, SetItem, PrintList
- **Generic Type Support**: Works with any data type via C++ templates
- **Destructor**: Automatically frees heap memory when the object goes out of scope

---

## 🚀 How to Use

Include the header file in your project:

```cpp
#include "clsDynamicArray.h"
```

### Basic Usage
```cpp
clsDynamicArray<int> arr(3);

arr.SetItem(0, 10);
arr.SetItem(1, 20);
arr.SetItem(2, 30);

arr.PtintList();      // 10 20 30
cout << arr.Size();   // 3
cout << arr.Find(20); // 1

arr.Reverse();
arr.PtintList();      // 30 20 10
```

### Insertion & Deletion
```cpp
arr.InsertAtBeginning(5);   // 5 30 20 10
arr.InsertAtEnd(99);        // 5 30 20 10 99
arr.InsertAt(2, 77);        // 5 30 77 20 10 99
arr.InsertAfter(1, 50);     // 5 30 50 77 20 10 99
arr.InsertBefore(3, 11);    // 5 30 50 11 77 20 10 99

arr.DeleteItemAt(0);        // removes index 0
arr.DeleteItem(99);         // removes by value
arr.DeleteFirstItem();
arr.DeleteLastItem();
```

### Resize & Clear
```cpp
arr.Resize(5);   // keeps first 5 items
arr.Clear();     // empties the array
```

---

## 🧠 Concepts Used

- **Templates** — Generic class supporting any data type via `template <class T>`
- **OOP** — Encapsulation of array data and behavior inside a class
- **Dynamic Memory** — Manual `new` and `delete[]` for heap-allocated arrays
- **Destructor** — `~clsDynamicArray()` ensures no memory leaks on object destruction
- **Pointer Arithmetic** — Direct manipulation of raw `T*` arrays
- **Resizing Strategy** — Allocates a new array, copies data, then frees the old one
- **Index Validation** — Bounds checking before any get, set, or delete operation
- **Inheritance-Ready** — `protected` members allow extending the class

---

## 🔑 Key Methods

| Method | Description |
|---|---|
| `SetItem()` | Sets the value at a given index |
| `GetItem()` | Returns the value at a given index |
| `Size()` | Returns the current size of the array |
| `IsEmpty()` | Returns true if the array has no items |
| `Resize()` | Resizes the array, preserving existing data |
| `InsertAt()` | Inserts a value at a specific index |
| `InsertAtBeginning()` | Inserts a value at index 0 |
| `InsertAtEnd()` | Inserts a value at the last position |
| `InsertBefore()` | Inserts a value before a given index |
| `InsertAfter()` | Inserts a value after a given index |
| `DeleteItemAt()` | Deletes the item at a given index |
| `DeleteFirstItem()` | Deletes the first item |
| `DeleteLastItem()` | Deletes the last item |
| `DeleteItem()` | Finds and deletes an item by value |
| `Find()` | Returns the index of a value, or -1 if not found |
| `Reverse()` | Reverses the array in-place |
| `Clear()` | Removes all items and resets the size to 0 |
| `PtintList()` | Prints all array items |

---

## 📄 License

This project is open source and free to use for educational purposes.

---

## 👤 Author

👤 **Mahmoud Abd El-Sattar**  
📧 mahmoud.abdelsattar.dev@gmail.com  
💼 [linkedin.com/in/mahmoud-abd-el-sattar](https://www.linkedin.com/in/mahmoud-abd-el-sattar-1b227522a)
