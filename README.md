# AI Engineer Take-Home Assignment: Support Ticket Classification

This project is a solution to an AI engineering take-home assignment. It uses Google's **Gemini** LLM to analyze software support tickets and automatically identify issue types, priority levels, and system components using both static and dynamic category taxonomies.

---

## Project Overview

The project is structured in three parts to reflect increasing complexity:

### Part 1: Static Single-Label Classification
- Identifies the most likely **Issue Type** and **Priority**.
- Uses hardcoded category lists.
- Outputs a simple JSON object.

### Part 2: Multi-Aspect Classification
- Extracts **multiple issue aspects** from the ticket.
- Includes Issue Type, Priority (with subcategories), and Component.
- Uses a fixed prompt structure with known categories.
- Outputs a list of lists (e.g. `["Priority", "High", "Performance"]`).

### Part 3: Dynamic Category Loading
- Parses `categories.json` at runtime.
- Automatically handles **nested categories** of arbitrary depth.
- Prompts Gemini with dynamically formatted category trees.
- Fallbacks to "Other" if no match is found.

---

## File Structure

```bash
AI-Assignment/
├── issue.txt                   # Sample support ticket input
├── categories.json             # Dynamic nested category definitions
├── Assignment.ipynb            # Contains the 3 parts of the assignment
└── README.md                   # Project documentation


---

## Setup Instructions:

Follow these steps to set up and run the project locally using the provided `.ipynb` notebook.

### 1. Clone the Repository:

```bash
git clone https://github.com/AyaJouni/AI-Assignment.git
cd AI-Assignment

### 2. Install Dependencies:

```bash
pip install -r requirements.txt

### 3. Open the Notebook:

```bash
jupyter notebook



