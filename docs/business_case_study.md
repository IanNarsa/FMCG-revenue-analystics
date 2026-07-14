# Business Case: FMCG Sales Performance Analytics 2024

## 1. Latar Belakang

Perusahaan FMCG (Fast-Moving Consumer Goods) ini beroperasi di 10 region di Indonesia dengan portofolio 25 SKU lintas 5 kategori produk (Sausage, Cheese, Nugget, Milk, Yoghurt), didistribusikan melalui 3 kanal penjualan (Distributor, Modern Trade, General Trade) dan didukung oleh 20 distributor mitra.

Sepanjang 2024, manajemen menetapkan target revenue tahunan per region, namun belum ada evaluasi terstruktur untuk menjawab:
- Apakah target tersebut realistis dan tercapai?
- Wilayah, kanal, dan produk mana yang menjadi penggerak utama bisnis?
- Apakah jaringan distributor beroperasi secara sehat, atau ada risiko operasional (over-stocking, inefisiensi penyaluran stok)?
- Apakah gap pencapaian target disebabkan oleh masalah distribusi, atau faktor lain?

## 2. Masalah Bisnis (Problem Statement)

Manajemen membutuhkan gambaran objektif dan berbasis data mengenai performa penjualan 2024 untuk:
1. Menentukan apakah target 2025 perlu direvisi.
2. Mengidentifikasi produk/region/kanal prioritas untuk alokasi sumber daya (stok, promosi, tenaga penjual).
3. Mendeteksi risiko operasional di jaringan distributor sebelum berdampak ke biaya penyimpanan atau kehilangan penjualan (stockout).
4. Memisahkan mana temuan yang benar-benar didukung data, dan mana yang sekadar asumsi, sebelum dijadikan dasar keputusan strategis.

## 3. Tujuan Analisis

- Mengukur pencapaian revenue aktual terhadap target, per region dan per bulan.
- Menganalisis kontribusi tiap kanal penjualan terhadap revenue dan profitabilitas.
- Mengidentifikasi SKU inti (Pareto 80/20) yang paling kritis dijaga ketersediaannya.
- Mengevaluasi kesehatan operasional distributor (Sell-Through Rate & Inventory-to-Sales Ratio), baik secara tahunan maupun tren bulanan.
- Menguji apakah kesehatan distributor berkorelasi dengan pencapaian target region, guna memvalidasi (atau membantah) asumsi awal sebelum masuk ke rekomendasi.

## 4. Sumber Data

| Dataset | Isi | Granularitas |
|---|---|---|
| `fmcg_sales_2024.csv` | Transaksi penjualan (revenue, profit, unit, kanal, kategori, produk, region, kota, tipe customer) | Per transaksi, harian |
| `sales_target_2024.csv` | Target revenue & unit per region | Per bulan, per region |
| `distributor_performance_2024.csv` | Stok dikirim (STD), stok terjual (STT), inventori akhir | Per bulan, per distributor |

Ketiga dataset diverifikasi memiliki cakupan region yang identik (10 region), tanpa missing value, sehingga aman digabungkan (join) tanpa risiko kehilangan data.

## 5. Ruang Lingkup & Batasan

**Termasuk dalam analisis:**
- Tren penjualan bulanan, regional, dan kategori produk
- Perbandingan actual vs target per region (tahunan & bulanan)
- Performa dan profitabilitas per kanal penjualan
- Kesehatan distributor (tahunan & tren bulanan)
- Konsentrasi produk (Pareto 80/20) beserta profitabilitasnya
- Uji korelasi lintas dataset (kesehatan distributor vs pencapaian target)

**Tidak termasuk (keterbatasan data):**
- Target hanya tersedia di level region, sehingga tidak bisa dievaluasi di level kota atau kanal
- Tidak ada data harga kompetitor atau aktivitas marketing/promosi, sehingga penyebab fluktuasi MoM tidak bisa dipastikan sepenuhnya dari data ini
- Analisis bersifat deskriptif dan korelasional, bukan kausal — temuan hubungan antar variabel perlu divalidasi lebih lanjut sebelum dijadikan dasar kebijakan besar

## 6. Ringkasan Temuan Utama

- Pencapaian target nasional 2024 berada di **86,17%**, dengan seluruh 10 region berada di rentang sempit **85,2%–86,8%** — mengindikasikan gap kemungkinan besar berasal dari penetapan baseline target, bukan masalah eksekusi lokal.
- Kanal **Distributor** mendominasi revenue (55,4%), namun **profit margin ketiga kanal penjualan praktis setara** (~18,7–18,9%) — perbedaan revenue murni soal volume, bukan efisiensi biaya per kanal.
- **14 dari 25 SKU** menyumbang 80% revenue (Pareto), menjadi prioritas utama untuk ketersediaan stok.
- Seluruh 20 distributor memiliki Sell-Through Rate sehat (>80%), namun ditemukan **pola musiman penumpukan inventori** yang berulang di Januari, Oktober, dan November — bukan insiden tunggal di satu bulan.
- **Tidak ditemukan korelasi kuat** antara kesehatan distributor dan pencapaian target region — memperkuat kesimpulan bahwa gap target lebih terkait faktor permintaan pasar atau penetapan target, bukan masalah rantai distribusi.

Detail lengkap analisis, kode, dan visualisasi tersedia di `Sales_Data_Analytics.ipynb`.

## 7. Dampak Bisnis yang Diharapkan (Expected Business Impact)

| Rekomendasi | Dampak yang diharapkan |
|---|---|
| Evaluasi ulang baseline target regional | Target 2025 lebih realistis, mengurangi tekanan eksekusi yang tidak proporsional ke tim sales lapangan |
| Prioritaskan safety stock untuk 14 SKU Core | Mengurangi risiko kehilangan penjualan (lost sales) akibat stockout pada produk penyumbang revenue terbesar |
| Tinjau jadwal pengiriman stok menjelang Januari & Oktober-November | Mengurangi biaya penyimpanan berlebih (holding cost) akibat pola over-stocking musiman |
| Alihkan strategi diversifikasi kanal ke pertumbuhan volume (bukan argumen margin) | Keputusan ekspansi kanal didasarkan pada data margin aktual, menghindari asumsi keliru |

## 8. Stakeholder Terkait

- **Sales & Regional Management** — evaluasi target dan strategi regional
- **Supply Chain & Distributor Relations** — perencanaan stok dan inventori
- **Product/Category Management** — prioritisasi SKU dan portofolio produk
- **Finance/Management** — validasi asumsi profitabilitas lintas kanal untuk perencanaan 2025
