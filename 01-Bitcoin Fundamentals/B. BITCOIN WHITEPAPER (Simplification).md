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


--

**5. Proof of Work**

Sekarang bayangkan jaringan Bitcoin itu seperti lomba memecahkan teka-teki.

Setiap komputer di jaringan berlomba mencari angka acak yang, ketika digabung dengan data transaksi lalu “diacak” (di-hash), hasilnya memenuhi aturan tertentu, misalnya hasilnya (hash) harus diawali dengan banyak nol. Mencari angka ini susah dan butuh listrik serta waktu, tapi mengeceknya sangat mudah. Kalau sudah ketemu, komputer itu berhak mengumumkan “blok” baru ke jaringan.

Blok ini juga terkunci ke blok sebelumnya. Kalau seseorang mau mengubah satu blok lama, dia harus mengulang teka-teki itu bukan cuma untuk satu blok, tapi untuk semua blok setelahnya. Dan itu hampir mustahil kalau jaringan jujur lebih cepat.

Soal “siapa yang menentukan kebenaran”:
Bitcoin tidak pakai sistem “satu orang satu suara” atau “satu komputer satu suara”.
Yang dipakai adalah siapa yang sudah mengeluarkan usaha paling besar.

Rantai blok yang punya pekerjaan terbanyak (paling banyak teka-teki yang sudah dipecahkan) dianggap sebagai catatan yang benar oleh semua orang.

Dan supaya sistem tetap stabil, jaringan menyesuaikan tingkat kesulitan teka-teki.
Kalau komputer makin cepat dan blok jadi terlalu sering muncul, teka-tekinya dibuat lebih susah.
Kalau komputer sedikit dan blok terlalu lama, teka-tekinya dibuat lebih mudah.

Proof of Work membuat Bitcoin aman dengan mengubah kejujuran menjadi hal yang paling “murah”, dan kecurangan menjadi hal yang sangat “mahal”.

<img width="354" height="87" alt="image" src="https://github.com/user-attachments/assets/115360fd-0190-49d3-b458-eebce28b7b7d" />

--

**6. Jaringan**

Jaringan Bitcoin seperti banyak komputer yang bekerja sebagai satu tim besar.

- Setiap kali ada transaksi baru, transaksi itu dikirim ke semua komputer di jaringan.
- Setiap komputer mengumpulkan transaksi-transaksi baru dan menyusunnya menjadi satu paket yang disebut blok.
- Semua komputer lalu berlomba memecahkan teka-teki matematika untuk mengamankan blok mereka.
- Komputer yang berhasil pertama mengumumkan bloknya ke jaringan.
- Komputer lain akan memeriksa blok itu. Jika semua transaksi di dalamnya valid dan belum pernah dipakai sebelumnya, blok tersebut diterima.
- Setelah diterima, semua komputer membangun blok berikutnya di atas blok itu, sehingga terbentuk satu rantai.

Kadang dua komputer bisa menemukan blok hampir bersamaan. Sebagian jaringan akan melihat versi A dulu, sebagian melihat versi B dulu.

Dalam kondisi ini, semua komputer sementara mengikuti versi yang pertama mereka terima. Begitu ada blok baru berikutnya, rantai yang menjadi lebih panjang dianggap benar, dan semua komputer akan berpindah ke rantai itu.

Transaksi tidak harus sampai ke semua komputer agar bisa masuk ke sistem. Selama sampai ke banyak komputer, transaksi itu akan segera masuk ke dalam sebuah blok. Kalau ada komputer yang ketinggalan satu blok, dia bisa meminta ulang saat melihat blok berikutnya dan sadar ada bagian yang terlewat.

--

**7. Insentif**

Di setiap blok, ada satu transaksi khusus di bagian paling awal. Yaitu transaksi "hadiah" kepada pembuat blok. Transaksi ini menciptakan koin baru dan langsung memberikannya kepada komputer yang berhasil membuat blok tersebut.

