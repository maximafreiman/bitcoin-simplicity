# Introduction to Blocks and the Timechain in Bitcoin

Now we move to the most important part of this fundamental discussion: how the basic system of Bitcoin works. Bitcoin operates on the foundation of a timechain. Yes, I know, some of you might ask, “Isn’t it called blockchain? Why is this different from the mainstream discussion?” Let me clarify.

What distinguishes the concept of a timechain from a blockchain?

1. A timechain is historical and cannot be rolled back. A blockchain can be, depending on the developers.
2. A timechain operates with strict regularity. A blockchain’s distribution can be accelerated or slowed.
3. A timechain has no central administrator. A blockchain does, even if it appears decentralized.

Understood? Okay, let’s continue.

---

Before getting into the core explanation, let me begin with one sentence:

**“If you want to imagine what a Bitcoin block looks like, think of it as a vault containing transaction data ‘documents.’ This vault has its own identity label in the form of a code, where both the label and the contents cannot be manipulated because everything is generated automatically through machine consensus.”**

Since this “vault” (a Bitcoin block) contains transaction data, we begin with transactions.

Think of transaction data as a document containing the details of a Bitcoin transfer. There are two types of transactions here: Coinbase Transactions and Normal Transactions.

---

## A. Coinbase Transaction

Simply put, this is the miner’s transaction. When a miner successfully creates a block, they receive the block reward plus all transaction fees from that block. This is recorded in a “transaction document.”

A coinbase transaction records the miner’s reward within a block: the block subsidy plus the total fees from all transactions included in that block.

In short:

**Miner reward = block reward + total transaction fees in the block (approximately every 10 minutes on average).**

The question is, how does the miner receive fees from each transaction? To answer that, we need to understand how Bitcoin transactions work.

---

## B. Normal Transaction

Imagine someone named Mrs. Yayuk. She wants to buy chili peppers worth 4 BTC from Mrs. Erni. Mrs. Yayuk has 10 BTC.

According to Bitcoin consensus rules, she cannot simply send exactly 4 BTC in isolation. Instead, she must spend her entire 10 BTC output. After sending 10 BTC, the system automatically returns change to her.

Here is what happens:

- 10 BTC is spent from Mrs. Yayuk’s wallet.
- Mrs. Erni receives 3.99 BTC.
- Mrs. Yayuk receives 5.99 BTC as change.
- 0.01 BTC goes to the miner as a transaction fee.

Why does Mrs. Erni receive 3.99 BTC instead of 4 BTC exactly? Because 0.01 BTC is paid as a fee to the miner for including and confirming the transaction.

Visually, this works more like digital cash. You spend a full “coin,” and any remainder is returned as change.

---

Each transaction, like the one between Mrs. Yayuk and Mrs. Erni, is recorded as detailed data containing:

- Sender information  
- Transaction details  
- Recipient information  

And this does not happen just once. Every block contains:

- 1 coinbase transaction  
- Many normal transactions  

---

## TXID: Compressing Transaction Data

There is one issue. If transaction data is recorded in full detail, verification would be inefficient and vulnerable to manipulation due to the sheer volume of data.

To improve efficiency, each transaction is summarized into a unique cryptographic identifier called a TXID (Transaction ID).

If even a tiny detail in the transaction changes, the entire TXID changes. This property makes Bitcoin transactions effectively immutable and extremely difficult to manipulate.

---

## From TXIDs to Blocks

Now all transactions, both coinbase and normal, are collected and each summarized as a TXID.

These TXIDs are then placed into the “vault” called a **Block**.

The block has a “label” called the **Block Header**.

The Block Header contains important metadata about the block. However, even the header itself is still quite detailed. Through the SHA-256 cryptographic hashing function, the block header is compressed into a single 64-character hexadecimal string known as the **Block Hash**.

---

## Block Anatomy Summary

In summary, a Bitcoin block consists of:

- **Block Header**: The identification tag containing metadata about the block. The header is hashed into a single Block Hash.
- **Block Body**: The vault containing a collection of TXIDs.
  - Each TXID represents a transaction.
  - There are two types of TXIDs:
    - One coinbase transaction per block
    - Multiple normal transactions

---

That completes the overview.

Feel free to ask questions or discuss further.

*Nodus meus lex mea.*
