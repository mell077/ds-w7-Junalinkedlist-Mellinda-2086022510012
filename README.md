1. Mengapa linked list membutuhkan variabel head?
Head adalah pintu masuk tunggal ke dalam struktur ini. Tanpa variabel head, program tidak akan tahu di mana daftar dimulai, sehingga kita tidak bisa mengakses atau menelusuri seluruh data yang tersimpan di dalam node-node lainnya.
2. Mengapa setiap node harus menyimpan referensi 'next'?
Karena posisi memori setiap node dalam linked list itu acak (tidak berurutan). Referensi next berfungsi sebagai "pengait" atau petunjuk jalan yang menghubungkan satu node ke node berikutnya sehingga mereka bisa membentuk satu kesatuan rantai data.
3. Mengapa penyisipan di awal lebih mudah pada linked list dibanding array?
Pada linked list, kita hanya perlu mengubah satu atau dua arah panah (referensi) saja tanpa memedulikan berapa banyak data yang ada. Sedangkan pada array, kita harus memindahkan atau menggeser setiap elemen yang sudah ada satu per satu ke posisi berikutnya untuk mengosongkan tempat di bagian depan.
4. Dalam insertAtBeginning(), mengapa urutannya harus newNode.next = head baru kemudian head = newNode?
Urutan ini bertujuan untuk menjaga kelangsungan rantai. Kita harus menyambungkan node baru ke daftar yang sudah ada terlebih dahulu agar data lama tidak terputus. Jika kita langsung mengubah head ke node baru, kita akan kehilangan alamat atau akses ke seluruh sisa daftar yang lama (terjadi memory leak).
5. Dalam display(), apa yang terjadi jika kita menulis while (current.next != null)?
Program akan berhenti terlalu cepat, sehingga node terakhir tidak akan ditampilkan. Loop tersebut akan berhenti tepat saat berada di node terakhir karena melihat next-nya sudah bernilai null, padahal isi dari node terakhir itu sendiri belum sempat diproses atau dicetak.
6. Struktur mana yang lebih baik untuk akses acak (random access) yang cepat?
Array jauh lebih baik. Karena elemen array disimpan berdampingan secara fisik di memori, kita bisa langsung melompat ke indeks mana pun secara instan. Di linked list, kita tidak bisa melompat; kita harus berjalan melewati satu per satu node dari depan sampai mencapai posisi yang diinginkan.
7. Struktur mana yang lebih baik jika sering melakukan penyisipan di awal?
Linked list adalah pemenangnya. Prosesnya tetap cepat tidak peduli seberapa panjang datanya. Di sisi lain, array akan semakin lambat dan memakan banyak tenaga seiring bertambahnya jumlah data karena banyaknya elemen yang harus digeser setiap kali ada data baru masuk di depan.
8. Mengapa linked list menggunakan lebih banyak memori daripada array?
Karena adanya beban tambahan atau overhead. Di array, memori murni hanya digunakan untuk menyimpan data. Di linked list, setiap node harus menyiapkan ruang ekstra untuk menyimpan alamat (pointer) guna menunjuk ke node selanjutnya, selain menyimpan data itu sendiri.
