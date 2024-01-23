# Latihan-SKLearn-Cross-Validation-Split

**Tahapan Latihan**

Tahapan yang dilakukan pada codelab ini sebagai berikut:

- Impor library yang dibutuhkan.

- Pisahkan antara atribut dan label pada dataset.

- Buat model decision tree.

- Hitung hasil cross validation dari model dengan fungsi cross_val_score().

**Codelab**

Para pengembang ML biasanya meng-import  semua library yang dibutuhkan di cell pertama. Dalam tahap latihan ini, Anda akan melakukan import library pada cell yang berkaitan saja. Tujuannya adalah agar Anda memahami fungsi setiap library yang digunakan dalam model ML yang Anda buat.

Dataset yang akan kita gunakan adalah dataset iris yang dipakai pada submodul sebelumnya.

![1](https://github.com/brnabidin/Latihan-SKLearn-Cross-Validation-Split/assets/67081096/f62e4ab7-edee-42c6-8848-e9a4c449a775)

Kemudian kita bagi antara atribut dan label pada dataset.

![2](https://github.com/brnabidin/Latihan-SKLearn-Cross-Validation-Split/assets/67081096/7f0f81d9-55ee-4f7f-b8af-36242dde053b)

Kita akan membuat model machine learning pertama kita yaitu decision tree, menggunakan library scikit learn. Model machine learning juga sering disebut sebagai classifier. Lebih lanjut, variabel clf adalah singkatan dari classifier.

![3](https://github.com/brnabidin/Latihan-SKLearn-Cross-Validation-Split/assets/67081096/93fe8e19-d738-4b0c-b054-d405e4c8a059)

Setelah dataset dan model siap, kita bisa menggunakan cross validation untuk mengevaluasi performa dari model machine learning. Fungsi cross_val_score() seperti di bawah menerima 4 parameter yaitu, ‘clf’ yang merupakan model machine learning, ‘X’ yang merupakan atribut dari dataset, ‘y’ yang merupakan label dari dataset, dan ‘cv’ yang merupakan jumlah fold yang akan dipakai pada cross validation.

![4](https://github.com/brnabidin/Latihan-SKLearn-Cross-Validation-Split/assets/67081096/7aa6da9d-29b7-4702-974e-ef7aa330468c)

Cross_val_score mengembalikan nilai berupa larik atau array yang terdiri dari akurasi pengujian setiap fold dari dataset. Untuk mencetak dan mengetahui hasilnya, tambahkan kode scores di bawah kode sebelumnya. Tampilannya seperti gambar di bawah ini.

![5](https://github.com/brnabidin/Latihan-SKLearn-Cross-Validation-Split/assets/67081096/80573ced-8d87-4e65-8e88-17edd5c4dd1a)

Elemen pertama dari larik menunjukkan nilai 0.96666 yang berarti ketika fold pertama dijadikan validation set dan fold lainnya dijadikan train set, hasil dari pengujian tersebut adalah akurasi sebesar 0.96666. 

Melihat akurasi dari seluruh pengujian fold yang memiliki nilai tinggi dan konsisten pada tiap fold, kita mendapatkan gambaran bahwa model kita memiliki performa yang sangat baik.

Secara umum jika hasil dari pengujian tiap fold pada cross validation memiliki nilai yang bervariasi dari 0.85 sampai 0.99, maka model tersebut dapat dikatakan baik.
