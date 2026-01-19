# pt-task1

Collection of 5 Python tasks for the pt-task1 assignment.

## Overview

This repository contains five Python tasks (task01 — task05). Each task is implemented as a standalone script in the repository root. The README documents how to run each task, expected inputs/outputs (placeholders), and how to test them. If a script requires command-line arguments, input files, or interactive input, the specific usage is shown in each task section below.

## Repository structure

- task01 — Python script for Task 1
- task02 — Python script for Task 2
- task03 — Python script for Task 3
- task04 — Python script for Task 4
- task05 — Python script for Task 5
- README.md — this file

> Note: The task files are Python scripts. They may or may not have the `.py` extension; run them with `python` or `python3` (examples below).

## Requirements

- Python 3.8+ recommended
- (Optional) virtual environment:
  - python -m venv .venv
  - source .venv/bin/activate  # Linux/macOS
  - .venv\Scripts\activate     # Windows
- If the repo includes dependencies, install them via:
  - pip install -r requirements.txt

## Running the tasks

General patterns:

- Run a script directly with Python:
  - python task01
  - python task02
- If scripts accept arguments:
  - python task01 arg1 arg2
- If scripts read from stdin, pipe input:
  - echo "input" | python task01

Below each task has a short template with placeholders. Replace placeholders with the exact behavior after reviewing the script.

---

### Task 1 (task01)

Description
- Short description: Placeholder — briefly state what the task does (e.g., "Compute the factorial of a number", "Filter lines that match a pattern", etc.)

Usage
- python task01 [args]
- Example (no args):
  - python task01
  - Expected output: <describe expected stdout>
- Example (with args):
  - python task01 42
  - Expected output: 1405006117752879898543142606244511569936384000000000

Notes
- If the script reads from stdin: echo "input" | python task01
- If the script writes to a file, mention the output file path

---

### Task 2 (task02)

Description
- Short description: Placeholder — what this script calculates or transforms.

Usage
- python task02 [args]
- Example:
  - python task02 input.txt
  - Expected output: <describe>

Notes
- List any edge cases the script handles or assumptions (e.g., expects integers, non-empty files)

---

### Task 3 (task03)

Description
- Short description: Placeholder — e.g., more complex logic, uses third-party libraries, etc.

Usage
- python task03 [args]
- Example:
  - python task03 --option value
  - Expected output: <describe>

Dependencies
- If this task requires extra packages, list them here (e.g., numpy, pandas).

---

### Task 4 (task04)

Description
- Short description: Placeholder

Usage
- python task04 [args]
- Example:
  - python task04 "some input"
  - Expected output: <describe>

Notes
- Mention if script has interactive prompts or requires environment variables.

---

### Task 5 (task05)

Description
- Short description: Placeholder

Usage
- python task05 [args]
- Example:
  - python task05 data.csv
  - Expected output: <describe>

Tests
- If there are tests, run them with:
  - python -m pytest
  - or
  - python -m unittest discover

## How to update this README with exact details

To provide precise usage, examples, and expected outputs I need the contents of each task script. You can:

- Allow the repository to be read (so I can fetch the scripts), or
- Paste each script into the chat, or
- Tell me key details for each task (what it does, arguments, input/output examples)

Once I have that, I will:
1. Replace the placeholder descriptions with exact summaries.
2. Add real usage examples and sample inputs/outputs.
3. Add any dependency installation steps required.

## Contributing

If you want to improve any task or add documentation:
- Fork the repo
- Create a branch with your changes
- Open a pull request with a clear description of changes

## License

Specify the project license here (e.g., MIT). If none is intended, add "All rights reserved."

## Contact

For questions and clarifications, open an issue or contact the repository owner.
