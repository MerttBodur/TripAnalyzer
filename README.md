# CMP2003 – Trip Analyzer Term Project

## Overview
This project is part of **CMP2003 – Data Structures** and focuses on building a **robust, efficient, and deterministic data analysis tool** for processing trip records stored in CSV format. Students are required to implement a `TripAnalyzer` class that ingests trip data, aggregates statistics, and returns ranked analytical results under strict correctness and performance constraints.

The project is **data-structure agnostic by design**: you are not told which data structures to use. Any correct STL-based solution is acceptable, but inefficient approaches will fail performance-gated tests.

---

## Learning Objectives
By completing this project, students will demonstrate the ability to:

- Parse large CSV files safely without crashing
- Handle malformed (dirty) data robustly
- Design efficient aggregation logic using STL containers
- Implement deterministic multi-key sorting
- Respect performance constraints and asymptotic complexity
- Write code that scales from small test files to millions of rows

---

## How It Works
1. The program reads the `.csv` file line by line.  
2. Each line is parsed and the hour field is validated.  
3. Incorrect entries are skipped using `continue`.  
4. Valid data is inserted into an `unordered_map`.  
5. The stored data is sorted by frequency.  
6. The system outputs the most frequently used areas and hours.

---

## Time Complexity

ingestFile -> topZones -> topBusySlots

O(n.lengthofinput) -> O(ZlogZ) -> O(SlogS)
Z = number of elements inside the ZoneCounts map
S = number of elements inside the SlotCounts map
Since the dominant operation is the line-by-line ingestion and parsing of the CSV file, the overall time complexity of the program is O(n · L), where n is the number of rows and L is the maximum length of a row. Because L is bounded by the fixed CSV schema, the effective runtime is linear, O(n).