Ini adalah hadiah supaya orang mau menjalankan komputer mereka untuk menjaga jaringan tetap berjalan, karena tidak ada bank atau kantor pusat yang membagikan koin.

Proses ini mirip seperti menambang emas. Bukan menggali tanah, tapi menghabiskan waktu dan listrik komputer untuk “menghasilkan” koin baru.

Selain dari koin baru, komputer atau mesin pembuat blok juga bisa mendapat biaya transaksi. Kalau seseorang mengirim 1 Bitcoin tapi hanya 0,99 Bitcoin yang sampai ke penerima, maka 0,01 Bitcoin sisanya jadi biaya untuk pembuat blok.

Nanti, ketika jumlah koin baru sudah mencapai batas yang ditentukan (21 juta), hadiah koin baru akan berhenti. Setelah itu, pembuat blok hanya dibayar dari biaya transaksi, bukan dari koin baru lagi.

Sistem hadiah ini juga mendorong kejujuran. Kalau seseorang punya komputer sangat kuat, dia bisa mencoba curang, tapi dalam jangka panjang dia akan dapat lebih banyak untung dengan mengikuti aturan, karena dia bisa terus mendapat hadiah dan biaya transaksi, tanpa merusak sistem yang memberi nilai pada koin yang dia miliki.

--

**8. Ruang Penyimpanan**

Bitcoin sejak awal dirancang supaya data lama tidak harus disimpan semuanya selamanya.
Setelah sebuah transaksi terkubur cukup dalam oleh banyak blok di atasnya, detail transaksi itu bisa “diringkas” untuk menghemat ruang penyimpanan.

Caranya, semua transaksi di dalam satu blok dirangkum menjadi satu “sidik jari digital” lewat struktur yang disebut Merkle Tree (cara menggabungkan banyak data menjadi satu hash utama yang mewakili semuanya). Yang disimpan di blok hanya hasil kesimpulan akhirnya saja dalam berbentuk kode hash, bukan semua isi transaksi.

Karena itu, komputer yang ikut menjaga jaringan cukup menyimpan kepala blok yang sangat kecil, sekitar 80 byte per blok, yang dalam setahun hanya memakan beberapa megabyte.

Satoshi lalu mengaitkan ini dengan Moore’s Law (pengamatan bahwa kemampuan komputer cenderung berlipat kira-kira setiap dua tahun, sehingga penyimpanan dan daya komputasi makin murah dan besar dari waktu ke waktu). Artinya, seiring teknologi berkembang, menyimpan dan memverifikasi Bitcoin seharusnya tidak menjadi beban berat bagi orang biasa.

--

**9. Verifikasi Pembayaran yang Sederhana**

Seseorang bisa mengecek apakah pembayaran Bitcoin sudah diterima tanpa harus menjalankan komputer yang menyimpan dan memeriksa seluruh jaringan. Caranya, dia menyimpan kepala blok dari rantai terpanjang (daftar ringkas dari semua blok), lalu meminta bukti kecil dari jaringan berupa cabang Merkle (data singkat yang menghubungkan transaksi tertentu ke satu blok tertentu) untuk memastikan transaksi itu benar-benar sudah masuk ke dalam blockchain.

Dengan begitu, dia bisa melihat bahwa transaksi tersebut benar-benar sudah masuk ke dalam blockchain dan bahwa blok-blok baru terus ditambahkan setelahnya, yang berarti jaringan menerima pembayaran itu.

Namun, cara ini bergantung pada kejujuran mayoritas jaringan.
Jika jaringan dikuasai oleh penyerang, metode sederhana ini bisa dikelabui.

Karena itu, untuk keamanan lebih tinggi, terutama bagi bisnis yang sering menerima pembayaran, menjalankan node sendiri tetap menjadi pilihan terbaik, karena bisa memeriksa semua transaksi secara langsung dan lebih cepat mendeteksi hal yang tidak wajar.

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
