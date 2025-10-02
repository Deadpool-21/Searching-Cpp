

# Searching in C++

## 🎯 Aim

To study, understand, and implement various **searching algorithms** in C++, analyze their working principles, compare their efficiency, and determine the most suitable algorithm for different scenarios.

---

## 💻 Software Used

* **Visual Studio Code (VS Code)**

---

## 📌 Objectives

* Implement searching algorithms in C++.
* Understand **linear** and **binary search** techniques.
* Analyze **time complexity** and **space complexity**.
* Compare the efficiency of different searching algorithms.
* Conclude which algorithm is best under specific conditions.

---

## 📖 Theory

Searching algorithms are techniques used to **locate a particular element** in a dataset (arrays, linked lists, or databases).

They are broadly categorized as:

### 1. Linear Search (Sequential Search)

* Examines each element one by one.
* Simple to implement but inefficient for large datasets.
* **Time Complexity:** O(n)
* **Space Complexity:** O(1)

### 2. Binary Search

* Applicable only on **sorted arrays**.
* Repeatedly divides the search interval in half.
* More efficient than linear search.
* **Time Complexity:** O(log n)
* **Space Complexity:** O(1) (iterative), O(log n) (recursive)

### 3. Interpolation Search

* Predicts the likely position of the element using a formula based on the key.
* Works best on **uniformly distributed sorted data**.
* **Time Complexity:** O(log log n) (best), O(n) (worst)
* **Space Complexity:** O(1)

### 4. Exponential Search

* Designed for **unbounded or infinite lists**.
* Steps:

  1. Find range by repeated doubling.
  2. Apply binary search within range.
* **Time Complexity:** O(log n)
* **Space Complexity:** O(1)

### 5. Jump Search

* Jumps ahead by fixed steps to find the block containing the target element.
* Performs **linear search** within that block.
* Optimal step size = √n.
* **Time Complexity:** O(√n)
* **Space Complexity:** O(1)

---

## 📊 Comparison Table

| Algorithm              | Best Case | Worst Case | Space Complexity | Data Requirement |
| ---------------------- | --------- | ---------- | ---------------- | ---------------- |
| **Linear Search**      | O(1)      | O(n)       | O(1)             | Sorted/Unsorted  |
| **Binary Search**      | O(1)      | O(log n)   | O(1)             | Sorted           |
| **Interpolation**      | O(1)      | O(n)       | O(1)             | Sorted, Uniform  |
| **Jump Search**        | O(√n)     | O(√n)      | O(1)             | Sorted           |
| **Exponential Search** | O(log n)  | O(log n)   | O(1)             | Sorted           |

---

## ⚙️ Algorithm Outlines

### 🔹 Binary Search Algorithm

**Precondition:** Array must be sorted.

1. Initialize: `low = 0`, `high = size - 1`.
2. While `low <= high`:

   * Find middle → `mid = (low + high)/2`.
   * If `arr[mid] == key` → return mid.
   * If `arr[mid] < key` → search right half (`low = mid + 1`).
   * Else → search left half (`high = mid - 1`).
3. If loop ends without match → return -1.

* **Time Complexity:** O(log n)
* **Space Complexity:** O(1)

---

### 🔹 Linear Search Algorithm

1. Start from first element.
2. For each `i < size`:

   * If `arr[i] == key` → return i.
   * Else increment `i`.
3. If not found → return -1.

* **Time Complexity:** O(n)
* **Space Complexity:** O(1)

---

### 🔹 Sequential Search Algorithm

(Similar to Linear Search, often using a while loop).

1. Initialize `index = 0`.
2. While `index < size`:

   * If `arr[index] == key` → return index.
   * Else increment index.
3. If not found → return -1.

* **Time Complexity:** O(n)
* **Space Complexity:** O(1)

---

## ✅ Summary

* **Binary Search** is the fastest, but only works on **sorted arrays**.
* **Linear & Sequential Search** work on **unsorted arrays**, but are inefficient for large datasets.
* **Interpolation, Jump, and Exponential Search** are specialized algorithms, useful in particular conditions (uniform distribution, infinite lists, or optimization).

