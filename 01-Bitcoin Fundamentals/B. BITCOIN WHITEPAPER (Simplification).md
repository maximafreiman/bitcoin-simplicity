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

**10. Menggabungkan dan Memisahkan Nilai Transaksi**

Daripada memperlakukan setiap “koin kecil” secara terpisah, Bitcoin menggabungkan dan memecah nilai dalam satu transaksi.
Sebuah transaksi biasanya punya beberapa masukan (uang dari satu atau beberapa transaksi sebelumnya) dan dua keluaran:
satu untuk penerima pembayaran, dan satu lagi untuk kembalian kembali ke pengirim jika ada sisa.

Walaupun sebuah transaksi bisa bergantung pada banyak transaksi sebelumnya, itu tidak jadi masalah, karena jaringan tidak perlu melacak seluruh sejarah satu per satu. Cukup memastikan bahwa semua nilai yang dipakai memang berasal dari transaksi yang sah di blockchain.

--

**11. Privasi**

Perbankan tradisional menjaga privasi dengan membatasi siapa saja yang bisa melihat data transaksi.
Bitcoin berbeda, karena semua transaksi bisa dilihat publik. Tapi privasi tetap dijaga dengan cara lain: identitas orangnya tidak ditampilkan, yang terlihat hanya alamat digitalnya (public key).

Jadi, orang bisa melihat bahwa sebuah alamat mengirim uang ke alamat lain, tapi tidak tahu siapa orang di balik alamat itu.
Ini mirip seperti bursa saham, di mana orang bisa melihat waktu dan jumlah transaksi, tapi tidak tahu siapa pelakunya.

Untuk perlindungan tambahan, pengguna disarankan memakai alamat baru setiap kali bertransaksi, supaya sulit menghubungkan banyak transaksi ke satu orang yang sama. Namun, dalam beberapa kasus, seperti saat satu transaksi memakai beberapa sumber dana sekaligus, masih bisa terlihat bahwa semuanya kemungkinan milik orang yang sama.

Artinya, privasi di Bitcoin itu bukan menghilangkan jejak, tapi menjaga jarak antara transaksi dan identitas manusia di baliknya.

--

** 12. Perhitungan Level Keamanan**

Bagian ini menjelaskan seberapa sulit bagi penyerang untuk “mengejar” dan mengubah transaksi yang sudah masuk ke blockchain.

Bayangkan ada dua jalur balapan:

- Jalur jujur = jaringan normal yang terus menambah blok

- Jalur penyerang = penyerang yang diam-diam mencoba membuat rantai versinya sendiri

Setiap kali jaringan jujur menambah satu blok, penyerang semakin tertinggal.
Penyerang hanya bisa berhasil kalau dia beruntung dan cukup kuat untuk menyusul dan melewati jaringan jujur.

Intinya:

Semakin banyak blok yang ditambahkan setelah transaksi kamu, semakin kecil peluang penyerang bisa membalikkan transaksi itu.
Peluangnya tidak turun pelan-pelan, tapi jatuh sangat cepat — seperti peluang menang lotre yang makin kecil setiap menit kamu menunggu.

Karena itu, Bitcoin punya konsep “konfirmasi”:

- 1 konfirmasi = transaksi sudah masuk ke satu blok

- 6 konfirmasi = transaksi sudah “terkunci” sangat kuat secara praktis

Soal kunci baru dan transaksi paralel, maknanya sederhana:
Penerima pembayaran membuat transaksi tidak bisa diprediksi lebih dulu oleh pengirim, sehingga penyerang tidak bisa menyiapkan rantai palsu dari jauh-jauh hari.

Kesimpulan besarnya:

Bitcoin tidak bergantung pada “tidak mungkin diserang”,
tapi pada fakta bahwa biaya, usaha, dan keberuntungan yang dibutuhkan untuk menyerang akan menjadi tidak masuk akal setelah beberapa blok berlalu.

--

**13. Kesimpulan**

Bitcoin adalah sistem uang digital yang tidak bergantung pada kepercayaan kepada siapa pun.
Kepemilikan dijaga oleh tanda tangan digital, dan kecurangan seperti memakai uang dua kali dicegah oleh jaringan komputer yang saling terhubung dan mencatat transaksi lewat proof-of-work.

Jaringan ini tidak punya pusat dan tidak butuh identitas. Komputer bisa datang dan pergi kapan saja, lalu menerima rantai terpanjang sebagai sejarah bersama yang sah.

Setiap komputer “memilih” bukan dengan suara, tapi dengan daya komputasi:
mereka mendukung blok yang benar dengan melanjutkannya, dan menolak blok yang salah dengan mengabaikannya.

Intinya:
Keamanan dan kepercayaan Bitcoin lahir dari kesepakatan bersama dan matematika, bukan dari otoritas atau janji manusia.

(Akan segera update untuk lanjutan materi. Stay tune..)
