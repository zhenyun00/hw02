# hw02
```mermaid
gantt
    title Project Tasks Gantt Chart
    dateFormat  YYYY-MM-DD
    section Task 1
    Research Plan         :done,    t1, 2024-01-01, 1d
    Task Allocation       :done,    t2, 2024-01-02, 4d
    Hardware Acquisition  :done,    t3, 2024-01-06, 17d
    section Task 2
    Program Development   :active,  t4, 2024-01-23, 70d
    Hardware Installation :         t5, 2024-02-01, 10d
    Program Testing       :         t6, 2024-03-12, 30d
    User Manual Writing   :         t7, 2024-04-11, 25d
    Data Conversion       :         t8, 2024-04-06, 20d
    System Testing        :         t9, 2024-05-01, 25d
    User Training         :         t10, 2024-05-26, 20d
    User Testing          :         t11, 2024-06-15, 25d
```
# Let's first define the tasks with their durations and dependencies for CPM/PERT analysis
import networkx as nx

# Tasks data: Task number, duration (in days), prerequisites (list of task numbers)
tasks = {
    1: {'duration': 1, 'prerequisites': []},
    2: {'duration': 4, 'prerequisites': [1]},
    3: {'duration': 17, 'prerequisites': [1]},
    4: {'duration': 70, 'prerequisites': [2]},
    5: {'duration': 10, 'prerequisites': [3]},
    6: {'duration': 30, 'prerequisites': [4]},
    7: {'duration': 25, 'prerequisites': [5]},
    8: {'duration': 20, 'prerequisites': [5]},
    9: {'duration': 25, 'prerequisites': [6]},
    10: {'duration': 20, 'prerequisites': [7, 8]},
    11: {'duration': 25, 'prerequisites': [9, 10]}
}

# Create a directed graph for PERT/CPM
G = nx.DiGraph()

# Add tasks as nodes and their dependencies as edges
for task, data in tasks.items():
    G.add_node(task, duration=data['duration'])
    for prereq in data['prerequisites']:
        G.add_edge(prereq, task)

# Now, we will compute the longest path (critical path) using networkx's built-in function.
# This will also serve as the Critical Path Method (CPM) result.
critical_path = nx.dag_longest_path(G, weight='duration')
critical_path_length = nx.dag_longest_path_length(G, weight='duration')

# We will visualize the PERT/CPM network and the Gantt chart for these tasks next.
# First, let's return the critical path and its length.
critical_path, critical_path_length
