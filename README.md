"Classification of Pornographic Content Based on Text Mining Using Naive Bayes lgorithm"

Description: 
Proyek ini adalah implementasi algoritma Naive Bayes untuk membuat model yang dapat mengklasifikasikan konten website (Teks). Algoritma Naive Bayes adalah sebuah metode klasifikasi probabilistik yang didasarkan pada teorema probabilitas Bayes dengan asumsi bahwa semua fitur (variabel) yang digunakan untuk klasifikasi adalah independen secara bersyarat. Proyek ini bertujuan untuk menganalisa suatu konten website apakah mengandung unsur pornografi atau tidak yang kemudian mengklasifikasikan teks menjadi dua kategori kelas: Pornografi dan Non-Pornography.

Gambaran Umum:
Alur peneltiaan yang saya lakukan dalam proyek ini adalah dengan menggunakan "Machine Learning Life Cycle" oleh (Gärtler dkk., 2021), sperti pada gambar berikut
![image](https://github.com/awm25/Model-MultinomialNB/assets/128027599/82a42d7b-00c4-4cff-bd30-af6d44e04f52)
  Berdasarkan gambar diatas berikut adalah penjelasan singkat terkait hal yang dilakukan disetiap proses:
  1. Data Collection
     Mengumpulkan data berupa konten website (Teks) yang telah dipublish secara daring dimulai dari tahun 2019-2022, pengumpulan data ini dilakukan dengan teknik       Scraping menggunakan tools Web Scraper. Hasil dari pengumpulan data ini adalah diperolehnya data website sebanyak 49.743 website.    
  3. Data Cleaning
     Melakukan Preprocessing Data dengan menerapkan beberapa teknik cleaning yaitu; Case Folding, Remove Number, Remove Special Character, Remove Punctuation,          Remove White Space dan Multiple White Space, Remove Single Character, Tokenizing, Stopword Removal dan Filtering, Stemming dan Remove Null Values. Hasil dari      tahap ini adalah terjaadi pengurangan jumlah data  menjadi 49.702 data.
  4. Data Labeling
     Tahap ini dilakukan dengan membuat kamus kata, menghitung total kata, menghitung jumlah kata Pornografi dan Non-Pornografi, menghitung persentase Pornografi       dan Non-Pornografi dan memeberikan label pada data. Hasil dari tahap ini adalah 32.405 data Non-Pornografi dan 17.297 data Pornografi.
  6. Feature Engineering
     Tahap ini dalakukan dengan menerapkan teknik Term Frequency-Inverse Document Frequency (TF-IDF) dan Synthetic Minority Over-Sampoling (SMOTE). Hasil dari tahap ini adalah mengubah data teks ke dalam bentuk matriks data
  8. Model Training
  9. Model Evaluation
  10. Operation
