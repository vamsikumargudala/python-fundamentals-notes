# Python Zero Course

Python fundamentals course from BITS Pilani. Contains original lecture notebooks and condensed personal notes.

---

## Folder Structure

```
├── Sessions/           # Original lecture notebooks from professor
│   ├── Session 1 Notes/    # Basics: print, input, strings, variables
│   ├── Session 2 Notes/    # Data structures & control flow
│   ├── Session 3 Notes/    # Files & functions
│   └── Session 4 Notes/    # NumPy, Pandas, Visualization, ML
│
├── My Notes/           # Condensed personal study notes
│   ├── 01-06              # Session 1: Python basics
│   ├── 07-12              # Session 2: Data structures & control flow
│   ├── 13-20              # Session 3: Files & functions
│   └── 21-30              # Session 4: NumPy, Pandas, Visualization
```

---

## My Notes - Quick Navigation

### Session 1: Python Basics

| # | Topic | Description |
|---|-------|-------------|
| 01 | [Print Function](My%20Notes/01_print_function.ipynb) | `print()`, sep, end, escape characters |
| 02 | [Input Function](My%20Notes/02_input_function.ipynb) | `input()`, type conversion |
| 03 | [Strings](My%20Notes/03_strings.ipynb) | Creation, indexing, slicing |
| 04 | [String Methods](My%20Notes/04_string_methods.ipynb) | Case, strip, find, replace, split/join |
| 05 | [Variables & Expressions](My%20Notes/05_variables_expressions.ipynb) | Variables, operators, precedence |
| 06 | [Data Types](My%20Notes/06_data_types.ipynb) | int, float, str, bool, type casting |

### Session 2: Data Structures & Control Flow

| # | Topic | Description |
|---|-------|-------------|
| 07 | [Lists](My%20Notes/07_lists.ipynb) | Creation, methods, list comprehensions |
| 08 | [Tuples](My%20Notes/08_tuples.ipynb) | Immutability, unpacking |
| 09 | [Sets](My%20Notes/09_sets.ipynb) | Uniqueness, set operations |
| 10 | [Dictionaries](My%20Notes/10_dictionaries.ipynb) | Key-value pairs, methods |
| 11 | [Conditionals](My%20Notes/11_conditionals.ipynb) | if/elif/else, try/except |
| 12 | [Loops](My%20Notes/12_loops.ipynb) | for, while, range, break/continue |

### Session 3: Files & Functions

| # | Topic | Description |
|---|-------|-------------|
| 13 | [File Reading](My%20Notes/13_file_reading.ipynb) | open(), read modes, with statement |
| 14 | [File Writing](My%20Notes/14_file_writing.ipynb) | write(), append, writelines() |
| 15 | [File Operations](My%20Notes/15_file_operations.ipynb) | Search, parse, process file data |
| 16 | [Functions](My%20Notes/16_functions.ipynb) | def, return, function types |
| 17 | [Built-in Functions](My%20Notes/17_builtin_functions.ipynb) | len, max, min, sorted, type |
| 18 | [Custom Functions](My%20Notes/18_custom_functions.ipynb) | Real-world examples, algorithms |
| 19 | [Parameters & Arguments](My%20Notes/19_parameters_arguments.ipynb) | *args, defaults, mutable vs immutable |
| 20 | [Modules & Packages](My%20Notes/20_modules_packages.ipynb) | import, from, as, built-in modules |

### Session 4: NumPy, Pandas & Visualization

| # | Topic | Description |
|---|-------|-------------|
| 21 | [NumPy Basics](My%20Notes/21_numpy_basics.ipynb) | Arrays, creation, indexing, slicing |
| 22 | [NumPy Computation](My%20Notes/22_numpy_computation.ipynb) | UFuncs, broadcasting, vectorization |
| 23 | [NumPy Aggregations](My%20Notes/23_numpy_aggregations.ipynb) | sum, mean, min, max, axis operations |
| 24 | [Pandas Series & DataFrame](My%20Notes/24_pandas_series_dataframe.ipynb) | Series, DataFrame, indexing with loc/iloc |
| 25 | [Pandas Operations](My%20Notes/25_pandas_operations.ipynb) | concat, merge, join |
| 26 | [Pandas File I/O](My%20Notes/26_pandas_file_io.ipynb) | read_csv, to_csv, Excel, JSON |
| 27 | [Pandas Exploration](My%20Notes/27_pandas_exploration.ipynb) | describe, groupby, missing values |
| 28 | [Matplotlib Basics](My%20Notes/28_matplotlib_basics.ipynb) | Plots, subplots, styling, saving |
| 29 | [Seaborn Visualizations](My%20Notes/29_seaborn_visualizations.ipynb) | Statistical plots, heatmaps, pairplots |
| 30 | [Linear Regression](My%20Notes/30_linear_regression.ipynb) | sklearn, train/test, evaluation metrics |

---

## Prerequisites

- **Python 3.10+** - [Download](https://www.python.org/downloads/)
- **UV** - [Install](https://docs.astral.sh/uv/getting-started/installation/)
- **VS Code** with Jupyter extension

---

## Quick Start

```bash
git clone https://github.com/vamsikumargudala/python-fundamentals-bits.git
cd python-fundamentals-bits
uv sync
```

Open any `.ipynb` file in VS Code and select the `.venv` kernel.

---

## Acknowledgment

These notes are based on lectures from BITS Pilani's Python course.

Original course materials: [BITS Pilani Taxila](https://taxila-aws.bits-pilani.ac.in/course/view.php?id=16745) (requires BITS login)
