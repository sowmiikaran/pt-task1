# pt-task1

Collection of five small CLI programming tasks. This README documents each of the five task files in the repository, how to run them, required dependencies, and short examples.

Note: an automated language analysis reported "Python 100%". However Task 01 is implemented in Java. Each task file is listed below with the language detected from its contents.

---

## Repository files

- task01 — Java: temperature converter (public class `PRODIGY_SD_01`)
- task02 — Python: number guessing game
- task03 — Python: CLI contact manager (JSON persistence)
- task04 — Python: Sudoku solver (backtracking + MRV heuristic)
- task05 — Python: web scraper for books.toscrape.com (requests + BeautifulSoup)

---

## Prerequisites

- Java JDK 8+ (for Task 01)
- Python 3.7+ (recommended 3.8+) for Tasks 02–05
- Python packages (for Task 05): requests, beautifulsoup4
  - Install with:
    - pip install requests beautifulsoup4

General notes:
- Scripts include a shebang for Unix. You can run them directly if the file is executable, or run via `python3`.
- If a file is missing a .py or .java extension in your local copy, you can run it by passing the file to the appropriate interpreter or renaming it as explained per task.

---

## Task 01 — Temperature Converter (Java)

File: `task01` (source contains `public class PRODIGY_SD_01`)

Language: Java

What it does:
- Interactive program that reads a numeric temperature and an original unit (C, F, or K) and prints conversions to Celsius, Fahrenheit and Kelvin.

How to run:
1. Save or rename the file to `PRODIGY_SD_01.java` (the filename must match the public class).
2. Compile:
   - javac PRODIGY_SD_01.java
3. Run:
   - java PRODIGY_SD_01

Example session:
- Enter temperature value: 100
- Enter original unit (C for Celsius, F for Fahrenheit, K for Kelvin): F

Output:
- Converted Temperatures:
- Celsius: 37.78
- Fahrenheit: 100.00
- Kelvin: 310.93

Notes:
- The program validates numeric input and unit (C, F, K). Unknown unit prints a friendly error message.
- To use non-interactive mode, modify source to accept command-line args or redirect stdin.

---

## Task 02 — Number Guessing Game (Python)

File: `task02` (executable script with shebang)

Language: Python 3

What it does:
- Simple interactive game. Program chooses a random integer between 1 and 100 and prompts the user to guess until correct. It gives feedback ("Too low", "Too high") and reports number of attempts.

How to run:
- Make executable and run:
  - chmod +x task02
  - ./task02
- Or run with Python:
  - python3 task02

Notes:
- No external dependencies required (stdlib only).
- Safe to run locally; interactive stdin is required.

---

## Task 03 — Contact Manager (Python)

File: `task03` (executable script with shebang)

Language: Python 3

What it does:
- CLI contact manager with JSON persistence (stores data in `contacts.json` in the working directory).
- Features: add, list, view, edit, delete, search contacts.

How to run:
- Make executable and run:
  - chmod +x task03
  - ./task03
- Or:
  - python3 task03

Behavior details:
- Adds contacts with an auto-incrementing integer ID.
- `contacts.json` is created next to the script when changes are saved.
- Uses only the Python standard library (json, os, typing).

Notes:
- Back up `contacts.json` if you want to preserve entries before testing.
- The program is interactive and menu-driven.

---

## Task 04 — Sudoku Solver (Python)

File: `task04` (executable script with shebang)

Language: Python 3

What it does:
- Automatic Sudoku solver using backtracking with MRV (minimum remaining values) heuristic.
- Accepts puzzle input in several forms: 81-char puzzle string or a file with 9 lines of digits/`0`/`.` placeholders.

How to run:
- Basic demo:
  - python3 task04
- Provide puzzle string:
  - python3 task04 --puzzle "530070000600195000098000060800060003400803001700020006060000280000419005000080079"
- Provide file input:
  - python3 task04 --file puzzle.txt
- Find all solutions (may be slow for ambiguous puzzles):
  - python3 task04 --all --puzzle "<puzzle_string>"

Notes:
- Requires Python 3.7+.
- The solver prints the solved grid in a readable format.
- If your local copy of `task04` is truncated, fetch the full file from the repository before running.

---

## Task 05 — Books Scraper (Python)

File: `task05` (executable script with shebang)

Language: Python 3

What it does:
- Scrapes product (book) data from books.toscrape.com (title, price, rating, availability, product page URL) and writes results to a CSV.

Dependencies:
- requests
- beautifulsoup4

Install dependencies:
- pip install requests beautifulsoup4

How to run:
- Basic run (default start URL and output file):
  - python3 task05
- Provide start URL and output path:
  - python3 task05 --start-url "https://books.toscrape.com/catalogue/category/books_1/index.html" --output books.csv
- Limit pages or increase verbosity:
  - python3 task05 --max-pages 5 --verbose

Notes & responsible scraping:
- The script includes polite delays and retry logic; respect robots.txt and site terms of service.
- Use small `--max-pages` and sensible delays when testing.
- The CSV headers: title, price, rating, rating_text, product_page_url, availability.

---

## Common tips

- If a file has no extension in the repository, you can still run it using the appropriate interpreter (e.g., `python3 task03`) or rename it to add the correct extension for convenience (e.g., `task03.py`).
- To run scripts directly on Unix-like systems:
  - Ensure the first line (shebang) exists (most Python tasks include it).
  - Mark the file executable: chmod +x task03
  - Then run: ./task03
- For Java (Task 01) the file name must match the public class name exactly.

---

## Want me to update the README in the repo?

I can:
- Commit this README.md into the repository (create a branch and open a PR), or
- Provide a raw README.md file text for you to paste and commit.

Tell me which you prefer and, if you want a commit/PR, provide the branch name and PR title. If you want me to inspect each task file and add usage examples (or tests), say "inspect all" and I'll produce a more detailed per-file section with expected I/O and sample runs.

---

## License / Contribution

If you want a license added (MIT, Apache-2.0, GPL-3.0, etc.) or a CONTRIBUTING.md, tell me which license and I will prepare the file.
