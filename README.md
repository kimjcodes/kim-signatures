# Kim's Bitcoin Signatures

Daily cryptographic proof of existence using Bitcoin message signing.

## How It Works

Every day, I sign a message with my Bitcoin private key:
- **Message format:** `Kim YY-MM-DD`
- **Address:** `1LU67hyXTEZGg38PMvKo4q5sLJ13z3CVL1`

I post the **short signature** on social media:
```
🔑 IO/ZW...og9k=
```

The **full signature** is stored here for verification.

---

## Quick Lookup

### By Date
Browse: [`by-YearMonth/`](by-YearMonth/)

### By Short Signature
Use GitHub's search: type the short sig (e.g., `IO/ZW...og9k=`) in the search bar.

### Programmatic Access
See [`signatures.json`](signatures.json)

---

## Recent Signatures

| Date | Short Sig | Full |
|------|-----------|------|
| [2026-02-09](by-YearMonth/2026-02/KimJBTC-2026-02-09.md) | `IO/ZW...og9k=` | [View](by-YearMonth/2026-02/KimJBTC-2026-02-09.md) |

---

## Verify a Signature

### Option 1: Online
1. Go to [bitcoin.com/tools/verify-message](https://www.bitcoin.com/tools/verify-message/)
2. Enter:
   - **Address:** `1LU67hyXTEZGg38PMvKo4q5sLJ13z3CVL1`
   - **Message:** `Kim YY-MM-DD` (the date)
   - **Signature:** (the full signature from the daily file)
3. Click Verify

### Option 2: Bitcoin CLI
```bash
bitcoin-cli verifymessage \
  "1LU67hyXTEZGg38PMvKo4q5sLJ13z3CVL1" \
  "FULL_SIGNATURE_HERE" \
  "Kim YY-MM-DD"
```

---

## Why?

Proof that I existed and posted on a specific day. The signature can only be created by someone who controls the private key for address `1LU67hyXTEZGg38PMvKo4q5sLJ13z3CVL1`.

No AI, no impersonator, no time traveler can fake this.

---

## Find Me

- **Twitter:** [@KimJBTC](https://x.com/KimJBTC)
- **Skool:** [Blueprint for Bitcoin](https://skool.com/b4b)

---

*Stack sats. Sign messages. Stay verifiable.* 🔑
