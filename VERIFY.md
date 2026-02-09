# How to Verify Kim's Signatures

## What You Need

1. **Address:** `1LU67hyXTEZGg38PMvKo4q5sLJ13z3CVL1`
2. **Message:** `Kim YY-MM-DD` (e.g., `Kim 26-02-09`)
3. **Signature:** The full signature from the daily file

## Method 1: Online (Easiest)

1. Go to [bitcoin.com/tools/verify-message](https://www.bitcoin.com/tools/verify-message/)
2. Paste the **Address**
3. Paste the **Message** (exactly as shown, including "Kim ")
4. Paste the **Full Signature**
5. Click **Verify Message**
6. Should show: ✅ **Verified**

## Method 2: Bitcoin Core CLI

If you run a Bitcoin node:

```bash
bitcoin-cli verifymessage \
  "1LU67hyXTEZGg38PMvKo4q5sLJ13z3CVL1" \
  "SIGNATURE_HERE" \
  "Kim YY-MM-DD"
```

Returns `true` if valid.

## Method 3: Electrum

1. Open Electrum
2. Go to **Tools → Verify Message**
3. Enter the address, message, and signature
4. Click **Verify**

## Method 4: Python

```python
from bitcoinlib.wallets import *

address = "1LU67hyXTEZGg38PMvKo4q5sLJ13z3CVL1"
message = "Kim 26-02-09"
signature = "IO/ZW9UvT1ShTqLdUEeb7eQak2KU21zcEpp6UX9B5S0ENH4rinmA07LfoX3o4sOlabkDjXYJhNBb8kd/PcPog9k="

# Use appropriate library to verify
```

## What This Proves

A valid signature proves that:
1. The person who signed **controls the private key** for that address
2. The message was signed **exactly as shown** (any change = invalid)
3. The signature **cannot be forged** without the private key

It does NOT prove:
- When the signature was created (only what date is in the message)
- The identity of the signer (only that they control the key)

## Troubleshooting

**"Invalid signature"**
- Check the message is EXACTLY right (including spaces and capitalization)
- Make sure you're using the FULL signature, not the short version
- Verify the address matches

**"Address invalid"**
- Ensure no extra spaces or characters
- The address should start with `1LU67...`

---

*Questions? Find me on Twitter [@KimJBTC](https://x.com/KimJBTC)*
