# The Byzantine Generals Problem, and How Bitcoin Consensus Becomes the Solution


In the world of distributed computing (such as the Bitcoin network which consists of thousands of unknown computers), there is a classic problem that is greatly feared, called the **Byzantine Generals Problem**.

The Byzantine generals analogy roughly goes like this:

Imagine several generals surrounding a powerful enemy city.

The condition: The armies are spread around different sides of the city. They can only win if all generals attack at the same time. If some attack while others retreat, the attacking army will be destroyed.

The problem: They can only communicate through couriers who carry messages (similar to data on the internet).

The risks:
1. Couriers could be captured by the enemy or their messages altered.
2. There may be traitor generals among them. A traitor general could send the message "Attack!" to General A, but send "Retreat!" to General B.

The result? General A attacks alone and is completely defeated. Consensus fails because false information has been spread by a traitor.

--

**Its Relation to Bitcoin**

Inside the Bitcoin network, every computer (node) is a "General".

The message is: "Andi sends 1 BTC to Budi."

The traitor is: A hacker or someone attempting to perform double spending (using the same money twice).

How can thousands of computers that do not know each other be sure that the message they receive is honest and agreed upon by the other generals?

The Brilliant Solution of Bitcoin: Proof of Work (PoW)

Satoshi Nakamoto (the creator of Bitcoin) solved the generals problem not by "trusting each other", but by making dishonesty extremely expensive.

In the generals analogy, PoW is like requiring a courier to complete a very difficult and time-consuming task (for example solving a complex puzzle) before they are allowed to deliver the message.

If a traitor general wants to send different false messages to many generals, they must spend enormous energy and effort (almost impossible to do alone). Of course, each general has their own courier. And every time they want to deliver a message, they must spend significant effort. Imagine if 99 generals receive the same message while 1 receives a different one. The lone general then has two choices: follow the agreement that already exists, or attempt to go their own way.

Most importantly, other generals can easily verify whether the courier's "work" is valid or not.

--

**Why the Banking System Instead Adopts a Model Similar to the Byzantine Generals Problem**

Unlike Bitcoin which attempts to solve the Byzantine problem, the modern banking system instead accepts and manages the problem in a different way, through centralization and institutional trust.

In the banking system, the "generals" are not truly independent like in the Bitcoin network. They exist within a clear structure: commercial banks, central banks, clearing institutions, regulators, and national legal systems.

This means that if a transaction message appears such as:

"Andi sends money to Budi"

the validity of that message is not determined by the consensus of thousands of independent computers, but by a trusted central authority.

There are several mechanisms that make this system function:

- Central authority (bank or clearing institution)  
The bank acts as the source of truth. If there is a data conflict, the bank's records are considered correct.

- Known identities (KYC)  
All participants in the banking system have verified identities. This reduces the possibility of anonymous traitors.

- Audits and regulation  
Banks are supervised by regulators and auditors. If data manipulation occurs, there are legal consequences.

- Transaction reversal systems  
If errors or fraud occur, transactions can be reversed through administrative or legal processes.

In other words, the banking system does not attempt to build a system that is mathematically resistant to traitors, as Bitcoin does.

Instead, it builds a system that depends on trust in institutions, law, and central authority to resolve conflicts.

This approach is far more efficient in terms of energy and transaction speed, but it comes with one major consequence:

If the central authority fails, is compromised, or becomes corrupt, the entire system can be affected, because everyone depends on the same source of truth.

Bitcoin attempts a different path: not by trusting institutions, but by building a system where even if some participants behave maliciously, the network can still reach the correct consensus.
