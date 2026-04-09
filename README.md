<div align="center">

# 🔢 NumPy Mastery

### *From Zero to Hero — A Complete NumPy Crash Course in Jupyter*

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.24%2B-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Anaconda](https://img.shields.io/badge/Anaconda-Environment-44A833?style=for-the-badge&logo=anaconda&logoColor=white)](https://www.anaconda.com/)
[![License](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge)](LICENSE)
[![Stars](https://img.shields.io/github/stars/yourusername/numpy?style=for-the-badge&color=FBBF24&logo=github)](https://github.com/yourusername/numpy/stargazers)

<br/>

> 🚀 **A hands-on, beginner-friendly Jupyter Notebook series** covering NumPy fundamentals — from array creation to broadcasting, vectorization, and beyond. Built with real benchmarks and clean, commented code.

<br/>

[📖 View Notebook](#-notebook-overview) · [⚡ Quick Start](#-quick-start) · [📚 Topics Covered](#-topics-covered) · [📊 Benchmarks](#-performance-benchmarks)

</div>

---

## 📌 About This Repository

**`numpy`** is a structured, beginner-to-intermediate learning repository focused entirely on the **NumPy** library — the backbone of scientific computing in Python. Each concept is demonstrated with clean code, inline comments, and real execution outputs inside Jupyter Notebooks.

Whether you're just getting started with data science or brushing up on array operations, this repo has you covered.

---

## ✨ Highlights

| Feature | Detail |
|---|---|
| 📓 Format | Jupyter Notebook (`.ipynb`) |
| 🐍 Language | Python 3.8+ |
| 📦 Environment | Anaconda / pip |
| 🧪 Tested | ✅ All cells executed & verified |
| 💬 Comments | Inline explanations throughout |
| 📊 Benchmarks | Real time & memory comparisons |

---

## 📚 Topics Covered

<details>
<summary><b>🟦 1. NumPy vs Python Lists — Performance Showdown</b></summary>
<br/>

```python
# Python List: ~2.12 seconds for 10M elements
sq_list = [i**2 for i in py_list]

# NumPy Array: ~0.038 seconds — 55x faster! ⚡
sq_arr = np_arr**2
```

- Speed benchmark with `time` module on 10,000,000 elements
- Memory comparison using `sys.getsizeof` vs `.nbytes`

</details>

<details>
<summary><b>🟦 2. Array Creation</b></summary>
<br/>

```python
np.array([1, 2, 3])          # From list
np.zeros((4, 5), dtype='int64')  # All zeros
np.ones((4,), dtype='int64')     # All ones
np.full((4, 3), 29)          # Constant fill
np.eye(5)                    # Identity matrix
np.arange(1, 11, 2)          # Range-based
np.linspace(1, 100, 5)       # Evenly spaced
```

</details>

<details>
<summary><b>🟦 3. Array Properties</b></summary>
<br/>

```python
arr.shape    # Dimensions
arr.size     # Total elements
arr.dtype    # Data type
arr.ndim     # Number of dimensions
```

</details>

<details>
<summary><b>🟦 4. Type Casting</b></summary>
<br/>

```python
float_arr = arr.astype(np.float64)
```

</details>

<details>
<summary><b>🟦 5. Reshaping & Flattening</b></summary>
<br/>

```python
arr.reshape(4, 2)   # Change shape
arr.flatten()       # 2D → 1D
```

</details>

<details>
<summary><b>🟦 6. Indexing — 1D, 2D, Fancy & Boolean</b></summary>
<br/>

```python
arr[2]              # 1D indexing
arr[1][2]           # 2D indexing
arr[[0, 2, 3]]      # Fancy indexing
arr[arr > 5]        # Boolean indexing
arr[arr % 2 == 0]   # Filter evens
```

</details>

<details>
<summary><b>🟦 7. Slicing — 1D, 2D, 3D + Copy vs View</b></summary>
<br/>

```python
arr[2:8]            # Basic slice
arr[::3]            # Step slicing
arr2D[0:2, 1:2]     # 2D slice
arr3D[:, 0, :]      # 3D slice
```

> ⚠️ **Important:** NumPy slicing returns a **view**, not a copy — modifying the slice modifies the original array!

</details>

<details>
<summary><b>🟦 8. Multi-Dimensional Arrays (2D & 3D)</b></summary>
<br/>

```python
np.sum(arr2D, axis=0)   # Column-wise sum
np.sum(arr2D, axis=1)   # Row-wise sum
arr3D[1, 1, 1]           # 3D indexing
```

</details>

<details>
<summary><b>🟦 9. Vectorization & Broadcasting</b></summary>
<br/>

```python
arr ** 2            # Vectorized squaring
arr + 10            # Scalar broadcasting
arr + arr1          # Array broadcasting (2D)
```

</details>

<details>
<summary><b>🟦 10. Normalization</b></summary>
<br/>

```python
mean = np.mean(arr)
std  = np.std(arr)
normalized = (arr - mean) / std
```

</details>

<details>
<summary><b>🟦 11. NumPy Built-in Functions</b></summary>
<br/>

| Category | Functions |
|---|---|
| Aggregation | `sum`, `prod`, `max`, `min`, `argmin`, `argmax` |
| Power / Root | `square`, `sqrt` |
| Logarithm | `log`, `log2`, `log10`, `exp` |
| Rounding | `round`, `ceil`, `floor`, `trunc` |
| Utility | `unique`, `sort`, `abs` |
| Complex | Supports `complex128` dtype |

</details>

---

## 📊 Performance Benchmarks

> Tested on 10,000,000 elements

```
┌────────────────────────────┬───────────────────┬──────────────────────┐
│ Operation                  │ Python List       │ NumPy Array          │
├────────────────────────────┼───────────────────┼──────────────────────┤
│ Square (i**2)              │ ~2.12 seconds     │ ~0.038 seconds ⚡    │
│ Memory Usage               │ ~800 GB (logical) │ ~80 MB               │
│ Speed Improvement          │ —                 │ ~55x faster 🚀       │
└────────────────────────────┴───────────────────┴──────────────────────┘
```

---

## ⚡ Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/saifullah857/numpy-mastery.git
cd numpy
```

### 2. Set Up Environment

**Using Anaconda (recommended):**
```bash
conda create -n numpy-env python=3.10
conda activate numpy-env
conda install numpy jupyter
```

**Using pip:**
```bash
pip install numpy jupyter
```

### 3. Launch the Notebook

```bash
jupyter notebook numpy.ipynb
```

---

## 📁 Project Structure

```
numpy/
│
├── 📓 numpy.ipynb          # Main notebook — all concepts & code
├── 📁 .ipynb_checkpoints/  # Auto-saved Jupyter checkpoints
├── 📁 .virtual_documents/  # VS Code Jupyter virtual docs
├── 📁 anaconda_projects/   # Anaconda project config
└── 📄 README.md            # You are here!
```

---

## 🛠️ Requirements

```txt
python >= 3.8
numpy  >= 1.24
jupyter >= 1.0
```

Install all at once:
```bash
pip install numpy jupyter
```

---

## 🤝 Contributing

Contributions are welcome! If you'd like to add more examples, fix a bug, or improve documentation:

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/add-advanced-indexing`
3. Commit your changes: `git commit -m 'Add advanced indexing examples'`
4. Push to the branch: `git push origin feature/add-advanced-indexing`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with ❤️ and lots of `np.array([ ])` calls

[![GitHub followers](https://img.shields.io/github/followers/saifullah857?style=social)](https://github.com/saifullah857)


**⭐ Star this repo if it helped you learn NumPy!**

</div>