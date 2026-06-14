# Smart Inventory AI Assistant

Smart Inventory AI Assistant adalah aplikasi chatbot berbasis Artificial Intelligence (AI) yang dirancang untuk membantu analisis dan pengelolaan inventory secara lebih efektif. Aplikasi ini dibangun menggunakan **Streamlit** sebagai antarmuka web interaktif dan **Google Gemini API** sebagai Large Language Model (LLM) untuk memberikan insight, rekomendasi, dan menjawab pertanyaan pengguna terkait kondisi inventory.

Project ini memungkinkan pengguna untuk mengunggah dataset inventory, melakukan analisis kondisi stok, mendeteksi risiko stockout maupun overstock, menampilkan dashboard visualisasi data, serta berinteraksi dengan chatbot AI untuk mendapatkan rekomendasi berbasis data.

Project ini dibuat sebagai Final Project dari program LLM-Based Tools and Gemini API Integration for Data Scientists by Hacktiv8. Project ini bertujuan untuk mengimplementasikan teknologi Large Language Model (LLM) dalam kasus nyata di bidang Inventory Management dan Supply Chain Analytics.

---

## Tujuan Project

Tujuan utama dari Smart Inventory AI Assistant adalah membantu pengguna dalam:

* Memantau kondisi inventory secara real-time.
* Mengidentifikasi risiko kehabisan stok (Stockout).
* Mengidentifikasi stok berlebih (Overstock).
* Menentukan prioritas produk yang perlu direstock.
* Mendapatkan rekomendasi inventory berbasis AI.
* Mengubah data inventory menjadi insight yang mudah dipahami.

---

## Fitur Utama

### Upload Dataset Inventory

Pengguna dapat mengunggah dataset inventory dalam format:

* CSV (.csv)
* Excel (.xlsx)
* Excel (.xls)

---

### Dataset Preview

Menampilkan isi dataset yang telah diunggah sehingga pengguna dapat memverifikasi data sebelum dilakukan analisis.

---

### Inventory Dashboard

Dashboard secara otomatis menampilkan:

* Total produk dengan risiko Stockout
* Total produk dengan kondisi Normal
* Total produk dengan kondisi Overstock

---

### 📈 Visualisasi Data Interaktif

Menggunakan Plotly untuk menampilkan:

#### 1. Sales Trend Analysis

Visualisasi tren penjualan berdasarkan waktu.

#### 2. Sales by Category

Visualisasi jumlah penjualan berdasarkan kategori produk.

#### 3. Inventory Status Distribution

Visualisasi distribusi status inventory dalam bentuk Donut Chart.

---

### Priority Restock Recommendation

Sistem secara otomatis mengidentifikasi 10 produk dengan Inventory Coverage terendah yang perlu diprioritaskan untuk dilakukan restock.

---

### AI Inventory Chatbot

Menggunakan Google Gemini API untuk memberikan insight dan rekomendasi inventory berbasis data.

Contoh pertanyaan yang dapat diajukan:

* Produk mana yang harus segera direstock?
* Kategori apa yang memiliki risiko stockout tertinggi?
* Bagaimana kondisi inventory saat ini?
* Berikan rekomendasi inventory berdasarkan data saya.
* Produk apa yang memiliki stok berlebih?

---

### Chat Memory

Aplikasi menggunakan Streamlit Session State sehingga riwayat percakapan tetap tersimpan selama sesi berlangsung.

Fitur ini memungkinkan chatbot mempertahankan konteks percakapan sebelumnya dan memberikan pengalaman yang lebih interaktif.

---

## 🛠️ Teknologi yang Digunakan

| Teknologi         | Fungsi                         |
| ----------------- | ------------------------------ |
| Python            | Bahasa Pemrograman Utama       |
| Streamlit         | Framework Web Application      |
| Google Gemini API | Large Language Model (LLM)     |
| Pandas            | Data Processing & Analysis     |
| Plotly            | Interactive Data Visualization |
| Ngrok             | Public URL Deployment          |
| Google Colab      | Development Environment        |

---

## Alur Analisis Inventory

### 1. Upload Dataset

Pengguna mengunggah dataset inventory.

↓

### 2. Data Preparation

Kolom yang digunakan untuk analisis:

* Store ID
* Product ID
* Category
* Inventory Level
* Units Sold
* Demand Forecast

↓

### 3. Inventory Coverage Calculation

Formula:

```text
Inventory Coverage = Inventory Level ÷ Demand Forecast
```

↓

### 4. Inventory Classification

| Status         | Kondisi                  |
| -------------- | ------------------------ |
| Stockout Risk  | Inventory Coverage < 1   |
| Normal         | Inventory Coverage 1 – 5 |
| Overstock Risk | Inventory Coverage > 5   |

↓

### 5. Restock Prioritization

Produk dengan Inventory Coverage terendah diprioritaskan untuk dilakukan restock.

↓

### 6. AI Recommendation

Data inventory dikirim ke Gemini API untuk menghasilkan rekomendasi dan insight berbasis AI.

---

##  Tampilan Aplikasi

Tambahkan screenshot aplikasi pada bagian ini.

### Dashboard Inventory

* Inventory Health Dashboard
* Sales Trend Analysis
* Sales by Category
* Inventory Status Distribution

### AI Chatbot

* Inventory Recommendation
* Inventory Insights
* Conversational Analysis

---

## Author

**Nadia Chusnul Ikromah**

Linkedin: www.linkedin.com/in/nadiacikr

---

## 📄 License

Project ini dibuat untuk tujuan pembelajaran, pengembangan keterampilan, dan portfolio.
