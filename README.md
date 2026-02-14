Prediksi nasabah yang mungkin akan membeli deposito
Background : Dalam industri perbankan, memahami perilaku, nasabah sangat krusial untuk meningkatkan efektivitas kampanye pemasaran. Salah satu tantangan terbesar adalah mengetahui siapa saja yang berpotensi merespons positif terhadap penawaran produk keuangan tertentu, seperti deposito berjangka.

Dengan memanfaatkan data historis yang mencakup informasi demografis nasabah, riwayat transaksi, serta hasil kampanye sebelumnya, peserta

🛠 Tujuan:
Membuat model machine learning yang dapat mengklasifikasikan nasabah ke dalam dua kategori:

● 1: nasabah diprediksi akan membeli deposito berjangka

● 0: nasabah diprediksi tidak akan membeli

Nama Kolom : Deskripsi Kolom

1. customer_number : Angka unik yang diberikan kepada setiap nasabah untuk membedakan satu nasabah dengan yang lainnya

2. usia : Usia nasabah (dalam tahun)

3. pekerjaan : Jenis pekerjaan nasabah

4. status_perkawinan : Status perkawinan nasabah (termasuk duda/janda sebagai "cerai")

5. pendidikan : Tingkat pendidikan terakhir yang diselesaikan oleh nasabah

6. gagal_bayar_sebelumnya : Apakah nasabah pernah mengalami gagal bayar kredit sebelumnya

7. pinjaman_rumah : Apakah nasabah memiliki pinjaman rumah

8. pinjaman_pribadi : Apakah nasabah memiliki pinjaman pribadi

9. jenis_kontak : Jenis media komunikasi yang digunakan untuk menghubungi nasabah

10. bulan_kontak_terakhir : Bulan ketika nasabah terakhir kali dihubungi

11. hari_kontak_terakhir : Hari dalam seminggu ketika nasabah terakhir kali dihubungi

12. durasi_kontak : Durasi kontak terakhir dalam satuan detik (tidak digunakan dalam model prediksi nyata karena hanya diketahui setelah kontak dilakukan)

13. jumlah_kontak_kampanye_ini : Jumlah total kontak yang dilakukan selama kampanye saat ini

14. hari_sejak_kontak_sebelumnya : Jumlah hari sejak nasabah terakhir dihubungi dari kampanye sebelumnya (999 berarti belum pernah dihubungi sebelumnya)

15. jumlah_kontak_sebelumnya : Jumlah kontak yang dilakukan sebelum kampanye saat ini terhadap nasabah

16. hasil_kampanye_sebelumnya : Hasil dari kampanye pemasaran sebelumnya terhadap nasabah

17. tingkat_variasi_pekerjaan : Indikator variasi tingkat pekerjaan secara kuartalan

18. indeks_harga_konsumen : Indeks harga konsumen pada bulan terkait

19. indeks_kepercayaan_konsumen : Indeks tingkat kepercayaan konsumen pada bulan terkait

20. suku_bunga_euribor_3bln : Suku bunga Euribor untuk tenor 3 bulan

21. jumlah_pekerja : Jumlah total tenaga kerja dalam indikator kuartalan

22. berlangganan_deposito : Apakah nasabah memutuskan untuk berlangganan produk deposito berjangka (1 berarti berlangganan deposito dan 0 berarti customer tidak berlangganan deposito)
