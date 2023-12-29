
# Basic Arithmetics for Ordered Euclidian Ring: Case of Bitarrays

## Implementing Basic Arithmetic Operations on Bitarrays

### Computing the Greatest Common Divisor (GCD) of Bitarrays
**Explanation in Natural Language:**  
The function `gcd_b` computes the greatest common divisor (GCD) of two non-zero bitarrays `bA` and `bB`. It uses the Euclidean algorithm, repeatedly taking the modulus of the bitarrays until the remainder is zero, at which point the last non-zero remainder is the GCD.

**Pseudo-Code:**
```
Function GCDB(bA, bB)
    Convert bA and bB to their absolute values
    Recursively compute GCD using the Euclidean algorithm
    Return the GCD
End Function
```

### Extended Euclidean Division of Bitarrays
**Explanation in Natural Language:**  
The `bezout_b` function computes the coefficients of the Bézout's identity for two bitarrays `bA` and `bB`. It finds `u`, `v`, and `d` such that `a*u + b*v = d`, where `d` is the GCD of `a` and `b`. This is useful in solving linear Diophantine equations and computing modular inverses.

**Pseudo-Code:**
```
Function BezoutB(bA, bB)
    If bA is zero, return the base case values
    Otherwise, recursively apply the algorithm
    Adjust the coefficients in each step
    Return the coefficients and GCD
End Function
```

**Fact:** GCD and Extended Euclidean algorithms are fundamental in number theory and have applications in cryptography, particularly in algorithms like RSA.

**Tip:** Understanding these algorithms is crucial for their application in areas such as cryptographic key generation and solving modular linear equations.
