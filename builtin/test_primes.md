
# Testing for Primality: Deterministic and Probabilistic Methods

## Implementing Primality Tests in OCaml

### Deterministic Primality Test
**Explanation in Natural Language:**  
The function `is_prime` deterministically tests if a number `n` is prime. It checks if any integer from 2 up to the square root of `n` divides `n`. If any such divisor is found, `n` is not prime; otherwise, it is prime.

**Pseudo-Code:**
```
Function IsPrime(n)
    If n is less than 2
        Return false (as primes are greater than 1)
    Check divisibility from 2 up to the square root of n
    Return true if no divisors found, otherwise false
End Function
```

### Primality Test Based on Small Fermat Theorem
**Explanation in Natural Language:**  
The `is_pseudo_prime` function uses the Fermat primality test, a probabilistic method. It tests the integer `p` against a sequence of numbers (`test_seq`). If `p` satisfies the condition `(a^(p-1)) mod p = 1` for all `a` in `test_seq`, then `p` is likely prime.

**Pseudo-Code:**
```
Function IsPseudoPrime(p, test_seq)
    For each element e in test_seq
        Check if (e^(p-1)) mod p equals 1
        If not, return false
    Return true if all tests pass
End Function
```

**Fact:** Deterministic tests for primality are exact but can be slow for large numbers. Probabilistic tests like Fermat's offer faster alternatives but with a trade-off in certainty.

**Tip:** In practical applications like cryptography, probabilistic primality tests are often preferred due to their efficiency, especially when working with very large numbers.
