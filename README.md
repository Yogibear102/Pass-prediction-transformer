 
# ⚽ Premier League Pass Prediction

A machine learning project to analyze and predict passing patterns in Premier League football using transformer models. This system models each possession as a linked list of passes and predicts the next pass based on spatial and player data.

---

## 🧠 Overview

This project:
- Maps the pitch into a 2D grid
- Tracks passes as a doubly linked list
- Calculates spatial overloads (your players vs opposition in a zone)
- Converts possession data into sequences for machine learning
- Uses a Transformer to predict the next pass (receiver, grid, and completion)

---

## 🏗️ Data Structure

Each pass is stored as a `PassNode`:

```python
class PassNode:
    def __init__(self, passer, receiver, completed, start_grid, end_grid):
        self.passer = passer
        self.receiver = receiver
        self.completed = completed
        self.start_grid = start_grid
        self.end_grid = end_grid
        self.next = None
        self.prev = None

