# The Byzantine General Problem, dan Bagaimana Konsensus Bitcoin Menjadi Solusi


Dalam dunia komputer terdistribusi (seperti jaringan Bitcoin yang isinya ribuan komputer asing), ada satu masalah klasik yang sangat ditakuti, namanya **Byzantine Generals Problem** (Masalah Jenderal Bizantium).

Analogi Jenderal Bizantium kurang lebih seperti ini:

Bayangkan ada beberapa pasukan jenderal yang mengepung sebuah kota musuh yang kuat.

Kondisinya: Pasukan ini tersebar di berbagai sisi kota. Mereka hanya bisa menang kalau semua jenderal menyerang bersamaan. Kalau ada yang menyerang dan ada yang mundur, pasukan yang menyerang akan dihancurkan.

Masalahnya: Mereka hanya bisa berkomunikasi lewat kurir yang membawa pesan (seperti data internet).

Risikonya: 
1.  Kurir bisa ditangkap musuh atau pesannya diganti.
2.  Ada jenderal pengkhianat di antara mereka. Jenderal pengkhianat ini bisa mengirim pesan "Serang!" ke Jenderal A, tapi mengirim pesan "Mundur!" ke Jenderal B.

Hasilnya? Jenderal A menyerang sendirian dan kalah total. Konsensus gagal karena ada data palsu yang disebarkan oleh pengkhianat.

--

**Hubungannya dengan Bitcoin**

Di dalam jaringan Bitcoin, setiap komputer (node) adalah "Jenderal".

Pesannya adalah: "Si Andi mengirim 1 BTC ke Budi."

Pengkhianatnya adalah: Hacker atau orang yang ingin melakukan double spending (menggunakan uang yang sama dua kali).

Bagaimana ribuan komputer yang tidak saling kenal ini bisa yakin bahwa pesan yang mereka terima adalah pesan yang jujur dan disepakati oleh semua jenderal lainnya?

Solusi Jenius Bitcoin: Proof of Work (PoW)

Satoshi Nakamoto (pencipta Bitcoin) menyelesaikan masalah jenderal ini bukan dengan "saling percaya", tapi dengan "biaya yang mahal".

Dalam analogi jenderal tadi, PoW ibarat mewajibkan kurir untuk mengerjakan tugas yang sangat sulit dan memakan waktu lama (misalnya menyusun teka-teki rumit) sebelum bisa menyampaikan pesan.

Jika jenderal pengkhianat ingin mengirim pesan palsu yang berbeda-beda ke banyak jenderal, dia harus mengeluarkan energi dan usaha yang sangat besar (hampir mustahil dilakukan sendirian). Tentu saja. Masing-masing jenderal punya kurirnya masing-masing. Dan setiap mereka ingin mengantar pesan harus mengeluarkan effort yang besar. Bayangkan jika 99 jenderal dapat pesan yang sama, yang 1 dapat pesan yang berbeda. Maka pilihan untuk 1 jenderal ini ada 2: ikuti kesepakatan yang sudah ada, atau cari jalurnya sendiri.

Dan yang terpenting juga, jenderal lain bisa dengan mudah memverifikasi apakah "pekerjaan" kurir itu benar atau tidak.
