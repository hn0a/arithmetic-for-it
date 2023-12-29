
# Power Function Implementations for Builtin Integers

## Implementing Various Power Functions in OCaml

### Naive Power Function (Linear Complexity)
**Explanation in Natural Language:**  
The `pow` function computes the power of a base `x` raised to an exponent `n` in a straightforward, linear manner. For positive exponents, it recursively multiplies `x` by itself `n` times. For negative exponents, it divides 1 by `x` `n` times.

**Pseudo-Code:**
```
Function Pow(x, n)
    If n is positive
        Recursively multiply x by itself n times
    Else
        Recursively divide 1 by x n times
    Return the result
End Function
```

### Fast Integer Exponentiation (Logarithmic Complexity)
**Explanation in Natural Language:**  
The `power` function is a more efficient implementation, using a logarithmic approach. It reduces the number of multiplications by squaring the base and halving the exponent in each step, effectively decreasing the time complexity.

**Pseudo-Code:**
```
Function Power(x, n)
    If n is 0
        Return 1
    If n is positive
        Recursively compute x^2 raised to half of n
    Else
        Recursively compute 1 divided by x^2 raised to half of -n
    Return the result
End Function
```

### Fast Modular Exponentiation
**Explanation in Natural Language:**  
The `mod_power` function extends the fast exponentiation to modular arithmetic. It computes `(x^n) mod m` efficiently, ensuring that intermediate results remain within the bounds of the modular base `m`.

**Pseudo-Code:**
```
Function ModPower(x, n, m)
    Recursively compute x^n mod m using fast exponentiation
    Adjust the result to be within the bounds of m
    Return the result
End Function
```

### Fast Modular Exponentiation Mod Prime (Using Fermat's Little Theorem)
**Explanation in Natural Language:**  
The `prime_mod_power` function is specifically optimized for a prime modular base `p`. It utilizes Fermat's Little Theorem to efficiently compute `(x^n) mod p`. This function is particularly useful in cryptographic applications.

**Pseudo-Code:**
```
Function PrimeModPower(x, n, p)
    If n is 0
        Return 1
    Use Fermat's Little Theorem to optimize calculations
    Recursively compute x^n mod p
    Adjust the result to be within the bounds of p
    Return the result
End Function
```

**Fact:** The efficiency of power functions is crucial in computational mathematics, particularly in fields like cryptography, where fast exponentiation underpins many algorithms.

**Tip:** Choosing the right power function can significantly impact the performance of algorithms, especially when dealing with large numbers or in resource-constrained environments.
