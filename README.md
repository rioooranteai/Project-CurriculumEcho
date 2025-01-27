# **Technical Report: Analisis Kurikulum Merdeka Menggunakan Clustering dan BERTopic**

---

## **Status Proyek Saat Ini**

Saat ini, proyek sedang fokus pada dua aktivitas utama:

1. **Hyperparameter Tuning**:  
   - Mengoptimalkan metode embedding (**SBERT**, **IndoBERT**) dan algoritma clustering (**HDBSCAN**, **KMeans**, **Agglomerative Clustering**) menggunakan **Optuna**.
   - Mengevaluasi metode reduksi dimensi seperti **UMAP**, **PCA**, dan **t-SNE** untuk meningkatkan kualitas clustering.

2. **Pembaruan Laporan**:  
   - Memperbarui laporan dengan hasil evaluasi terbaru dari proses *hyperparameter tuning*.  

---

## **1. Overview**

Proyek ini bertujuan untuk menganalisis persepsi netizen terhadap Kurikulum Merdeka di Indonesia melalui data yang diambil dari Twitter menggunakan hashtag terkait. Solusi ini menerapkan *topic modeling* menggunakan **BERTopic** untuk menemukan pola dan topik dominan dalam diskusi online. Hasil analisis ini diharapkan memberikan wawasan mendalam bagi pemangku kebijakan pendidikan dan pihak terkait untuk memahami persepsi publik terhadap Kurikulum Merdeka.

---

## **2. Motivation**

Kurikulum Merdeka merupakan inisiatif besar dalam sistem pendidikan Indonesia yang bertujuan meningkatkan kualitas pembelajaran. Namun, pemahaman masyarakat tentang efektivitas dan implementasi kurikulum ini masih beragam. Dengan meningkatnya penggunaan media sosial, analisis persepsi netizen terhadap kebijakan pendidikan menjadi lebih relevan dari sebelumnya. Proyek ini bertujuan untuk menyediakan wawasan berdasarkan data aktual untuk membantu perbaikan kebijakan pendidikan di masa mendatang.

---

## **3. Success Metrics**

- **Kualitas Clustering**: Diukur menggunakan **silhouette score** untuk memastikan topik yang dihasilkan representatif dan terstruktur dengan baik.
- **Jumlah Topik yang Relevan**: Mengidentifikasi topik utama yang signifikan terkait Kurikulum Merdeka.
- **Wawasan yang Dihasilkan**: Jumlah dan kualitas wawasan yang dapat membantu pemangku kebijakan dalam memahami persepsi publik.
- **Akurasi Evaluasi**: Menilai efektivitas metode embedding dan algoritma clustering yang digunakan setelah *hyperparameter tuning*.

---

## **4. Requirements & Constraints**

### **4.1 Functional Requirements**

1. **Pengumpulan Data**: Mengambil data dari Twitter dengan hashtag seperti `#kurikulummerdeka` dan `#pendidikanIndonesia`.
2. **Preprocessing Data**: Membersihkan data (menghapus *stopwords*, emoji, dan data yang tidak relevan).
3. **Topic Modeling**: Menggunakan BERTopic untuk menemukan dan memvisualisasikan topik.
4. **Evaluasi Model**: Menggunakan **silhouette score** dan *hyperparameter tuning* untuk meningkatkan akurasi model.

### **4.2 Constraints**

- **Teknis**: Penggunaan algoritma clustering seperti HDBSCAN, KMeans, atau Agglomerative sesuai dengan performa terbaik setelah *hyperparameter tuning*.
- **Waktu Pemrosesan**: Batas pemrosesan data maksimal 5 menit.
- **Biaya Infrastruktur**: Anggaran terbatas untuk penggunaan layanan cloud.

### **4.3 What's In-Scope & Out-of-Scope**

- **In-Scope**:  
  - Analisis topik dari data Twitter.  
  - *Hyperparameter tuning* untuk BERTopic.  

- **Out-of-Scope**:  
  - Analisis sentimen mendalam.  
  - Penggunaan data dari sumber selain Twitter.  
  - Penyempurnaan model real-time.

---

## **5. Methodology**

### **5.1 Problem Statement**

Masalah ini diformulasikan sebagai **unsupervised learning problem** menggunakan *topic modeling* untuk menemukan dan mengelompokkan topik terkait Kurikulum Merdeka dari percakapan netizen di Twitter.

### **5.2 Data**

- **Sumber Data**: Data Twitter yang diambil menggunakan hashtag `#kurikulummerdeka` dan `#pendidikanIndonesia`.  
- **Jumlah Data**: Sekitar 15.000 sampel teks dari hasil scraping.  
- **Preprocessing**:  
  - Pembersihan teks (stopwords, emoji, URL).  
  - Tokenisasi.  
  - Stemming (opsional).

### **5.3 Techniques**

1. **Embedding Methods**:  
   - **SBERT**  
   - **IndoBERT**  

2. **Clustering Algorithms**:  
   - **HDBSCAN**  
   - **KMeans**  
   - **Agglomerative Clustering**  
   - Pemilihan algoritma terbaik berdasarkan **silhouette score**.
   - Evaluasi performa embedding dengan *hyperparameter tuning* menggunakan **Optuna**.

3. **Dimensionality Reduction**:  
   - **UMAP**  
   - **PCA**  
   - Menggunakan Optuna untuk *hyperparameter tuning*.
---

## **6. Results and Analysis**


---

## **7. Conclusion**

Proyek ini berhasil mengidentifikasi dan mengelompokkan topik terkait Kurikulum Merdeka menggunakan BERTopic dengan embedding dari IndoBERT dan SBERT. Hasil ini memberikan wawasan berguna untuk pemangku kebijakan dalam memahami persepsi publik terhadap kebijakan pendidikan.

---
