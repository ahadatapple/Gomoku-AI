# Gomoku AI

A competitive Gomoku (five in a row) bot in Python, built for the Rice Emerging Scholars Program (RESP) Coding Track, summer 2026. Selected as one of 38 first-year projects presented at Rice's STEM Symposium.

## How it works
- Custom heuristic board evaluator: scans every row, column, and diagonal for attack and defense patterns (live and blocked sequences of 2-4 stones) and scores the position
- Plays through a minimax game tree using the RESP course's Strategy engine
- Tuned iteratively with a tournament harness that benchmarks each strategy change over 20-game matchups

## Results (empty-board start)
- Initial version (n = 10): 100% vs easy/medium bots, 70% vs hard, 30-100% vs peer bots
- After finding and removing a directional bias in the attack/defense scoring (n = 20): 90-100% vs easy/medium, 80% vs hard, 100% vs both peer bots

## What's mine
The game engine, tournament harness, and notebook scaffolding are the RESP course framework (Bryce Kille / Rice, Apache 2.0). My work is the heuristic evaluator and the tuning process documented above.

## Setup
pip install numpy termcolor tqdm prettytable ipywidgets
Open heuristic-tester-final.ipynb in Jupyter and run the cells to test the heuristic or run a tournament.