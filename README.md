
# Profile Packing Algorithm

This repository contains an implementation of the Profile Packing algorithm based on the article "Online Bin Packing with Predictions" by Spyros Angelopoulos, Shahin Kamali, and Kimia Shadkami.

## Table of Contents

- [Overview](#overview)
- [Algorithm Description](#algorithm-description)
- [Usage](#usage)
- [Example](#example)
- [Authors and Acknowledgments](#authors-and-acknowledgments)


## Overview

The Profile Packing algorithm is designed to efficiently pack items of various sizes into bins based on predicted item frequencies. The goal is to minimize the number of bins used by leveraging a profile of expected item distributions.

## Algorithm Description

### Steps of the Algorithm

1. **Form the Profile Set `Pf`**:
   - Convert predicted frequencies into actual counts of items.

2. **Compute an Optimal Packing of `Pf`**:
   - Pack items from the profile set into bins using a dummy implementation of an optimal packing function.

3. **Initialize Bins**:
   - Create bins for items, separating them into NonEmpty, Empty, and Special categories.

4. **Process Each Item in the Input Sequence**:
   - Place each item into the appropriate bin based on available placeholders or treat it as a special item if no suitable bin is found.

5. **Combine and Return the Results**:
   - Combine all bins to get the final packed bins.

## Usage

Clone this repository and run the provided code with your own input sequences and predicted frequencies.

```python
def profile_packing(w, f, m, k):
    # Implementation details
    ...

# Example Usage
w = [1, 2, 3, 4, 5, 6, 7, 1, 1, 10]  # Input sequence of item sizes
f = [0.11, 0.53, 0.15, 0.10, 0, 0.03, 0.05, 0, 0.03, 0]  # Predicted frequencies of item sizes
m = 20  # Total number of items to consider
k = 10  # Maximum item size

packed_bins = profile_packing(w, f, m, k)
print("Packed Bins:", packed_bins)
```

## Example

Here's an example of how to use the Profile Packing algorithm:

```python
# Example Usage
w = [1, 2, 3, 4, 5, 6, 7, 1, 1, 10]  # Input sequence of item sizes
f = [0.11, 0.53, 0.15, 0.10, 0, 0.03, 0.05, 0, 0.03, 0]  # Predicted frequencies of item sizes
m = 20  # Total number of items to consider
k = 10  # Maximum item size

packed_bins = profile_packing(w, f, m, k)
print("Packed Bins:", packed_bins)
```


## Authors and Acknowledgments

This code was implemented based on the article "Online Bin Packing with Predictions" by Spyros Angelopoulos, Shahin Kamali, and Kimia Shadkami. The algorithm efficiently packs items into bins using predicted item frequencies to minimize the number of bins used.
