
# Deteksi dan Klasifikasi Jenis Kerusakan Jalan Berbasis WebGIS

## Research Overview

Penelitian ini mengusulkan penerapan YOLOv8 untuk mendeteksi area kerusakan jalan dan MobileNetV3 untuk mengklasifikasikan jenis kerusakan berdasarkan citra hasil deteksi. Informasi hasil analisis kemudian diintegrasikan ke dalam WebGIS untuk menyajikan persebaran kerusakan jalan secara geografis.

## 1. Dataset Rencana Riset Kecil

### Sumber Dataset
- Dataset publik: Road Damage Detection 2022 (RDD2022).
- Dataset tambahan: citra kerusakan jalan lokal, apabila tersedia.

### Kategori Kerusakan
- Retak memanjang (*longitudinal crack*)
- Retak melintang (*transverse crack*)
- Retak kulit buaya (*alligator crack*)
- Lubang (*pothole*)

Kategori akhir akan disesuaikan dengan anotasi dan ketersediaan data.

### Rencana Pengolahan Data
1. Seleksi dan pemeriksaan kualitas citra.
2. Anotasi area kerusakan menggunakan bounding box.
3. Pelabelan kelas kerusakan.
4. Pembagian data train, validation, dan test.
5. Preprocessing dan augmentasi pada data train.

## 2. Research Gap

Penelitian terdahulu telah membahas deteksi kerusakan jalan menggunakan deep learning, klasifikasi jenis kerusakan, serta pemetaan kondisi jalan berbasis GIS.

Penelitian ini mengusulkan alur dua tahap yang menggabungkan YOLOv8 untuk deteksi area kerusakan dan MobileNetV3 untuk klasifikasi jenis kerusakan. Hasilnya diintegrasikan ke dalam WebGIS untuk menampilkan informasi kerusakan berdasarkan lokasi geografis.

Kesenjangan penelitian yang akan dikaji meliputi:
1. Evaluasi penggunaan deteksi dan klasifikasi dalam dua tahap.
2. Pengukuran kinerja deteksi dan klasifikasi secara terpisah.
3. Integrasi hasil analisis citra dengan informasi spasial.
4. Pengujian kinerja sistem pada variasi kondisi citra.

## 3. Research Method

Alur penelitian:

Citra Jalan
→ Preprocessing
→ YOLOv8 (Deteksi)
→ Ekstraksi Area Kerusakan
→ MobileNetV3 (Klasifikasi)
→ Penyimpanan Koordinat dan Hasil
→ WebGIS

## 4. Evaluation Metrics

### YOLOv8 - Object Detection
- Precision
- Recall
- mAP@0.5
- mAP@0.5:0.95
- Waktu inferensi

### MobileNetV3 - Image Classification
- Accuracy
- Precision per kelas
- Recall per kelas
- Macro F1-score
- Confusion matrix

### WebGIS
- Black-box testing
- Validasi koordinat pada peta
- Waktu pemrosesan alur sistem

## 5. References

[1] H. Maeda et al., "Road Damage Detection and Classification
Using Deep Neural Networks with Smartphone Images,"
Computer-Aided Civil and Infrastructure Engineering,
vol. 33, no. 12, pp. 1127–1141, 2018.

[2] P. J. Pardeshi et al., "Patch-Based Self-Supervised Learning
for Road Damage Classification: A Case Study on the RDD2022
Dataset of Indian Test Site," ISPRS Annals, 2025.
