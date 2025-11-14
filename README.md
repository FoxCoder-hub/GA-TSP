# GA-TSP
Hybrid Metaheuristics for the Traveling Salesman Problem (TSP)

This project solves the Traveling Salesman Problem (TSP) using a hybrid metaheuristic approach based on:

- Genetic Algorithm (GA)

- Tabu Search

- Google OR-Tools (benchmark)

The project uses your own Excel dataset containing a distance matrix between U.S. cities.

📂 Project Structure
📁 project/
│── main.py / main.ipynb        # Main solver script
│── data/
│     └── distances.xlsx        # Your distance matrix (included in the repo)
│── README.md                   # Documentation

📊 Input Dataset

The dataset included in the repository contains a precomputed distance matrix.
Rows and columns represent city names, and each cell contains the distance between two cities.

Example (extracted from your file)
	Albuquerque, NM	Atlanta, GA	Austin, TX	Baltimore, MD	Boston, MA
Albuquerque	0	1494	1330	1295	1838
Atlanta	1494	0	2947	1175	2006
Austin	1330	2947	0	2155	1785
Baltimore	1295	1175	2155	0	579
Boston	1838	2006	1785	579	0
Charlotte	2369	389	1221	692	1951
Chicago	666	2934	2813	1380	1004
Requirements

The first row must contain city names

The first column must contain city names

Internal values must be numeric distances

The matrix must be square (n × n)

➡️ No coordinate computation is required — distances are already provided.

🚀 Features

✔ Load a distance matrix directly from Excel
✔ Solve TSP using GA, Tabu Search, and Hybrid GA+Tabu
✔ Compare metaheuristic solutions to OR-Tools reference solution
✔ Extract best tour and total distance
✔ Time performance measurements

🧠 Methodology
---- Genetic Algorithm (GA)

Performs global search through:

-Selection

-Order Crossover (OX)

- Mutation (swap, inversion)

- Elitism

---- Tabu Search

Improves solutions using:

- Neighborhood exploration (swap / 2-opt)

- Tabu list

- Aspiration criteria

- Stopping conditions (iteration limit or stagnation)

---- Hybrid GA + Tabu

Each GA generation:

-Select current best route

- Improve it using Tabu Search

- Inject improved route back into population

OR-Tools Benchmark

Used to:

Validate performance

Compare optimal distance vs heuristic results

🧪 How to Run
Install dependencies
pip install numpy pandas openpyxl ortools

Execute the script
python main.py


Or use the notebook version in Jupyter/Colab.

📈 Outputs

The solver reports:

Best GA distance

Best Tabu Search distance

Best Hybrid distance

OR-Tools reference solution

Execution time per algorithm

Best tour (ordered sequence of cities)

🎯 Purpose

This project is designed for:

Metaheuristics research

TSP experimentation

Operations research and optimization courses

Benchmarking heuristic vs exact solvers

It demonstrates how combining GA and Tabu Search can improve quality and convergence speed.

📜 License

Released under the MIT License.
Free to use, modify, and redistribute for academic or educational purposes.
