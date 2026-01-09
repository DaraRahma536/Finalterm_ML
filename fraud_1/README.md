**============================================**   
**DETEKSI PENIPUAN TRANSAKSI DENGAN MODEL DEEP LEARNING**   
**============================================**   

*Nama: Dara Rahma Safitri*   
*NIM: 1103220169*   
*Kelas: TK-46-02*   

Tujuan Repository
   -
   Proyek ini menggunakan model Deep Learning untuk mendeteksi penipuan (fraud) dalam transaksi keuangan. Tujuan utamanya adalah membangun model klasifikasi yang dapat mengidentifikasi transaksi penipuan dengan transaksi normal.
   
Penjelasan Singkat
   - 
   Proyek ini mengimplementasikan pipeline end-to-end dengan model Deep Learning lengkap untuk mendeteksi penipuan. Proyek ini menggunakan sumber data berupa **train_transaction.csv** dan **test_transaction.csv**.Skala data yang digunakan sekitar 590.000 sampel training dengan 393 fitur dan 506.000 sampel testing. Dalam pemrosesan data menggunakan polars agar lebih ringan dan cepat, sedangkan untuk modeling menggunakan Neural Network dan TensorFlow/Keras.
 
Deskripsi Model dan Hasil Metriks
   -
   - **Model**   
     Neural Network (Deep Learning) dengan arsitektur yang diuji:
     - Small_Network: 2 lapisan tersembunyi (32, 16 neuron)
     - Medium_Network: 3 lapisan tersembunyi (64, 32, 16 neuron)
     - Deep_Network: 4 lapisan tersembunyi (128, 64, 32, 16 neuron)
     - Wide_Network: 2 lapisan lebar (128, 64 neuron)
       
     Hypermeter Tuning (Berdasarkan AUC Validation):
     - Small_Network → AUC Validasi: 0.8233
     - Medium_Network → AUC Validasi: 0.8129   
     - Deep_Network → AUC Validasi: 0.8125   
     - Wide_Network → AUC Validasi: 0.8110   

       Model terbaik adalah **Small_Network** dengan AUC Validasi tertinggi.   
   - **Matriks Evaluasi**   
     - Loss (Training dan Validasi)
     - AUC
     - Accuracy
     - Precision
     - Recall
     
Navigasi Notebooks
   -
   - **Struktur Repository**   
     ├── UTS1_ML_Dara(NoTuning).ipynb &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Notebook utama (baseline tanpa tuning)   
├── midterm_folder/ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Folder data (dari Google Drive)   
│   ├── train_transaction.csv &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Data training   
│   └── test_transaction.csv &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Data testing   
├── best_dl_model.keras preprocessing   
├── fraud_detection_dl_model.h5   
├── scaler.pkl   
├── fraud_detection_dl_submission.csv   
└── dl-results_summary.json

   - **Navigasi Notebook**
     - Instalasi Modul dan Import Library (polars, Sckit-learn, TensorFlow, dll)
     - Download dataset Training dan Testing
     - Load Dataset   
     - Preprocessing Data (membersihkan Data, mengisi nilai null, dan encoding fitur kategorikal)
     - Simple Feature Engineering (membuat fitur tambahan seperti statistik dan interaksi fitur)
     - Deep Learning Model (membangun arsitektur Neural Network dengan Batch Normalization dan Dropout)
     - Hyperparameter Tuning (menguji beberapa konfigurasi arsitektur jaringan)
     - Train Deep Learning Model (melatih model dengan data training dan memvisualisasikan riwayat pelatihan)
     - Save Result Summary

