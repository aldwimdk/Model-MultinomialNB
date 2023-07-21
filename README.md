"Classification of Pornographic Content Based on Text Mining Using Naive Bayes lgorithm"

Description: 
This project is an implementation of the Naive Bayes algorithm to create a model that can classify website content (Text). The Naive Bayes algorithm is a probabilistic classification method based on the Bayes probability theorem with the assumption that all features (variables) used for classification are conditionally independent. This project aims to analyze a website's content whether it contains pornographic elements or not which then classifies the text into two class categories: Pornography and Non-Pornography.

Overview:
The research flow carried out in this project is to use the "Machine Learning Life Cycle" by (Gärtler et al., 2021), as shown in the following image:


![image](https://github.com/awm25/Model-MultinomialNB/assets/128027599/1512d8ea-d7a8-4682-8999-88f256a09402)


  Based on the picture above, here is a brief explanation of what is done in each process:
  1. Data Collection
     Collecting data in the form of website content (Text) that has been published online starting from 2019-2022, this data collection is carried out by           Scraping techniques using Web Scraper tools. The result of this data collection was obtained data as many as 49,743 websites.    
  3. Data Cleaning
     Preprocessing Data by applying several cleaning techniques, namely; Case Folding, Remove Number, Remove Special Character, Remove Punctuation, Remove          White Space and Multiple White Space, Remove Single Character, Tokenizing, Stopword Removal and Filtering, Stemming and Remove Null Values. The result         of this stage caused a reduction in the number of datasets to 49,702.
  4. Data Labeling
     This stage is done by creating a word dictionary, counting total words, counting the number of Pornographic and Non-Pornographic words, calculating the        percentage of Pornography and Non-Pornographic and labeling the dataset. The results of this stage are 32,405 Non-Pornography datasets and 17,297              Pornography datasets.
  6. Feature Engineering
     This stage is done by applying the Term Frequency-Inverse Document Frequency (TF-IDF) and Synthetic Minority Over-Sampoling (SMOTE) techniques. The            result of this stage is to convert text data into a data matrix by applying TF-IDF and applying SMOTE techniques to increase the amount of data in             datasets in a balanced way, especially for datasets used for Training Sets, where before applying SMOTE techniques, Pornography labels were 12,108             datasets and Non-Pornography labels were 22,683 datasets. Then after applying the SMOTE technique, the two class labels became balanced, which was 22,683      for both class labels.
  7. Model Training
     This stage has several processes, namely Model Selection, Grid Search, Model Tuning. The result of this stage is to use Multinomial Naive Bayes as a           model that has the best performance of 93.50%.
  8. Model Evaluation
     This stage is carried out by applying several evaluation matrices, namely Overfitting and Underfitting Model, Null Accuracy, Confusion Matrix and              validating the model using ROC Curve, Cross Validation and conducting model trials by comparing the results of analysis from Indonesian linguists with         the models that have been made. The result of this stage is that the Multinomial Naive Bayes model that has been created has an excellent performance in       classifying texts into Pornography and Non-Pornography categories.
  9. Operation
     This stage is done by creating a simple classification system that can be used to classify website text.

Repository Structure:
The project has the following directory structure:
  1. Aldwi Mandak Final Fix.ipynb : Contains the classification model program.
  2. Sistem Klasifikasi.ipynb     : In the form of a simple program code that can be used to classify website text based on the features and models that have                                      been saved.
  3. model_mnb.pkl                : Contains multinomial Naive Bayes models that have been trained and saved.
  4. tfidf.joblib                 : Contains TF-IDF features that have been extracted and saved.

Enviroment used in this project:
  - Anaconda versi 3.1.0
  - Python versi 3.9.13
  - Jupyter Notebook versi 6.4.12
  - Scikit-Learn versi 1.2.0

Install Library/Package:
  - pip install pandas
  - pip install numpy
  - pip install matplotlib
  - pip install seaborn
  - pip install wordcloud
  - pip install plotly
  - pip install scikit-learn
  - pip install imbalanced-learn
  - pip install nltk
  - pip install sastrawi
  - pip install pandas-profiling

Short Explanation about how to run "Sistem Klasifikasi.ipynb":
  - Make sure you have installed all the required libraries and packages, namely Scikit-Learn and joblib.
  - Download and save the "Sistem Klasifikasi.ipynb", "model_mnb.pkl", and "tfidf.joblib" files in the same directory.
  - Jalankan aplikasi Jupyter Notebook pada Anaconda Navigator
  - On the Jupyter Notebook page, navigate to the directory containing the downloaded file and open the "classification system.ipynb" file.
  - Once the file is open, it executes all the code it contains by pressing the "Run" key or by pressing the "Shift + Enter" keys in each cell.
  - Make sure that the files "model_mnb.pkl" and "tfidf.joblib" are located in the same directory as the "Sistem Klasifikasi.ipynb" file. If the file is not        found, be sure to adjust its path in the code.

Summary:
The Naïve Bayes Multinomial classification model used in this project has a very good performance with an initial accuracy value of 93.38% which is then applied various techniques to improve model performance so that the model experiences an increase in performance to 94.61% and can classify documents precisely and accurately.

*** IMPORTANT NOTICE ***
Based on the results of discussions with my supervisor Mrs. Rahmalia Syahputri, S.Kom., M.Eng. Sc, we decided not to upload the dataset used in this repository because we considered several things as follows:
  - Privacy Policy
  - Copyright
  - Legal Compliance
  - Context and Accuracy
  - Ethics and Fair Use
Given the context of using data obtained through web scraping, it is important to always adhere to the rules and policies of the websites accessed, obtain consent where necessary, and consider ethical and privacy aspects in the use and distribution of such data. Publishing scraped data, it is necessary to have proper permission from the data owner and ensure it does not violate the law or privacy policy.
Therefore if you want to use this dataset for academic or research purposes, please contact me via the following e-maail aldwimandak.1911010070@mail.darmajaya.ac.id

*** -_- ***

References :
1. Program
   
   https://kagle.com/
   
   https://github.com/
   
   https://medium.com/
3. Academic Paper
Albitar, S., Fournier, S., & Espinasse, B. (2014). An effective TF/IDF-based text-to-text semantic similarity measure for text classification. Web         Information Sistem Engineering–WISE 2014: 15th International Conference, Thessaloniki, Greece, October 12-14, 2014, Proceedings, Part I 15, 105–114.
Ashari, H., Arifianto, D., & Faruq, H. A. A. (2020). PERBANDINGAN KINERJA ALGORITMA MULTINOMIAL NAÏVE BAYES (MNB), MULTIVARIATE BERNOULLI DAN ROCCHIO ALGORITHM DALAM KLASIFIKASI KONTEN BERITA HOAX BERBAHASA INDONESIA PADA MEDIA SOSIAL.
Azeez, N. A., Idiakose, S. O., Onyema, C. J., & Vyver, C. V. D. (2021). Cyberbullying Detection in Social Networks: Artificial Intelligence Approach. Journal of Cyber Security and Mobility. https://doi.org/10.13052/jcsm2245-1439.1046
Berrar, D. (2018). Cross-Validation. https://doi.org/10.1016/B978-0-12-809633-8.20349-X
Booker, L. B., Goldberg, D. E., & Holland, J. H. (1989). Classifier sistem and genetic algorithms. Artificial Intelligence, 40(1–3), 235–282. https://doi.org/10.1016/0004-3702(89)90050-7
Brownlee, J. (2016). Deep learning with Python: Develop deep learning models on Theano and TensorFlow using Keras. Machine Learning Mastery.
Busiarli, N., Aditya, L. A., & Andika, A. Y. (2016). PENERAPAN ALGORITMA NAÏVE BAYES & NATURAL LANGUAGE PROCESSING UNTUK MENGKLASIFIKASI JENIS BERITA PADA ARSIP PEMBERITAAN. 6.
Christian, H., Agus, M. P., & Suhartono, D. (2016). Single document automatic text summarization using term frequency-inverse document frequency (TF-IDF). ComTech: Computer, Mathematics and Engineering Applications, 7(4), 285–294.
Darmalaksana, W., Irwansyah, F. S., Sugilar, H., Maylawati, D. S., Azis, W. D. I., & Rahman, A. (2021). Logical framework for hate speech detection on religion issues in Indonesia. IOP Conference Series: Materials Science and Engineering, 1098(3), 032046. https://doi.org/10.1088/1757-899X/1098/3/032046
Dzaffa ’Ulhaq, Suarna, N., & Dwilestari, G. (2022). Klasifikasi Berita Kriminal Menggunakan Algoritma Naïve Bayes Berbasis PSO. INFORMATICS FOR EDUCATORS AND PROFESSIONAL : Journal of Informatics, 6(2), 116–125. https://doi.org/10.51211/itbi.v6i2.1701
Fawcett, T. (2006). An introduction to ROC analysis. Pattern Recognition Letters, 27(8), 861–874. https://doi.org/10.1016/j.patrec.2005.10.010
Gärtler, M., Khaydarov, V., Klöpper, B., & Urbas, L. (2021). The Machine Learning Life Cycle in Chemical Operations – Status and Open Challenges. Chem. Ing. Tech., 12, 18.
Ghimire, D. (2020). Comparative study on Python web frameworks: Flask and Django. 40.
Hadna, N. M. S., Santosa, P. I., & Winarno, W. W. (2016). STUDI LITERATUR TENTANG PERBANDINGAN METODE UNTUK PROSES ANALISIS SENTIMEN DI TWITTER. 9.
Harahap, C. N., Marthasari, G. I., & Hayatin, N. (2021). Perbandingan Klasifikasi Berita Hoax Kategori Kesehatan Menggunakan Naive Bayes dan Multinomial Naive Bayes. Jurnal Repositor, 3(4), Article 4. https://doi.org/10.22219/repositor.v3i4.1380
Hayaza, Q., Wahyuni, E. D., & Anjani, A. (2020). KLASIFIKASI BERITA PADA AKUN TWITTER SUARA SURABAYA MENGGUNAKAN METODE NAÏVE BAYES. Jurnal Informatika Dan Sistem Informasi, 1(2), Article 2. https://doi.org/10.33005/jifosi.v1i2.112
Huang, G.-B., Zhu, Q.-Y., & Siew, C.-K. (2006). Extreme learning machine: Theory and applications. Neurocomputing, 70(1–3), 489–501.
Janah, A. K., Wahyuni, E. D., & Arifiyanti, A. A. (2020). KLASIFIKASI EMOSI ULASAN APLIKASI TRAVELOKA PADA GOOGLE PLAY MENGGUNAKAN NAÏVE BAYES. . . November, 1(3).
Kurniawan, D., & Creativity, J. (2017). Menangkal Cyberporn. Elex Media Komputindo.
Mustofa, H., & Mahfudh, A. A. (2019). Klasifikasi Berita Hoax Dengan Menggunakan Metode Naive Bayes. Walisongo Journal of Information Technology, 1(1), Article 1.
Nurdin, N., Suhendri, M., Afrilia, Y., & Rizal, R. (2021). Klasifikasi Karya Ilmiah (Tugas Akhir) Mahasiswa Menggunakan Metode Naive Bayes Classifier (NBC). Sistem: Jurnal Sistem Informasi, 10(2), Article 2. https://doi.org/10.32520/stmsi.v10i2.1193
Purwiantono, F. E., & Aditya, A. (2020). KLASIFIKASI SENTIMEN SARA, HOAKS DAN RADIKAL PADA POSTINGAN MEDIA SOSIAL MENGGUNAKAN ALGORITMA NAIVE BAYES MULTINOMIAL TEXT. Jurnal Tekno Kompak, 14(2), 68. https://doi.org/10.33365/jtk.v14i2.709
Pustejovsky, J., & Stubbs, A. (2013). Natural language annotation for machine learning. O’Reilly Media.
Putri, N. B., & Wijayanto, A. W. (2022). Analisis Komparasi Algoritma Klasifikasi Data Mining Dalam Klasifikasi Website Phishing. Komputika : Jurnal Sistem Komputer, 11(1), 59–66. https://doi.org/10.34010/komputika.v11i1.4350
Riaddy, A. I., Sibaroni, Y., & Si, S. (2016). Ekstraksi Informasi pada Makalah Ilmiah dengan Pendekatan Supervised Learning Information Extraction on Scientific Papers with Supervised Learning Approach. 2016, 3, 7.
Ristiari, L., Karyawati, A. E., Suputra, I. P. G. H., Muliantara, A., Darmawan, I. D. M. B. A., & Widiartha, I. M. (2022). Klasifikasi Cerita Pendek Berbahasa Bali Berdasarkan Umur Pembaca dengan Metode Naive Bayes. JELIKU (Jurnal Elektronik Ilmu Komputer Udayana), 10(4), 363. https://doi.org/10.24843/JLK.2022.v10.i04.p06
Roh, Y., Heo, G., & Whang, S. E. (2021). A Survey on Data Collection for Machine Learning: A Big Data - AI Integration Perspective. IEEE Transactions on Knowledge and Data Engineering, 33(4), 1328–1347. https://doi.org/10.1109/TKDE.2019.2946162
Saleh, A. (2015). Implementasi Metode Klasifikasi Naïve Bayes Dalam Memprediksi Besarnya Penggunaan Listrik Rumah Tangga. 2(3), 11.
Salman, H. A., & Obaida, T. H. (2021). BBC NEWS DATA CLASSIFICATION USING NAÏVE BAYES BASED ON BAG OF WORD. 2021.
Saraswati, M., & Riminarsih, D. (2021). Analisis Sentimen Terhadap Pelayanan Krl Commuterline Berdasarkan Data Twitter Menggunakan Algortima Bernoulli Naive Bayes. Jurnal Ilmiah Informatika Komputer, 25(3), 225–238.
Setiawan, A., Santoso, L. W., & Adipranata, R. (2020). Klasifikasi Artikel Berita Bahasa Indonesia Dengan Naive Bayes Classifier.
Shofiya, F., Arifianto, D., Kom, M., & Al Faruq, H. A. (2020). Perbandingan Algoritma Support Vector Machine (Svm) Dan Multinomial Naive Bayes (Mnb) Dalam Klasifikasi Abstrak Tugas Akhir (Studi Kasus: Fakultas Teknik Universitas Muhammadiyah Jember). Undergraduate thesis, Universitas Muhammadiyah Jember.
Singh, G., Kumar, B., Gaur, L., & Tyagi, A. (2019). Comparison between Multinomial and Bernoulli Naïve Bayes for Text Classification. 2019 International Conference on Automation, Computational and Technology Management (ICACTM), 593–596. https://doi.org/10.1109/ICACTM.2019.8776800
Sokolova, M., & Lapalme, G. (2009). A sistem analysis of performance measures for classification tasks. Information Processing & Management, 45(4), 427–437. https://doi.org/10.1016/j.ipm.2009.03.002
Somvanshi, M., Chavan, P., Tambade, S., & Shinde, S. V. (2016). A review of machine learning techniques using decision tree and support vector machine. 2016 International Conference on Computing Communication Control and Automation (ICCUBEA), 1–7. https://doi.org/10.1109/ICCUBEA.2016.7860040
Supriati, E., & Fikawati, S. (2009). Effect of Pornography Exposure on Junior High School Teenagers of Pontianak in 2008. Makara Human Behavior Studies in Asia, 13(1), 48. https://doi.org/10.7454/mssh.v13i1.210
Webb, G. (2016). Naïve Bayes (hlm. 1–2). https://doi.org/10.1007/978-1-4899-7502-7_581-1
Wibowo, A. P., & Darmawan, A. S. (2020). Penerapan Algoritma Naïve Bayes Untuk Klasifikasi Konten Berita Olahraga. IC-Tech, 15(1), Article 1. https://doi.org/10.47775/ictech.v15i1.85
Xu, S., Li, Y., & Wang, Z. (2017). Bayesian Multinomial Naïve Bayes Classifier to Text Classification. Dalam J. J. Park, S.-C. Chen, & K.-K. Raymond Choo (Ed.), Advanced Multimedia and Ubiquitous Engineering (Vol. 448, hlm. 347–352). Springer Singapore. https://doi.org/10.1007/978-981-10-5041-1_57
Yance Nanlohy, L., Mulyanto Yuniarno, E., & Mardi Susiki Nugroho, S. (2020). Classification of Public Complaint Data in SMS Complaint Using Naive Bayes Multinomial Method. 2020 4th International Conference on Vocational Education and Training (ICOVET), 241–246. https://doi.org/10.1109/ICOVET50258.2020.9229941
