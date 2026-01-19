#!/usr/bin/env python3
"""
sudoku_solver.py

Automatic Sudoku solver using backtracking with MRV heuristic (choose the empty cell
with the fewest candidates).

Usage:
- Run with no arguments to see a demo:
    python sudoku_solver.py

- Provide a puzzle string of 81 characters (digits 1-9, and 0 or . for empties):
    python sudoku_solver.py --puzzle "530070000600195000098000060800060003400803001700020006060000280000419005000080079"

- Or provide a file containing 9 lines (each line 9 characters, digits or . / 0):
    python sudoku_solver.py --file puzzle.txt

Options:
    --all    Find and print all possible solutions (may be slow for ambiguous puzzles)

The solver prints the solved grid in a readable format.
"""

import sys
import argparse
from typing import List, Tuple, Optional, Set

Grid = List[List[int]]

def parse_puzzle_string(s: str) -> Grid:
    """Parse a linear puzzle string (length 81) into 9x9 grid."""
    filtered = [ch for ch in s if ch.isdigit() or ch in ".0"]
    if len(filtered) != 81:
        raise ValueError("Puzzle string must contain 81 digits or '.'/'0' placeholders.")
    grid = []
    for i in range(9):
        row = []
        for j in range(9):
            ch = filtered[i*9 +
