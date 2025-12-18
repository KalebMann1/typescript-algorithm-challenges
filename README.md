# TypeScript Algorithm Challenges

This repository contains a few small algorithmic problems implemented in
TypeScript. Each problem focuses on a different area: permutations and
combinatorics, counting coin-change combinations, and working with word values
and figurate numbers.

The code is written as simple functions with minimal dependencies so it can be
run with `ts-node` or compiled with `tsc`.

---

## Problems

### 1. Millionth Lexicographic Permutation

Given the digits `0–9`, generate all permutations in lexicographic (sorted)
order and find the **millionth** permutation in that ordering.

Key ideas:

- Factorial number system / ranking permutations
- Avoiding brute-force generation of all 10! permutations

File: `src/problem01_lexicographicPermutation.ts`

---

### 2. Ways to Make £2 with UK Coins

Using UK coin denominations:  
`1p, 2p, 5p, 10p, 20p, 50p, £1 (100p), £2 (200p)`

Count how many different ways there are to make **200 pence** using any number
of coins.

Key ideas:

- Dynamic programming for coin-change counting
- Representing amounts in pence (integers) instead of floating point

File: `src/problem02_coinSums.ts`

---

### 3. Triangle Words

A triangle number is defined by:

\[
t_n = \frac{1}{2} n (n + 1)
\]

For a given list of words, each word is assigned a value equal to the sum of
its letters’ positions in the alphabet (`A=1, B=2, ..., Z=26`). A word is a
*triangle word* if its value is a triangle number.

Using `data/words.txt`, count how many of the words are triangle words.

Key ideas:

- Reading and parsing a text file in Node/TypeScript
- Mapping characters to numeric values
- Precomputing triangle numbers and membership checking

File: `src/problem03_triangleWords.ts`

---

## Running the Code

With `ts-node`:

```bash
npm install -D typescript ts-node
npx ts-node src/problem01_lexicographicPermutation.ts
npx ts-node src/problem02_coinSums.ts
npx ts-node src/problem03_triangleWords.ts
