# Task 4 — Cryptography Notes


## 1. Goals of cryptography
- **Confidentiality** — keep data secret.
- **Integrity** — ensure data isn't altered undetectably.
- **Authentication** — verify sender/receiver identity.
- **Non-repudiation** — prevent denial of actions.


## 2. Symmetric vs Asymmetric
- **Symmetric encryption**: same key for encrypt/decrypt (AES, 3DES). Fast, used for bulk encryption. Key distribution is a challenge.
- **Asymmetric encryption**: public/private key pairs (RSA, ECC). Public key encrypts, private key decrypts (or signs). Useful for key exchange and signatures.


## 3. Hashing
- One-way functions producing fixed-size digests (SHA-256, SHA-1, MD5). Use cases: integrity checks, password storage (with salt + slow KDFs like bcrypt/scrypt).
- **Important**: MD5 and SHA-1 are considered broken for collision resistance — avoid for security-critical systems.


## 4. Common algorithms & purposes
- **AES (symmetric)** — AES-128/192/256 for confidentiality.
- **RSA (asymmetric)** — 2048-bit or higher keys for encryption/signing.
- **ECC (asymmetric)** — smaller keys with similar security (e.g., secp256r1).
- **SHA-256** — hashing for integrity.


## 5. OpenSSL quick commands (practical)
### Generate a 2048-bit RSA key


## 6. Password storage best practices (lab notes)
- Never store plaintext passwords.
- Use salted hashes + a slow KDF (bcrypt, Argon2) for user passwords.


## 7. TLS basics
- TLS provides confidentiality and integrity via a combination of asymmetric (key exchange) and symmetric (bulk cipher) algorithms.
- Certificates bind public keys to identities; browsers trust certs signed by known CAs.


## 8. Practical exercise suggestions
- Create a self-signed cert and serve a small HTTPS site in the lab.
- Use `openssl s_client -connect 192.168.56.20:443` to view TLS handshake details.
