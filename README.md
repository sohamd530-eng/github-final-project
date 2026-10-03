# Simple Interest Calculator

A simple interest calculator project developed for the IBM Developer Skills Network course on Git and GitHub.

## Overview
This repository contains a Bash script (`simple-interest.sh`) designed to compute simple interest based on user inputs.

## Formula
Simple Interest is calculated using the standard formula:
$$Simple Interest = \frac{P \times R \times T}{100}$$

Where:
- **P** = Principal amount
- **R** = Annual rate of interest (%)
- **T** = Time period in years

## Usage
Run the Bash script in your terminal:
```bash
chmod +x simple-interest.sh
./simple-interest.sh
```

### Input Fields:
1. **Principal Amount**: Enter the starting principal.
2. **Rate of Interest**: Enter the annual interest rate.
3. **Time Period**: Enter the time duration in years.

### Code Snippet (`simple-interest.sh`):
```bash
#!/bin/bash
read -p "Enter Principal Amount (P): " principal
read -p "Enter Rate of Interest (R %): " rate
read -p "Enter Time Period in years (T): " time_period

interest=$(echo "scale=2; ($principal * $rate * $time_period) / 100" | bc)
echo "Simple Interest: $interest"
```

## License
Licensed under the [Apache 2.0 License](LICENSE).
