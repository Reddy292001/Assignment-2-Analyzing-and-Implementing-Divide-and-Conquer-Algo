# Assignment 2: Analyzing and Implementing Divide-and-Conquer Algorithms

## Overview
This Python script compares two divide-and-conquer sorting algorithms: **Merge Sort** and **Quick Sort**. It tests them on three types of datasets:

- Sorted data
- Reverse-sorted data
- Random data

For each test, the script records:

- Execution time
- Peak memory usage

The goal is to analyze how both algorithms behave under different input conditions and to observe the trade-offs between speed and memory usage. :contentReference[oaicite:0]{index=0}

## Algorithms Used

### Merge Sort
Merge Sort follows the divide-and-conquer strategy by:

- Dividing the list into two halves
- Recursively sorting each half
- Merging the sorted halves into one final sorted list

This implementation returns a new sorted list and uses extra memory during the merge process. :contentReference[oaicite:1]{index=1}

### Quick Sort
Quick Sort also uses divide-and-conquer by:

- Choosing a pivot
- Partitioning the array around the pivot
- Recursively sorting the left and right partitions

In this script, the **last element is always used as the pivot**. This is intentional so that the algorithm shows its worst-case behavior on already sorted and reverse-sorted inputs. :contentReference[oaicite:2]{index=2} :contentReference[oaicite:3]{index=3}

## Dataset Types
The script generates three dataset types for testing:

- `sorted`
- `reverse_sorted`
- `random`

The input sizes tested are:

- 500
- 1000
- 1500

This allows comparison of performance across both different input structures and different dataset sizes. :contentReference[oaicite:4]{index=4} :contentReference[oaicite:5]{index=5}

## Performance Measurement
The script measures:

- **Execution time** using `time.perf_counter()`
- **Peak memory usage** using `tracemalloc`

A small warm-up sort is also performed before measurement to reduce one-time startup effects. :contentReference[oaicite:6]{index=6}

## Output
After running all experiments, the script saves the results to a CSV file named:

`sorting_results.csv`

It also prints the results to the console in a readable format showing:

- Input size
- Dataset type
- Merge Sort time and memory
- Quick Sort time and memory :contentReference[oaicite:7]{index=7} :contentReference[oaicite:8]{index=8}

## Requirements
This script uses only Python standard library modules:

- `random`
- `time`
- `tracemalloc`
- `csv`
- `sys`
- `pathlib`

No external packages are required. :contentReference[oaicite:9]{index=9}

## How to Run
Run the script from the terminal using:

```bash
python assignment_2_analyzing_and_implementing_divide_and_conquer_algorithms.py
