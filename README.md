🚀 GA-TSP
Hybrid Metaheuristics for the Traveling Salesman Problem (TSP)

This project solves the Traveling Salesman Problem (TSP) using a hybrid metaheuristic approach combining:

🧬 Genetic Algorithm (GA)

🔄 Tabu Search

⚙️ Google OR-Tools (benchmark solver)

The goal is to compare metaheuristics and evaluate how hybridization improves solution quality and computational performance.

📊 Input Dataset

The repository includes a precomputed distance matrix in Excel format.

Rows = city names

Columns = city names

Each cell = distance between two cities

Matrix must be square (n × n)

Distances must be numeric

✔ No coordinate computation needed — distances are already provided.

✨ Features

✔ Load a distance matrix directly from Excel

✔ Solve TSP using GA, Tabu Search, and Hybrid GA+Tabu

✔ Benchmark against Google OR-Tools

✔ Extract the best route and total distance

✔ Measure execution times for all algorithms

🧠 Methodology
🔹 1. Genetic Algorithm (GA)

Global search using:

Selection (roulette or tournament)

Order Crossover (OX)

Mutation (swap / inversion)

Elitism

🔹 2. Tabu Search

Local improvement using:

Neighborhood moves (swap / 2-opt)

Tabu list memory

Aspiration criteria to escape local minima

Stop by iteration limit or stagnation

🔹 3. Hybrid GA + Tabu

Each GA generation:

Select the current best route

Improve it using Tabu Search

Reinsert the improved individual into the population

This provides:
GA = exploration
Tabu = exploitation

🔧 How to Run
1️⃣ Install dependencies
pip install numpy pandas openpyxl ortools

2️⃣ Run the program
python main.py


Or open the notebook in Jupyter / Google Colab and execute all cells.

📈 Outputs

The solver reports:

🧬 Best GA distance

🔄 Best Tabu Search distance

🧬➕🔄 Best Hybrid distance

⚙️ OR-Tools benchmark solution

⏱ Execution time for each algorithm

📍 Final optimized tour (sequence of cities)

🎯 Purpose

This project is ideal for:

Metaheuristics research

TSP and routing problem experimentation

Operations Research and Optimization courses

Benchmarking heuristic vs. exact solvers

It demonstrates how hybrid metaheuristics improve convergence and solution robustness.

📜 License

This project is released under the MIT License.
You are free to use, modify, and distribute it for research or academic purposes.
