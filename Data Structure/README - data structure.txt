
# Advanced Data Analysis Platform

This project represents a comprehensive data analysis platform designed for modular integration and efficient execution of various computational tasks, including graph operations, sorting and searching algorithms, stack and queue manipulation, and performance analysis. It provides a foundational yet flexible framework for exploring essential data structures and algorithms, tailored for advanced learners and practitioners.

## Core Features

1. Graph Operations:
   - Add tasks with their associated dependencies.
   - Detect the presence of cycles in a directed graph.
   - Execute topological sorting for acyclic graphs.

2. Sorting Algorithms:
   - Implementation of Merge Sort.
   - Implementation of Quick Sort.

3. Searching Algorithm:
   - Binary Search for efficient querying of sorted datasets.

4. Stack and Queue Operations:
   - Dual-stack implementation within a single array for memory optimization.
   - Standard queue operations using Python’s `deque` for efficient management.

5. Performance Benchmarking:
   - Quantify the execution time of functions for comparative analysis.

6. Interactive Console Menu:
   - A command-line interface enabling structured navigation through operations.

## Installation and Setup

1. Prerequisites:
   - Python 3.7 or higher.
   - Libraries: `numpy`, `networkx`.

2. Installation of Dependencies:
   ```bash
   pip install numpy networkx
   ```

3. Execution:
   ```bash
   python <filename>.py
   ```

## Module Breakdown

### 1. GraphModule
- Functionality: Facilitates operations on directed graphs.
- Methods:
  - `add_task(task, dependencies=[])`: Incorporates a task and its dependency graph.
  - `detect_cycle()`: Identifies cycles, returning details if present.
  - `topological_sort()`: Produces a topological ordering for acyclic graphs, raising errors if cycles exist.

### 2. DataOperations
- Purpose: Implements advanced sorting and searching techniques.
- Methods:
  - `merge_sort(arr)`: Recursively sorts an array using divide-and-conquer strategy.
  - `quick_sort(arr)`: Performs in-place sorting leveraging a pivot-based partitioning.
  - `binary_search(arr, target)`: Searches efficiently within a sorted array, returning the index if found.

### 3. StackQueue
- Design: Optimized stack and queue mechanisms for data manipulation.
- Stack Methods:
  - `push_stack1(data)`, `push_stack2(data)`: Insert elements into the respective stack.
  - `pop_stack1()`, `pop_stack2()`: Retrieve and remove elements from the respective stack.
- Queue Methods:
  - `enqueue(data)`: Adds an element to the end of the queue.
  - `dequeue()`: Removes and returns the front element.

### 4. PerformanceModule
- Capability: Provides benchmarking tools for runtime measurement.
- Method:
  - `benchmark(func, *args)`: Executes a function with arguments and reports execution time.

## Usage Instructions

The application launches an interactive menu in the console. Users can select desired functionalities and provide input to execute operations.

### Main Menu Options
1. Graph Operations:
   - Add tasks and dependencies.
   - Detect cycles in the graph.
   - Perform topological sorting.

2. Sorting Algorithms:
   - Execute merge sort or quick sort.
   - Input a dataset for sorting.

3. Searching Algorithms:
   - Perform binary search on a sorted dataset.

4. Stack Operations:
   - Push and pop operations on dual stacks.

5. Queue Operations:
   - Enqueue and dequeue operations.

6. Exit:
   - Terminate the program.

### Illustrative Examples

#### Adding Graph Tasks
```
Enter task name: Task1
Enter dependencies (comma-separated): Task2,Task3
```

#### Sorting Operations
```
Enter numbers (space-separated): 10 5 2 8
Sorted Data (Merge Sort): 2 5 8 10
```

#### Binary Search Example
```
Enter numbers (space-separated): 1 2 3 4 5
Enter target number: 3
Index of target: 2
```

## Error Handling Mechanisms
- Cycle detection in graphs ensures logical validity before topological sorting.
- Explicit handling of stack overflow and underflow scenarios with descriptive error feedback.
- Queue underflow protection prevents invalid dequeue operations.

## Performance Measurement Example
To benchmark sorting operations, use:
```python
result, elapsed_time = PerformanceModule.benchmark(DataOperations.merge_sort, [10, 5, 2, 8])
print(f"Sorted Data: {result}, Time Taken: {elapsed_time} seconds")
```

## Key Dependencies
- `numpy`: Supports efficient array processing and manipulation.
- `networkx`: Provides advanced tools for graph representation and analysis.
- `collections.deque`: Implements a high-performance queue.

## Prospective Enhancements
- Extend support to weighted graphs and shortest-path algorithms (e.g., Dijkstra’s, Bellman-Ford).
- Integrate additional sorting algorithms such as heap sort.
- Enrich the user interface with visualization options for graph structures and sorting steps.