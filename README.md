# hackathon-judging-system

To run this project you need the following CSVs:

1. `judges.csv` with the following columns:
    - `judgeFirstName`
    - `judgeLastName`

2. `teams.csv` with the following columns:
    - `teamName`
    - `tableNumber`


Change the variable `x` in `judge_assignments.ipynb` to the number of judges each team will receive.

Run all cells in `judge_assignments.ipynb` to generate judge assignments. The output will be a CSV file with the teams each judge will be judging. Note that our algorithm does not ensure that two judges will not be judging the same team at the same slot.

During judging, the judges will be given a Google Form to fill out. You'll need to ask them specific questions to generate a `points.csv` file containing the following columns:
- `tableNumber`
- `judgeNumber`
- `points`

Run all cells in `calculate_scores.ipynb` to generate a sorted ranking of the teams based on the judges' scores. The output will be a CSV file with the following columns:
- `tableNumber`
- `standardizedPoints`
- `judgeCount`
- `teamName`

The top teams will be the ones with the highest `standardizedPoints`.

