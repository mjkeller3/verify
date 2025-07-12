# Matthew James Keller Identity Verification

This repository hosts a simple webpage to verify signatures signed by Matthew James Keller's private key.

## How to Use

1. **Generate a challenge** (random string) — the verifier provides this.

2. **Sign the challenge** with the private key (not included here).  
   Example signing command with OpenSSL:

   ```bash
   echo -n "your-challenge-string" | openssl dgst -sha256 -sign private.pem | base64
