
# Factoring Bitarrays into Primes

## Implementing Prime Factorization of Bitarrays for Cryptographic Applications

### Factoring Product of Two Prime Bitarrays
**Explanation in Natural Language:**  
The function `break` factors a product of two prime bitarrays, typically representing the public key of an RSA cryptosystem. It iteratively searches for a divisor of the bitarray `n` (part of the key) starting from the smallest prime bitarray. Once a divisor is found, the function divides `n` by this divisor to obtain the other prime.

**Pseudo-Code:**
```
Function Break(key)
    Extract n (product of primes) from the key
    Start searching for divisors from the smallest prime bitarray
    If a divisor is found, divide n by this divisor to find the other prime
    Return the pair of prime bitarrays
End Function
```

**Fact:** Factoring large numbers into primes is a fundamental problem in cryptography, especially for RSA where the security depends on the difficulty of this factorization.

**Tip:** The ability to factor large bitarrays into primes efficiently is crucial for certain cryptographic attacks, such as breaking RSA encryption under specific conditions.
