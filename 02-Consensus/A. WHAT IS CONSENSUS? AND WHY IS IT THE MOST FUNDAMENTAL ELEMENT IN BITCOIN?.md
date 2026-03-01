# What Is Consensus? And Why Is It the Most Fundamental Element in Bitcoin?

In a social context, consensus is a way of making decisions without resorting to voting that creates winners and losers.

The goal is to find a solution that everyone, or at least a large majority, can accept.

For example, community deliberation in a village. There is no single boss with absolute authority, yet everyone agrees to follow one decision for the common good.

In the world of computers, consensus is far more rigid. Computers cannot “discuss” or “feel hesitant.” Here, consensus means agreement among computers (nodes) on a single data value.

Imagine 1,000 computers maintaining the same ledger. If computer A says, “Budi has $100,” while computer B says, “Budi has $50,” the system collapses because there is no unified state of truth.

Therefore, technological consensus must satisfy three core properties:

- **Termination:** Every honest node must eventually decide on a value. It cannot hang forever.
- **Agreement:** All honest nodes must decide on the same value.
- **Validity:** The agreed value must be one that was actually proposed by a node, not something that appeared out of nowhere.

---

## Why Is Consensus So Difficult?

The problem is that in globally distributed computer systems, such as the internet, we face two major challenges:

- **Technical Failures:** Computers may crash unexpectedly or lose internet connectivity.
- **Malicious Failures:** Some participants may intentionally send false data to disrupt the system or steal money.

---

## The Connection to Bitcoin

In traditional banking, we do not need consensus among users because there is a central authority, such as a central bank or a commercial bank. The bank is the single source of truth. Whatever the bank says becomes reality.

Bitcoin removes that central authority. The challenge then becomes: how can thousands of computers that do not know each other, do not trust each other, and are scattered around the world maintain a ledger that is 100 percent identical at every moment?

This is why consensus rules exist.

Without consensus, Bitcoin would be nothing more than a collection of meaningless data.
