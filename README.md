# Auto-Annotation-Dataset-Roboflow
# Tutorial Auto-Annotation Dataset dengan Grounding DINO & Autodistill


Project ini merupakan tugas kelompok yang membahas proses **Auto-Annotation** (anotasi otomatis) untuk kebutuhan **Object Detection**. 
Berbeda dengan metode manual, project ini memanfaatkan *Foundation Model* (Grounding DINO) untuk mendeteksi dan melabeli objek secara otomatis hanya dengan menggunakan perintah teks (*ontology*), sehingga mempercepat proses penyiapan dataset.

👥 Anggota Kelompok

1. [Ahasanul Ikram] ([231001026])
2. [Dinda Oktavia Pratiwi] ([231001026])

🛠 Tools yang Digunakan

* **Autodistill & Grounding DINO** (Foundation Model untuk Labeling)
* **Supervision** (Visualisasi dan Manajemen Dataset)
* **Python**
* **Google Colab** (Akselerasi GPU)
* **YOLOv8** (Model target hasil training)
* **VsCode**

📂 Tahapan Pengerjaan

1️⃣ Persiapan Environment & Library
Menginstal library `autodistill-grounding-dino` dan mengunci versi `transformers` pada 4.38.2 untuk menjaga stabilitas sistem.

2️⃣ Penentuan Ontology
Mendefinisikan objek target melalui teks. Contoh: menentukan kata "scissors" untuk dideteksi sebagai label "scissors" pada gambar.

3️⃣ Proses Auto-Labeling
Menjalankan `base_model.predict()` pada seluruh gambar mentah. Model AI akan otomatis mencari objek dan memberikan *bounding box* tanpa intervensi manual.

4️⃣ Filtering & NMS (Non-Max Suppression)
Membersihkan hasil deteksi yang tumpang tindih menggunakan fungsi NMS agar anotasi menjadi lebih akurat dan rapi.

5️⃣ Export Dataset ke Format YOLO
Hasil anotasi otomatis dieksport ke format `.txt` (YOLO) agar siap digunakan langsung untuk proses training model deteksi objek.

6️⃣ Training & Inference
Melatih model YOLOv8 dengan dataset hasil auto-labeling dan melakukan pengujian (*inference*) menggunakan OpenCV DNN.

📊 Hasil

Proses labeling yang biasanya memakan waktu berjam-jam dapat diselesaikan dalam hitungan menit dengan akurasi yang tinggi. Dataset hasil anotasi otomatis ini terbukti valid untuk melatih model YOLOv8 hingga mencapai performa yang optimal.

✅ Kesimpulan

Auto-Annotation menggunakan Grounding DINO dan Autodistill adalah solusi masa depan untuk efisiensi pembuatan dataset AI, memungkinkan pengembang untuk membangun model Object Detection secara cepat tanpa terkendala proses labeling manual yang melelahkan.

🎥 Link Video YouTube

[https://youtu.be/pTAV3heaMbk?si=k051G9TWlqwskWbe]
