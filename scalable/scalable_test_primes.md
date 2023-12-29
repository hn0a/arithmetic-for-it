
# Testing for Primality Using Bitarrays

## Implementing Primality Tests with Bitarrays

### Deterministic Primality Test
**Explanation in Natural Language:**  
The `is_prime` function deterministically tests if a bitarray `n` represents a prime number. It checks divisibility by all bitarrays from 2 up to the square root of `n`. If any divisor is found, `n` is not prime; otherwise, it is prime.

**Pseudo-Code:**
```
Function IsPrime(n)
    If n is less than 2, return false
    Check divisibility from 2 up to the square root of n
    Return true if no divisors found, else false
End Function
```

### Pseudo-Primality Test Based on Fermat's Little Theorem
**Explanation in Natural Language:**  
The `is_pseudo_prime` function uses Fermat's primality test, a probabilistic method. For a bitarray `p` and a sequence of test bitarrays `test_seq`, `p` is likely prime if it satisfies `(a^(p-1)) mod p = 1` for all `a` in `test_seq`.

**Pseudo-Code:**
```
Function IsPseudoPrime(p, test_seq)
    For each element e in test_seq
        Check if (e^(p-1)) mod p equals 1
        If not, return false
    Return true if all tests pass
End Function
```

**Fact:** Deterministic tests for primality are exact but can be slow for large bitarrays. Probabilistic tests like Fermat's offer faster but less certain alternatives.

**Tip:** Understanding these primality tests is crucial for applications in cryptography, where identifying prime numbers is a fundamental step in key generation.
