## GAVC (Geometrical Affine Vector Cipher) by Mike Zorbas
This cipher uses a vector space approach with random orthogonal transformations,
translations, and permutations to encrypt and decrypt messages.
This cipher is designed to work with byte arrays, treating them as vectors in a high-dimensional space.

This mechanism could resist linear and differential cryptanalysis due to the randomness introduced in each step.
This has quantum-resistant properties.

HMAC is used for integrity verification of the ciphertext.
The cipher is designed to be secure against both classical and quantum attacks.
(IV) Initialization Vector is used to ensure that the same plaintext encrypted multiple times will yield different ciphertexts.

# TO DO

- [ ] Harden all randomness (IV tracking, HKDF separation)
- [ ] Write game-based IND-CCA2 proof sketch
- [ ] Make matrix ops constant-time and test against side-channels
- [ ] Add AEAD-style support
- [ ] Use non-Abelian or cryptographically stronger matrix rings (optional)
- [ ] Add config/versioning, better API
- [ ] Benchmark and compare performance to AES-GCM
