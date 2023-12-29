
# Factoring Big Integers into Primes

## Implementing Prime Factorization of Big Integers for Cryptographic Applications

### Factoring Product of Two Prime Big Integers
**Explanation in Natural Language:**  
The `break` function factors a product of two prime big integers, typically representing the public key of an RSA cryptosystem. It searches for a divisor of the big integer `n` (part of the key) starting from the smallest prime, 2. Once a divisor is found, the function divides `n` by this divisor to obtain the other prime.

**Pseudo-Code:**
```
Function Break(key)
    Extract n from the key
    Start searching for divisors from 2
    If a divisor is found, divide n by this divisor to find the other prime
    Return the pair of prime big integers
End Function
```

**Fact:** Factoring large numbers into primes is a critical problem in cryptography, especially for RSA, where the security is based on the difficulty of this factorization.

**Tip:** Efficient factorization algorithms are key in cryptographic analysis and attacks, such as breaking RSA encryption under certain conditions.

