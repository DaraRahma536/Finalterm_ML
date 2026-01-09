**===========================================**   
**DETEKSI TAHUN TERBIT LAGU DENGAN MODEL DEEP LEARNING**   
**===========================================**   

*Nama: Dara Rahma Safitri*   
*NIM: 1103220169*   
*Kelas: TK-46-02*   

Tujuan Repository
   -
   Proyek ini menggunakan model Deep Learning yang berfokus pada analisis data regresi menggunakan dataset berskala besar, implementasi model Deep Learning, serta evaluasi performa model yang digunakan.
   
Penjelasan Singkat
   - 
   Proyek ini menggunakan dataset berisi sekitar 515.000 sampel dengan 90 fitur audio untuk memprediksi tahun rilis lagu (variabel target). Pada proyek ini dilakukan penyeleksian fitur berdasarkan korelasi target dan pelatihan model dengan menggunakan Neural Network serta Hperparameter Tuning. Analisis hasil evaluasi model menggunakan matriks RMSE, MAE, R².
 
Deskripsi Model dan Hasil Metriks
   -
   - **Model**   
     Neural Network (TensorFlow/Keras)
     - Arsitektur: 128 → 64 → 32 → 1
     - Dropout dan Batch Normalization
     - Loss: MSE, Optimzer: Adam
       
     Hyperparameter Tuning
     - Menggunakan RandomizedSearchCV
     - Parameter terbaik: max_depth: None, min_samples_split: 6, n_estimators: 217
     
   - **Hasil Matriks**   
     - MSE: 89.04
     - RMSE: 9.44
     - MAE: 6.85
     - R²: 0.248

     Model dapat menjelaskan sekitar 24.8% variasi dalam data target. RMSE sekitar 9.44 tahun menunjukkan rata-rata error prediksi. 
     
Navigasi Notebooks
   -
   - **Struktur Repository**   
     ├── UTS2_DL_Dara.ipynb &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Notebook utama (baseline tanpa tuning)   

   - **Navigasi Notebook**
     - Instalasi Modul (polars, gdown, sklearn, dll)   
     - Download dataset training dan testing   
     - Load Dataset   
     - Preprocessing Data (mengisi nilai null, scaling fitur, pembagian data train, validasi, dan test 70/15/15, seleksi fitur dan pemilihan fitur)   
     - Pemodelan Deep Learning (train dengan Neural Network, train dengan early stopping, dan evaluasi model)   
     - Evaluasi Pada Data Uji (Pengujian model terbaik pada data uji serta menampilkan visualisasi hasil prediksi dan aktual)


