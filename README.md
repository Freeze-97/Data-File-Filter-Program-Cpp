# Data File Filter Program (C++)
This C++ program reads numerical values from a file, filters them based on a specified valid range, and handles both format and range errors. It demonstrates template usage, file I/O, exception handling, and basic data filtering.

## Description
The program performs the following tasks:

Reads values from an input file (Values.dat) using a templated class DataFileReader<T>.

Filters those values to check if they fall within a specified numeric range (0.0 to 10.0) using DataFilter<T>.

Handles errors:

Invalid input format → written to Error.dat

Out-of-range values → written to rangeError.dat

Calculates statistics:

Number of valid values

Sum of valid values

Average of valid values

Displays results in the terminal.

## File Overview
dataFileReader.h / .cpp: Templated class for reading values from a file with error handling for bad input.

dataFilter.h / .cpp: Templated class that filters values outside a defined range and throws exceptions.

testProgram.h / .cpp: Contains the TestProgram class that drives the program logic and displays results.

Values.dat: Input data file (must be created by the user).

Error.dat: Output file for invalid input lines.

rangeError.dat: Output file for values outside the valid range.

## How to Compile
```bash
g++ -std=c++17 -o data_filter main.cpp testProgram.cpp dataFileReader.cpp dataFilter.cpp
```

## How to Run
Make sure a file named Values.dat exists in the same directory, with one numeric value per line. Then run:
```bash
./data_filter
```

