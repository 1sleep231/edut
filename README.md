# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding
Jaya Jaya Institut merupakan salah satu institusi pendidikan perguruan yang telah berdiri sejak tahun 2000. Hingga saat ini, institusi tersebut telah mencetak banyak lulusan dengan reputasi yang baik.
Akan tetapi, masih terdapat banyak juga siswa yang tidak menyelesaikan pendidikannya alias dropout. 

### Permasalahan Bisnis
Dari background tersebut, Jaya Jaya Institut ingin mendeteksi secepat mungkin siswa yang mungkin akan melakukan
dropout sehingga dapat diberi bimbingan khusus.

### Cakupan Proyek
- Bagaimana hubungan dan persebaran antara course dengan tingkat dropout?
- Apakah ada kecenderungan dropout jika berdasarkan tipe attendance?
- Apakah ada perbedaan yang signifikan dalam tingkat dropout antara siswa yang telah membayar kuliah tepat waktu (Tuition_fees_up_to_date) dan mereka yang belum?
- Apakah ada kecenderungan antara Admission Grade dengan Dropout?
- Mengetahui fitur-fitur akademis (numerik) mana yang berkontribusi terhadap dropout.

### Persiapan

Sumber data: (https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/students_performance/data.csv)

Setup environment:
```
- Menyiapkan virtual environment
- Menginstall dependencies yang diperlukan pada file requirements.txt
- Menjalankan dashboard.py di terminal dan membukanya di http://127.0.0.1:8050/
```

## Business Dashboard
Pada dashboard, ditampilkan feature yang berpengaruh pada dropout. Berikut penjelasannya:
1. **Curricular_units_2nd_sem_grade (0.1958) dan Curricular_units_2nd_sem_approved (0.1894)**
Fitur ini memiliki importance tertinggi dalam model, yang menunjukkan bahwa nilai rata-rata dan jumlah mata kuliah yang disetujui di semester kedua merupakan indikator kuat apakah siswa akan dropout atau berhasil.

2. **Admission_grade (0.1465)**
Nilai masuk juga merupakan faktor penting. Ini menunjukkan bahwa siswa yang masuk dengan nilai lebih rendah mungkin berisiko lebih tinggi untuk dropout, kemungkinan karena mereka kurang siap secara akademik.

3. **Curricular_units_1st_sem_approved (0.1282) dan Curricular_units_1st_sem_grade (0.1149)**
Seperti pada semester kedua, performa akademik di semester pertama juga memiliki dampak signifikan pada prediksi dropout. Jumlah mata kuliah yang disetujui dan nilai rata-rata di semester pertama sangat memengaruhi kesuksesan siswa ke depannya.

## Menjalankan Sistem Machine Learning
Jelaskan cara menjalankan protoype sistem machine learning yang telah dibuat. Selain itu, sertakan juga link untuk mengakses prototype tersebut.
```
- cara menjalankan prototype machine learning dengan menjalankan dashboard.py di terminal (sesuaikan dengan direktori Anda)
- masukkan data.csv dan rf_model.pkl pada satu folder yang sama dengan dashboard.py.
- lalu buka di http://127.0.0.1:8050/ 
```

## Conclusion
- Dari distribusi feature kategorik, ditemukan adanya dropout di setiap feature. Dengan kata lain, dropout tersebar secara merata di berbagai feature kategorik. Namun, ada beberapa kecenderungan, yaitu perbedaaan signifikan antara tingkat dropout di jurusan Management baik waktu malam (evening) maupun waktu pagi (daytime) memiliki tingkat dropout yang lebih tinggi dibandingkan dengan jurusan lain.
- Admission Grade memiliki peran penting dalam memprediksi risiko dropout. Siswa dengan nilai admission yang lebih rendah menunjukkan kecenderungan dropout yang lebih tinggi, menunjukkan bahwa kesiapan akademik saat masuk berpengaruh terhadap keberhasilan dalam studi. Intervensi awal, seperti program orientasi atau pelatihan keterampilan dasar, dapat membantu siswa yang berpotensi dropout.
- Fitur seperti Curricular_units_1st_sem_approved, Curricular_units_1st_sem_grade, dan Curricular_units_1st_sem_evaluations menunjukkan bahwa performa di semester pertama memiliki dampak signifikan pada keberhasilan jangka panjang siswa. Siswa yang menunjukkan nilai rendah dan persetujuan mata kuliah yang sedikit di semester pertama cenderung lebih berisiko untuk dropout.
- Nilai rata-rata dan jumlah mata kuliah yang disetujui di semester kedua (Curricular_units_2nd_sem_grade dan Curricular_units_2nd_sem_approved) memiliki importance tinggi dalam model prediksi. Siswa yang gagal menunjukkan peningkatan atau mempertahankan performa di semester kedua juga menunjukkan risiko dropout yang lebih tinggi.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- Program Dukungan Khusus untuk Siswa Berisiko
Siswa dengan nilai admission rendah dan performa awal yang kurang baik dapat dimasukkan dalam program dukungan khusus yang berfokus pada penguatan akademik.
- Pemantauan Ketat Selama Semester Awal
Pemantauan performa siswa, khususnya di semester pertama dan kedua, dapat membantu mengidentifikasi siswa berisiko sedini mungkin.
- Bimbingan Manajemen Beban Studi
Institusi dapat memberikan panduan kepada siswa dalam memilih jumlah mata kuliah yang sesuai dengan kemampuan mereka untuk mencegah beban akademik yang berlebihan.
