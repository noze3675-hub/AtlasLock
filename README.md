# AtlasLock
Windows folder encryption tool (.atlas format) using Argon2 + XChaCha20-Poly1305 + Zstd compression. Runs locally · No telemetry.


<img width="460" height="412" alt="Screenshot 2025-11-24 190237" src="https://github.com/user-attachments/assets/c556b2cb-e76a-4ed0-9a3b-5dcfb6b67486" />


AtlasLock is designed with a modern, defense-in-depth security model rather than relying on legacy archive formats.

Strong password protection – User passwords are processed through a modern, memory-hard password hashing function from the Argon2 family, making large-scale brute-force attacks significantly more expensive compared to traditional ZIP/RAR style encryption.

Authenticated encryption – All user data is encrypted with an AEAD (authenticated encryption with associated data) construction from a well-audited cryptographic library. This ensures that files are not only confidential, but also protected against silent tampering or corruption.

Per-archive salts and unique keys – Each .atlas archive uses its own random salt and derived key material, so compromising one archive does not help an attacker with any other archive.

Integrity of metadata – Not only the file contents, but also the internal structure and metadata of the archive are protected by integrity checks, so modified or truncated archives are detected during unlock rather than producing partial or corrupted output.

Streaming architecture – Encryption and decryption are implemented in a streaming fashion, so large folders can be processed without keeping everything in memory at once. This reduces the attack surface and avoids unsafe ad-hoc buffering.

Local-only cryptography – All cryptographic operations run entirely on the user’s device. No keys or file contents are sent to remote servers, and AtlasLock does not rely on any cloud component.

Secure defaults – The application uses safe defaults for cryptographic parameters and does not expose low-level tuning options that could accidentally weaken security.

In short, AtlasLock aims to behave like a dedicated, modern encryption tool rather than a “fancy archive format”, focusing on strong password resistance, authenticated encryption, and predictable, local-only behavior.

File to .atlas

<img width="280" height="177" alt="Screenshot 2025-11-24 190211" src="https://github.com/user-attachments/assets/dfb8fea0-9802-41e2-a986-c6bf8f67d0e5" />

<img width="826" height="512" alt="Screenshot 2025-11-24 185252" src="https://github.com/user-attachments/assets/2b4e8842-5bc6-408b-9355-4b75cfdfd03b" />
<img width="1508" height="489" alt="Screenshot 2025-11-24 185303" src="https://github.com/user-attachments/assets/591fda39-7df6-4630-9fee-54621d09a1c9" />
