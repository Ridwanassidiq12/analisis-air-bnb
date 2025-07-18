# analisis-air-bnb
1.1 DATA UNDERSTANDING
Data set Variable :
baris : 15.854 
kolom : 16

1.2 CLEANING
Data memiliki missing value di beberapa kolom penting seperti last_review, reviews_per_month, name, dan host_name yang telah berhasil ditangani, dengan mengisi valuenya bedasarkan korelasi yang sudah di uji statistikanya
Nilai 0 di kolom number_of_reviews dan availability_365 diidentifikasi dan diperlakukan dengan tepat dengan mengisi valuenya bedasarkan korelasi yanng sudah di uji statistikanya
Duplikasi data : 0

2.EDA (eksplorasi data)
Distribusi neighbourhood ,number_of_reviews, last_review dan reviews_per_month tidak normal
number_of_reviews dan reviews_per_month memiliki outlier
Korelasi antara neighbourhood dengan number_of_reviews, last_review,reviews_per_month memiliki pengaruh, yagn sudah di uji statistikanya dengan metode uji kruskal

3.REKAYASA DATA
nambahan kolom reviews_per_year agar mudah dimengerti

4.VISUALISASI DATA
neighbourhood : barplot dan maps top 20
neigbourhood dengan review_per_year : barplot dan maps top 20 lalu melihat modus review per yearnya di wilayah top 5
neigbourhood dengan last_review 2022 : barplot dan maps top 20
neigbourhood dengan jumlah_last_review : barplot dan maps top 20
neigbourhood dengan number_of_reviews : barplot dan maps top 20
top 5 neigbourhood : 1.Vadhana, 2.Khlong Toei, 3.Huai Khwang, 4.Ratchathewi, 5.Bang Rak
top 5 neighbourhood dengan reviews_per_year 1.Khlong Toei, 2.Vadhana, 3.Sathon, 4.Ratchathewi, 5.Huai Khwang

- 3.1 top 5 neighbourhood dengan last_review thn 2022 : 1.Khlong Toei, 2.Vadhana, 3.Ratchathewi, 4.Sathon, 5.Bang Rak
- 3.2 top 5 neighbourhood dengan last_review seluruh tahun : 1.Vadhana, 2.Khlong Toei, 3.Huai Khwang, 4.Ratchathewi, 5.Bang Rak
  top 5 neighbourhood dengan last_review seluruh tahun : 1.Khlong Toei, 2.Vadhana, 3.Sathon, 4.Ratchathewi, 5.Bang Rak

5.ANALISIS LANJUTAN
1.Price
Distribusi harga tidak normal dan memiliki outlier, korelasi harga dengan wilayah (neighbourhood) juga memiliki pengaruh yang sudah di uji statistikanya dengan metode kruskal
disini wilayah yang memiliki price tertinggi ;

Vadhana : 1100000
Khlong Toei : 1000000
Huai Khwang : 1000000

price_max
Vadhana : 1100000
Khlong Toei : 1000000

price_median
Vadhana : 2000
Khlong Toei : 1700

price_min
Vadhana : 350
Khlong Toei : 332

2.total pendapatan dan total pendapatan perwilayah
total pendapatan : 51.014.978

wilayah kontributor terbesar

Vadhana : 9.586.939, 18.79%
Khlong Toei : 8.910.845, 17.47%
Huai Khwang : 5.665.595, 11.11%
jadi kita bisa simpulkan vadhana dan kholng toei berkontribusi paling besar terhadap total pendapatan

3.Room type
Distribusi room type tidak normal, korelasi room_type dengan wilayah (neighbourhood) juga memiliki pengaruh yang sudah di uji statistikanya dengan metode chi2_contingency
disini room_type terlaris ada ;

Entire home/apt : 8912
Private room : 5770
Hotel room : 649
Shared room : 523
wilayah dengan room_type terlaris ;

khlong toei, entire home/apt : 1520 , private_room : 489, total : 2009
vadhana, entire home/apt : 1451 , private_room : 544, total : 1995
huai khwang, entire home/apt : 776 , private_room : 301, total : 1077
price dengan room_type price_max dan price_mean ;

price_max
Entire home/apt, max : 1100000
Private room, max : 600700
Hotel room, max : 300000
Shared room, max : 31200
price_mean
Entire home/apt, mean : 3465.47
Private room, mean : 3064.60
Hotel room, mean : 3028.30
Shared room, mean : 919.75

4.Rfm
kebanyakan harga yang sedang - rendah memiliki review yang banyak dan baru direview
harga tinggi memiliki review yang tinggi tetapi sudah sudah sangat lama direview
harga sedang memiliki review sedang score 3-4 dan lumayan baru direview memiliki score 3 - 4
jadi bisa disimpulkan bahwa pelanggan sangat mempertimbangkan harga ketika ingin menyewa

6.Rekomendasi 
Khlong toei ;

room_type & price
Entire home/apt, jmlh_tersewa : 1520, harga : 3962 - 36613
Private room, jmlh_tersewa : 489, harga : 5481 - 27650
Hotel room, jmlh_tersewa : 73, harga : 2665 - 2448
Shared room, jmlh_tersewa : 15, harga : 893 - 804
Vadhana ;

room_type & price
Entire home/apt, jmlh_tersewa : 1451, harga : 4699 - 39426
Private room, jmlh_tersewa : 544, harga : 4251 - 13550
Hotel room, jmlh_tersewa : 105, harga : 3942 - 4692
Shared room, jmlh_tersewa : 53, harga : 793 - 674
lain - lain yang meningkatkan review
kelengkapan interior
layanan yang super cepat
