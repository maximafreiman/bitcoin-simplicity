Bitcoin Whitepaper (Simplification)
---
![202211011450-main cropped_1667290056](https://github.com/user-attachments/assets/c705bc11-ff0a-4ff2-b2fc-0272b9561462)

Have you ever heard the term *whitepaper*? In short, it is an official document, similar to a research journal, that discusses an issue, a proposed solution, a project, a technical guide, and so on.  

In the context of Bitcoin, the Bitcoin Whitepaper contains the issues raised about a new solution to improve the financial system, in which it also explains in detail how Bitcoin works and the purpose for which Bitcoin was created.

Written under the pseudonym **Satoshi Nakamoto** on **October 31, 2008**, a new idea was born about how a peer-to-peer digital cash system could work without a third party such as banks. Drawing on developments in cryptography and computing since 1974, Satoshi explains how all disciplines of cryptography and computer science can be implemented in digital cash.


The contents of this Whitepaper consist of 13 sections.

- Abstract  
- Introduction  
- Transactions  
- Timestamp Server  
- Proof of Work  
- Network  
- Incentive  
- Storage Space  
- Simplified Payment Verification  
- Combining and Splitting Value  
- Privacy  
- Calculations  
- Conclusion  

Everything in the Whitepaper is explained in technical language, although some parts are simplified. But don’t worry! Each point will be explained in a simple way. So we don’t need to feel insecure or afraid when we see the formulas and diagrams in the whitepaper that may seem intimidating to beginners.

--

**1. Abstract**

Here, it is explained in the form of a one-page summary that outlines the big idea and the main workings of Bitcoin at a high level. It explains that Bitcoin is a digital money system that allows people to send payments directly without banks or intermediaries, with security maintained by a global network of computers. Transactions are secured with cryptographic signatures and recorded on the blockchain through proof-of-work, making the records difficult to alter. The longest chain is considered the truth because it represents the greatest amount of computational power and keeps the network secure from fraud such as double spending.

--

**2. Introduction**

Currently, online payments still rely on financial institutions as trusted intermediaries, but this system is expensive, slow, and vulnerable to fraud because transactions can be reversed and must be mediated. As a result, small transactions become inefficient, and merchants have to collect large amounts of customer data to reduce risk.

Bitcoin offers a solution by replacing trust in third parties with cryptographic proof, allowing two people to transact directly and securely. With a peer-to-peer network and a proof-of-work–based timestamping system, transactions are recorded in sequence and are nearly impossible to alter, and the system remains secure as long as the majority of the computing power is controlled by honest nodes.

--

**3. Transaction**

This is an explanation of the Bitcoin transfer mechanism and how these transfer activities are verified. We use the analogy of coins to make it simpler. So, every time someone sends a coin, they “sign” proof that the coin now belongs to the next person. The receiver can check this signature to make sure the coin truly came from the previous owner.

The problem is: Someone could try to send the same coin to two different people at almost the same time.

Normally, in a banking system, there is a central office that checks all transactions and decides which one is valid. But in that case, everyone has to trust that office. Bitcoin chooses a different approach: All transactions are announced to the entire network of computers around the world.

These computers work together to agree on which transaction arrived first. The transaction that is accepted first by the majority of computers is considered valid, and the one that arrives later is automatically rejected.

So in essence, Bitcoin does not prevent people from trying to cheat, but it makes a global network collectively determine which transaction is the correct one, without the need for a bank or a central authority.

<img width="388" height="224" alt="image" src="https://github.com/user-attachments/assets/95d78032-d62f-47b2-ac22-a9d44cdb3992" />

--

**4. Timestamp Server**

Imagine there is a digital time bulletin board.

Every few minutes, the system gathers new transactions and then creates a digital fingerprint (a hash) of that collection. This fingerprint is announced to the entire network, so everyone can see: “At this time, this data truly already existed.”

Each new timestamp record also includes the fingerprint of the previous record, forming a chain that is linked together.  
If someone tries to change an old record, its fingerprint will change and everyone can immediately notice.

The timestamp server is how Bitcoin gives transactions a time stamp and locks them into a chain that cannot be altered without being detected.

--

**5. Proof of Work**

Now imagine the Bitcoin network as a puzzle-solving race.

Every computer on the network competes to find a random number that, when combined with transaction data and “scrambled” (hashed), produces a result that meets certain rules—for example, the hash must start with many zeros. Finding this number is difficult and requires electricity and time, but checking it is very easy. Once a computer finds it, it earns the right to announce a new “block” to the network.

This block is also locked to the previous block. If someone wants to change an old block, they would have to redo the puzzle not just for that one block, but for all the blocks after it. And that is almost impossible if the honest network keeps moving faster.

About “who decides the truth”:
Bitcoin does not use a “one person, one vote” or “one computer, one vote” system.  
Instead, it uses “one unit of work, one vote.”

The chain of blocks that has the most work behind it (the most puzzles solved) is considered the correct record by everyone.

To keep the system stable, the network adjusts the difficulty of the puzzles.  
If computers get faster and blocks start appearing too often, the puzzles are made harder.  
If there are fewer computers and blocks take too long, the puzzles are made easier.

Proof of Work secures Bitcoin by making honesty the cheapest option and cheating extremely expensive.

<img width="367" height="92" alt="image" src="https://github.com/user-attachments/assets/9b616ce4-1cd1-43e1-9b91-9870e2373337" />

--

**6. Network**

The Bitcoin network is like many computers working together as one big team.

- Every time there is a new transaction, it is broadcast to all the computers on the network.  
- Each computer collects new transactions and groups them into a package called a block.  
- All computers then compete to solve a mathematical puzzle to secure their block.  
- The computer that succeeds first announces its block to the network.  
- Other computers verify the block. If all the transactions inside it are valid and have not been used before, the block is accepted.  
- Once accepted, all computers build the next block on top of it, forming a chain.

Sometimes two computers can find a block at almost the same time. Part of the network will see version A first, while another part will see version B first.

In this situation, all computers temporarily follow the version they received first. As soon as the next new block is found, the chain that becomes longer is considered the correct one, and all computers switch to that chain.

A transaction does not have to reach every computer to enter the system. As long as it reaches many computers, it will soon be included in a block. If a computer misses a block, it can request it again when it sees the next block and realizes that something was missed.

--

**7. Insentive**

In every block, there is one special transaction at the very beginning. This is the “reward” transaction for the block creator. This transaction creates new coins and immediately gives them to the computer that successfully created the block.

This is a reward to encourage people to run their computers to keep the network operating, because there is no bank or central office that distributes coins.

This process is similar to mining gold. Instead of digging the ground, it uses computer time and electricity to “produce” new coins.

In addition to new coins, the block-creating computer or machine can also receive transaction fees. If someone sends 1 Bitcoin but only 0.99 Bitcoin reaches the receiver, then the remaining 0.01 Bitcoin becomes a fee for the block creator.

Later, when the number of new coins reaches the predetermined limit (21 million), the new-coin reward will stop. After that, block creators will be paid only from transaction fees, not from newly created coins.

This reward system also encourages honesty. If someone has very powerful computers, they could try to cheat, but in the long run they will profit more by following the rules, because they can continue to earn rewards and transaction fees without damaging the system that gives value to the coins they own.

--

**8. Storage Space**

From the beginning, Bitcoin was designed so that old data does not have to be stored forever. After a transaction is buried deep enough under many blocks above it, the details of that transaction can be “summarized” to save storage space.

The method is that all transactions in a block are combined into a single “digital fingerprint” through a structure called a Merkle Tree (a way of combining many pieces of data into one main hash that represents them all). What is stored in the block is only this final summary in the form of a hash code, not the full contents of every transaction.

Because of this, computers that help maintain the network only need to store the block headers, which are very small—about 80 bytes per block—amounting to only a few megabytes per year.

Satoshi then connects this to Moore’s Law (the observation that computer capabilities tend to roughly double every two years, making storage and computing power cheaper and larger over time). This means that as technology advances, storing and verifying Bitcoin should not become a heavy burden for ordinary users.

--

**9. Simplified Payment Verification**

A person can check whether a Bitcoin payment has been received without having to run a computer that stores and verifies the entire network. The way to do this is by storing the block headers from the longest chain (a compact list of all blocks), and then requesting a small proof from the network in the form of a Merkle branch (a short piece of data that links a specific transaction to a specific block) to confirm that the transaction has indeed been included in the blockchain.

This allows them to see that the transaction is truly part of the blockchain and that new blocks continue to be added afterward, which means the network has accepted the payment.

However, this method depends on the honesty of the majority of the network.  
If the network is controlled by an attacker, this simplified method can be fooled.

Therefore, for higher security—especially for businesses that frequently receive payments—running your own node remains the best option, because it can verify all transactions directly and detect abnormal behavior more quickly.

--

**10. Combining and Splitting Transaction Value**

Rather than treating every “small coin” separately, Bitcoin combines and splits value within a single transaction.  
A transaction usually has multiple inputs (funds coming from one or more previous transactions) and two outputs:  
one for the payment recipient, and another for change back to the sender if there is any remainder.

Even though a transaction can depend on many previous transactions, this is not a problem, because the network does not need to track the entire history one by one. It only needs to ensure that all the value being spent truly comes from valid transactions recorded on the blockchain.

--

**11. Privacy**

Traditional banking protects privacy by limiting who can see transaction data.  
Bitcoin is different, because all transactions are publicly visible. However, privacy is preserved in another way: people’s identities are not shown, only their digital addresses (public keys) are visible.

So, anyone can see that one address sends money to another address, but they cannot see who the person behind the address is.  
This is similar to a stock exchange, where people can see the time and size of trades, but not the identities of the traders.

For additional protection, users are encouraged to use a new address for each transaction, making it harder to link many transactions to the same person. However, in some cases—such as when a single transaction uses multiple sources of funds—it can still be inferred that they likely belong to the same owner.

This means that privacy in Bitcoin is not about erasing traces, but about keeping distance between transactions and the human identities behind them.

--

**12. Calculations of Security Levels**

This section explains how difficult it is for an attacker to “catch up” and alter a transaction that has already been added to the blockchain.

Imagine two race tracks:

- Honest track = the normal network that keeps adding blocks  
- Attacker’s track = an attacker secretly trying to build their own version of the chain

Every time the honest network adds a new block, the attacker falls further behind.  
The attacker can only succeed if they get lucky and have enough power to catch up and overtake the honest network.

The key idea:

The more blocks that are added after your transaction, the smaller the chance that an attacker can reverse it.  
The probability does not decrease slowly—it drops very fast, like the odds of winning a lottery shrinking with every minute you wait.

That is why Bitcoin has the concept of “confirmations”:

- 1 confirmation = the transaction is included in one block  
- 6 confirmations = the transaction is, in practical terms, very strongly locked in

Regarding new keys and parallel transactions, the simple meaning is this:  
The recipient of a payment makes the transaction unpredictable in advance to the sender, so an attacker cannot prepare a fake chain far ahead of time.

The big conclusion:

Bitcoin does not rely on being “impossible to attack,”  
but on the fact that the cost, effort, and luck required to attack become unreasonable after a few blocks have passed.

--

**13. Conclusion**

Bitcoin is a digital money system that does not rely on trust in any individual or institution.  
Ownership is secured by digital signatures, and fraud such as double spending is prevented by a network of connected computers that record transactions through proof-of-work.

This network has no center and requires no identities. Computers can come and go at any time, and then accept the longest chain as the valid shared history.

Each computer “chooses” not by voting, but by computing power:  
they support correct blocks by extending them, and reject incorrect blocks by ignoring them.

In essence:  
Bitcoin’s security and trust emerge from collective agreement and mathematics, not from authority or human promises.

---

And that is the simplified version of all the explanations contained in the Bitcoin Whitepaper. All of the mathematical and technical aspects have been explained in a simple way.

To view the original Bitcoin Whitepaper written by Satoshi Nakamoto, you can see it here:
  
https://bitcoin.org/bitcoin.pdf
