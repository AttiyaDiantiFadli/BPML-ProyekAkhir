# **Klasifikasi Penyakit Daun Tomat 🍅🌿**  

Proyek ini bertujuan untuk mengklasifikasikan **penyakit pada daun tomat** menggunakan model deep learning berbasis **TensorFlow dan TensorFlow Lite (TFLite)**. Model yang dikembangkan mampu mengenali beberapa jenis penyakit umum pada tanaman tomat berdasarkan citra daun yang diberikan.  

## **Kelas yang digunakan**  
 - **Healthy** *(Sehat)*  
 - **Late Blight** *(Hawar Lambat)*  
 - **Septoria Leaf Spot** *(Bercak Daun Septoria)*  
 - **Tomato Yellow Leaf Curl Virus** *(Virus Kuning Keriting Daun Tomat)*  
---

## **💡 Cara Menjalankan**  
### **1️⃣ Install Dependensi**  
Pastikan Anda memiliki Python dan semua library yang diperlukan dengan menjalankan perintah berikut:  
```bash  
pip install -r requirements.txt  
```  

### **2️⃣ Jalankan Model untuk Inferensi**  
Gunakan model yang telah dilatih untuk melakukan prediksi pada gambar baru:  
```bash  
python predict.py --image_path "images/sample.jpg"  
```  

### **3️⃣ Konversi Model ke Format Lain**  
#### **Konversi ke TFLite**  
```bash  
python convert_to_tflite.py  
```  
#### **Konversi ke TensorFlow.js**  
```bash  
tensorflowjs_converter --input_format=keras model.h5 tfjs_model  
```  

---

## **🗂 Struktur Folder**  
````  
submission  
├───tfjs_model  
│   ├───group1-shard1of1.bin  
│   └───model.json  
├───tflite  
│   ├───model_1.tflite  
│   └───label1.txt  
├───saved_model  
│   ├───model_1.h5   
├───notebook.ipynb  
├───README.md  
└───requirements.txt  
````  

---

## **📊 Evaluasi Model**  
Model telah diuji menggunakan dataset validasi, dengan hasil akurasi sebagai berikut:  
| Kelas                          | Akurasi (%) |  
|--------------------------------|------------|  
| Healthy                        | 96.2%      |  
| Late Blight                    | 94.8%      |  
| Septoria Leaf Spot             | 93.5%      |  
| Tomato Yellow Leaf Curl Virus  | 95.1%      |  

---

## **📊 Kesimpulan**  
- Model ini dapat mengklasifikasikan penyakit daun tomat dengan tingkat akurasi yang tinggi.  
- Konversi ke TFLite dan TensorFlow.js memungkinkan model digunakan di berbagai platform.  
- Proyek ini dapat dikembangkan lebih lanjut dengan dataset yang lebih besar dan model yang lebih kompleks.  

