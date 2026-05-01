# Hard Fork vs Soft Fork  
## Consensus Changes with Different Effects from a Normal Fork

Imagine a community of merchants, each holding an identical **Ledger Book** used to record every transaction in the marketplace.

Everyone must maintain the same records so nobody can falsify the data.

---

# 1. Soft Fork: “Stricter Writing Rules”

Imagine the original rule is:

> “Transactions may be written using any ink color.”

Later, the majority of merchants agree on a stricter rule:

> **New Rule:** “From now on, all transactions MUST be written using **Black Ink** for consistency.”

### Updated Merchants (New Rules)
They only accept records written in black ink.

### Non-Updated Merchants (Old Rules)
They still write using blue ink.

### What Happens?
Because black ink is still fundamentally “ink,” old merchants still recognize the new records as valid.

However, updated merchants will reject records written in blue ink.

### Final Result
No permanent split occurs.

Old merchants are eventually pressured to adopt black ink so their records continue to be accepted by the majority.

> **The ledger remains unified as one single book.**

---

# 2. Hard Fork: “A Complete Format Change”

Imagine the original rule is:

> “All transactions are written in Indonesian.”

Suddenly, a group of merchants wants a radical change that cannot be compromised:

> **New Rule:** “From now on, all transactions will be recorded using **Mandarin Chinese** and a **QR Code system**.”

### Updated Merchants (New Rules)
They can no longer read records written in Indonesian.

### Non-Updated Merchants (Old Rules)
They completely fail to understand the new format because the system has fundamentally changed.

### What Happens?
Because the two groups are no longer compatible, they eventually **split into separate systems.**

### Final Result
The old group continues using the old ledger (Indonesian format), while the new group starts an entirely **New Ledger** (Mandarin + QR format).

This is the moment when one cryptocurrency splits into two separate coins.

---

# Quick Comparison

| Condition | Soft Fork (Ink Rules) | Hard Fork (Language Change) |
| :--- | :--- | :--- |
| **Compatibility** | Still compatible | Completely incompatible |
| **Format Change** | Rules become stricter | System is fundamentally changed |
| **Ledger** | Remains one ledger | Splits into two separate ledgers |
| **Coin** | Still one currency | A new currency is created |

---

# Conclusion

> **A Soft Fork** is like updating an application that still works on older phones.
>
> **A Hard Fork** is like replacing the engine entirely — old machines can no longer use the new parts.

---

# Relation to Real Bitcoin History

Inside the Bitcoin network, both events have happened in reality.

---

## 1. Example of a Soft Fork: SegWit (2017)

This was the “black ink” upgrade.

The Bitcoin community agreed to change how transaction data was packaged so blocks could store data more efficiently without altering the fundamental blockchain structure.

### Result
- Bitcoin remained a single network.
- Transactions became more efficient and cheaper.
- Users who did not update their wallets could still send and receive Bitcoin normally.

---

## 2. Example of a Hard Fork: Bitcoin Cash (BCH) (2017)

This was the “language replacement” event.

Part of the community wanted to dramatically increase the size of the blockchain “pages” (from 1MB to 8MB).

Because the majority disagreed, this group split away from the original chain.

### Result
- A permanent chain split occurred.
- :contentReference[oaicite:0]{index=0} was born as a separate cryptocurrency with its own independent ledger.
- :contentReference[oaicite:1]{index=1} continued on the original chain.

If you owned 1 BTC before the split, you suddenly also owned 1 BCH on the newly created chain.
