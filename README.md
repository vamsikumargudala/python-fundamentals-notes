# Python Zero Course

Personal study notes from a Python fundamentals course at BITS Pilani. Condensed, beginner-friendly notebooks covering Python basics to control flow.

---

## Folder Structure

```
├── My Notes/           # Study notes (12 notebooks)
│   ├── 01-06              # Basics: print, input, strings, variables, data types
│   └── 07-12              # Data structures & control flow
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

---

## Quick Start

```bash
# Clone and setup
git clone <repo-url>
cd Python_Zero_Course

# Create virtual environment (using UV)
uv venv
source .venv/Scripts/activate  # Git Bash on Windows
# or: .venv\Scripts\activate   # CMD/PowerShell

# Install dependencies
uv sync
```

Open any `.ipynb` file in VS Code and select the `.venv` kernel.

---

## Tools Used

- **UV** - Fast Python package manager
- **Jupyter** - Interactive notebooks
- **VS Code** - Editor with Jupyter extension

For detailed setup instructions, see [PROJECT_SETUP_GUIDE.md](PROJECT_SETUP_GUIDE.md).

---

## Acknowledgment

These notes are based on lectures from BITS Pilani's Python course.

Original course materials: [BITS Pilani Taxila](https://taxila-aws.bits-pilani.ac.in/course/view.php?id=16745) (requires BITS login)
