# TOPSIS Python Package – Assignment Submission

## Package Information

**Package Name:** topsis-anshika-102317059  
**Version:** 1.0.0  
**Author:** Anshika Ahuja  
**Roll Number:** 102317059  
**Published on PyPI:** Jan 20, 2026  

Install the package using:

```bash
pip install topsis-anshika-102317059==1.0.0
```

---

## Overview

This project implements the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** algorithm in Python and publishes it as an installable PyPI package.

TOPSIS is a Multi-Criteria Decision Making (MCDM) technique used to rank alternatives based on their distance from:

- Ideal Best Solution
- Ideal Worst Solution

The package accepts input data in CSV format, applies weights and impacts, calculates TOPSIS scores, and generates rankings.

---

## Assignment Objective

The objective of this assignment was to:

- Implement TOPSIS algorithm in Python
- Create a Python package
- Publish the package on PyPI
- Accept CSV input file
- Accept weights and impacts as parameters
- Calculate TOPSIS scores
- Rank alternatives
- Generate output CSV file

All assignment requirements have been successfully implemented.

---

## Command Line Usage

After installing the package, run:

```bash
topsis <InputDataFile> <Weights> <Impacts> <OutputFile>
```

### Example

```bash
topsis data.csv "1,1,1,1,1" "+,+,+,+,+" output.csv
```

---

## Input File Format

The input file must be a CSV file.

Example:

```
Fund Name,P1,P2,P3,P4,P5
M1,0.67,0.45,6.5,42.6,12.56
M2,0.60,0.36,3.6,53.3,14.47
M3,0.82,0.67,3.8,63.1,17.10
M4,0.60,0.36,3.5,69.2,18.42
M5,0.76,0.58,4.8,43.0,12.29
M6,0.69,0.48,6.6,48.7,14.12
M7,0.79,0.62,4.8,59.2,16.35
M8,0.84,0.71,6.5,34.5,10.64
```

### Input Requirements

- First column must contain alternative names
- All other columns must contain numeric values only
- Weights must be numeric and comma-separated
- Impacts must be '+' or '-' and comma-separated

Example:

Weights:
```
1,1,1,1,1
```

Impacts:
```
+,+,+,+,+
```

---

## Output

The output file will contain:

- Original data
- TOPSIS Score
- Rank

Example output:

```
Fund Name  P1    P2    P3    P4    P5    Topsis Score  Rank
M1         0.67  0.45  6.5   42.6  12.56 0.4354        7
M2         0.60  0.36  3.6   53.3  14.47 0.3038        3
M3         0.82  0.67  3.8   63.1  17.10 0.6269        8
M4         0.60  0.36  3.5   69.2  18.42 0.4730        6
M5         0.76  0.58  4.8   43.0  12.29 0.4177        4
M6         0.69  0.48  6.6   48.7  14.12 0.5234        1
M7         0.79  0.62  4.8   59.2  16.35 0.6514        5
M8         0.84  0.71  6.5   34.5  10.64 0.5237        2
```

---

## Algorithm Explanation

TOPSIS follows these steps:

1. Construct decision matrix
2. Normalize decision matrix
3. Multiply normalized matrix with weights
4. Determine ideal best and ideal worst values
5. Calculate Euclidean distance from ideal best and worst
6. Compute TOPSIS score
7. Rank alternatives based on score

### Formula Used

```
Score = S− / (S+ + S−)
```

Where:

- S+ = Distance from ideal best
- S− = Distance from ideal worst

Higher score indicates better alternative.

---

## Technologies Used

- Python 3
- Pandas
- NumPy
- setuptools
- PyPI

---

## Features

- Python package implementation
- PyPI deployment
- Command line interface
- CSV input support
- Weight and impact validation
- Automatic ranking generation
- Output CSV generation

---

## How to Run

Step 1: Install package

```bash
pip install topsis-anshika-102317059==1.0.0
```

Step 2: Run TOPSIS

```bash
topsis data.csv "1,1,1,1,1" "+,+,+,+,+" output.csv
```

Step 3: Check output.csv for results

---

## Assignment Reference

This project was developed as part of the TOPSIS Python Packaging Assignment.

---

## Author

Anshika Ahuja  
Roll Number: 102317059  

---

## License

This project is for academic purposes only.
