# Forking and the Longest Chain Rule

Now imagine this situation:

There are two miners in two different countries (we’ll use fictional countries as examples), one in Genovia and another in Kashfarstan. By pure coincidence, both miners discover the “magic number” (Proof of Work) at almost the exact same moment.

Both broadcast to the network:

> “I’m the winner! Here is my version of the transaction ledger!”

This situation is called a **Fork**.

Some computers around the world accept Genovia’s block, while others accept Kashfarstan’s block. Consensus (a single shared agreement) temporarily splits into two versions.

So how does Bitcoin reunify the network?

---

# The Longest Chain Rule

Bitcoin has a golden rule for resolving this conflict:

> “Follow the chain with the most accumulated Proof of Work (energy).”

Here is the simplified process:

---

## 1. Two Candidates

Now there are two versions of the ledger (Block A and Block B), both mathematically valid according to Bitcoin’s rules.

---

## 2. The Race Continues

Other miners around the world will choose one version (usually whichever block they received first) and begin mining the next block on top of it.

---

## 3. A Winner Emerges

Because internet speeds and luck differ, eventually one side will find the next block first.

For example:

- The miners building on top of Block A successfully mine the next block (Block A+1).
- Now the Block A chain becomes longer (two blocks) than the Block B chain (one block).

---

## 4. Consensus Reunifies

Once the computers following Block B see that another chain has become longer (Block A + A+1), they automatically abandon Block B and switch to the longer chain.

Consensus becomes unified again.

---

# Simple Analogy

Imagine two competing rumors spreading at the same time.

You are unsure which one is true.

But then, the first rumor gains stronger evidence:
photos, witnesses, and a much more complete timeline.

Naturally, you would abandon the weaker rumor and follow the version backed by stronger proof.

That is essentially how the longest chain rule works.

---

# What Happens to Transactions in the “Discarded Chain”?

The discarded block is called an **Orphan Block**.

The transactions inside it are not destroyed, but they are treated as if they never happened on the main chain.

Those transactions return to the waiting area called the **Mempool**, where they can be included again in future blocks.

---

# Why Are 6 Confirmations Recommended?

This is why Bitcoin users are often advised to wait for **6 confirmations** (6 new blocks after their transaction).

Why?

Because after 6 additional blocks, it becomes extremely unlikely that another competing chain could grow long enough to overtake the current chain.

The deeper a transaction is buried under Proof of Work, the more secure it becomes.

---

# Why Is This Important for Consensus?

The longest chain rule ensures two critical things:

## 1. There Is Only One Truth

Even if temporary disagreements occur, the network will always converge back into a single shared ledger.

---

## 2. Majority Power Determines Consensus

The longest chain represents where the majority of the world’s computational energy (Hash Power) is being directed.

In Bitcoin, consensus is not decided by voting, politics, or authority.

It is decided by accumulated Proof of Work.
