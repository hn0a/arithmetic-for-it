# Factoring Prime Numbers in RSA Cryptography

## Factoring Product of Two Prime Numbers

**Explanation in Natural Language:**  
This algorithm focuses on factorizing the product of two prime numbers, which is a key aspect of RSA cryptography. In the context of RSA, the public key is composed of a pair `(n, e)`, where `n` is the product of two prime numbers. The algorithm aims to find these two primes, which is a crucial step in decrypting RSA encrypted messages. It starts with the smallest prime number, 2, and increments through integers to find a divisor of `n`. When a divisor is found, `n` is divided by it to get the second prime number. This factorization is critical because knowing the prime factors allows for the determination of the private key in RSA.

**Pseudo-Code:**
```
Function FactorizeRSAPublicKey(key)
    (n, e) ← key
    Function Search(i)
        If n mod i = 0
            Return i
        Else
            Search(i+1)
    End Function
    res ← Search(2)
    other ← n / res
    Return (res, other)
End Function
```

**Fact:** In RSA cryptography, the security relies on the difficulty of factoring large numbers. The larger the primes used to generate `n`, the more secure the encryption, as factorization becomes computationally impractical.

**Tip:** While this algorithm is conceptually simple, its efficiency decreases significantly with larger numbers. Modern encryption systems use very large primes, making such factorization methods impractical for breaking RSA encryption in real-world scenarios.

