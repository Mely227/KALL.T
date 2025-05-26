---
title: Transformasi Matriks

---

##### Ringkasan dan Tugas [Transformasi Matriks]

Transformasi Matriks adalah Bayangin kamu punya vektor (misalnya panah yang nunjuk ke suatu arah), terus kamu "ubah" bentuk atau arahnya pakai aturan tertentu. Nah, kalau aturan itu bisa ditulis pakai perkalian matriks, itu disebut.Dengan menggunakan matriks $A$ berukuran $m$ X $n$ bisa digunakan untuk mendefinisikan sebuah fungsi $T$ yang mengambil vektor kolom $\vec{x}$ adalah vektor kolom berukuran $n \times 1$ dan menghasilkan vektor kolom $\vec{y}$ berukuran $m \times 1$ melalui persamaan:
$$
\vec{y} = T(\vec{x}) = A\vec{x}
$$

Fungsi ini disebut *Transformasi Matriks, dan termasuk dalam kelas umum yang biasanya disebut **Transformasi Linier* yaitu fungsi antar vektor

---

* Perkalian Matriks - Vektor

Agar hasil perkalian tetap berupa vektor  2D $(\ \mathbb{R}^2)$, maka matriks $A$ harus berukuran $2$ X $2$. 
Diberikan matriks $A$ dan tiga vektor $\vec{x},\ \vec{y},\ \vec{z}$ hasil perkalian antara matriks dan vektor dihitung sebagai berikut:
$$
A = \begin{bmatrix}
4 & 2 \\
1 & 3
\end{bmatrix}, \quad
\vec{x} = \begin{bmatrix}
1 \\
1
\end{bmatrix}, \quad
\vec{y} = \begin{bmatrix}
-1 \\
1
\end{bmatrix}, \quad
\vec{z} = \begin{bmatrix}
3 \\
-1
\end{bmatrix}
$$


Solusi:
$$
A\vec{x} = \begin{bmatrix}
5 \\
5
\end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix}
-3 \\
1
\end{bmatrix}, \quad
A\vec{z} = \begin{bmatrix}
-1 \\
3
\end{bmatrix}
$$


Perkalian matriks mengubah panjang dan arah vektor dalam contoh di atas vektor $\vec{x}$ dan $A\vec{x}$ memiliki arah yang sama tapi panjangnya yang berubah. Namun, $\vec{y}$ dan $\vec{z}$ beruubah arah saat dikalikan dengan $A$. Hal ini menunjukkan bahwa matriks bertindak secara berbeda terhadap vektor yang berbeda.

---

* Menggabungkan penjumlahan dan perkalian matriks

Diketahui:

$$
A = \begin{bmatrix}
1 & 1 \\
1 & 2
\end{bmatrix}, \quad
\vec{x} = \begin{bmatrix}
2 \\
1
\end{bmatrix}, \quad
\vec{y} = \begin{bmatrix}
-1 \\
1
\end{bmatrix}
$$


Sketsa: $\vec{x} + \vec{y}$,$A\vec{x}$,$A\vec{y}$ dan $A(\vec{x}+\vec{y})$
langkah ini bertujuan untuk melihat bagaimana penjumlahan vektor berinteraksi dengan transformasi matriks.

Dihitung:

$$
\vec{x} + \vec{y} = \begin{bmatrix}
1 \\
2
\end{bmatrix}, \quad
A\vec{x} = \begin{bmatrix}
3 \\
4
\end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix}
0 \\
1
\end{bmatrix}, \quad
A(\vec{x} + \vec{y}) = \begin{bmatrix}
3 \\
5
\end{bmatrix}
$$


Ini menunjukkan *sifat distributif* dari perkalian matriks terhadap penjumlahan vektor: $$A(\vec{x} + \vec{y}) = A\vec{x} + A\vec{y}$$

---

* Menggambar Efek dari Perkalian matriks

Diketahui:

$$
A = \begin{bmatrix}
1 & 1 \\
-1 & -1
\end{bmatrix}, \quad
\vec{x} = \begin{bmatrix}
1 \\
1
\end{bmatrix}, \quad
\vec{y} = \begin{bmatrix}
-1 \\
1
\end{bmatrix}, \quad
\vec{z} = \begin{bmatrix}
4 \\
4
\end{bmatrix}
$$


Solusi:

$$
A\vec{x} = \begin{bmatrix}
0 \\
0
\end{bmatrix} \quad 
A\vec{y} = \begin{bmatrix}
-2 \\
-2
\end{bmatrix} \quad
and \quad
A\vec{z} = \begin{bmatrix}
3 \\
3\end{bmatrix}
$$

Beberapa vektor seperti $(\vec{x}$ dan $\vec{y})$ setelah dikalikan dengan matriks, hasilnya adalah vektor nol sementara vektor lain tetepa berada pada garis tertentu.

---

* Transformasi terhadap bidang kartesius

Pada bagian ini memeperkenalkan transisi dan menggambarkan vektor satu per satu ke menggambarkan bagaimana seluruh bidang katresius $(\ \mathbb{R}^2)$berubah oleh matriks.

* Visualisasi Transformasi Matriks Menggunnakan vektor

efek transformasi terhadap seluruh bidang Kartesius dengan melihat bagaimana *persegi satuan (unit square)* berubah.
Misalkan: 

$$
A = \begin{bmatrix}
1 & 4 \\
2 & 3
\end{bmatrix}
$$


Titik - titik sudut dari persegi satuan berada di:

$$
\begin{bmatrix}
0 \\
0
\end{bmatrix}, \quad
\begin{bmatrix}
1 \\
0
\end{bmatrix}, \quad
\begin{bmatrix}
1 \\
1
\end{bmatrix}, \quad
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$


Setelah dikalikan deng $A$, titik - titik tersebut menjadi:


$$
\begin{bmatrix}
0 \\
0
\end{bmatrix}, \quad
\begin{bmatrix}
1 \\
2
\end{bmatrix}, \quad
\begin{bmatrix}
5 \\
5
\end{bmatrix}, \quad
\begin{bmatrix}
4 \\
3
\end{bmatrix}
$$

 Adapun tips cepat untuk menggunakan matriks kolom: 
 Buat matriks $B$ yang kolom - kolomnya adalah titik - titik sudut:


$$
B = \begin{bmatrix}
0 & 1 & 1 & 0 \\
0 & 0 & 1 & 1
\end{bmatrix}
$$


Dikalikan:

$$
AB = \begin{bmatrix}
0 & 2 & 6 & 4 \\
0 & 1 & 4 & 3
\end{bmatrix}
$$


Proses ini cepat jika harus dilakukan transformasi pada banyak titik sekaligus

Perubahan bentuk dari persegi satuan setelah dikalikan dengan matriks:

$$
A = \begin{bmatrix}
1 & 4 \\
2 & 3
\end{bmatrix}
$$ 

Menghasilkan persegi berubah menjadi jajargenjang. Selain merenggang, bentuknya juga tampak terbalik, seolah titik - titik segitiga dan persegi saling bertukar tempat.
menggambarkan bahwa garis-garis lurus pada persegi satuan tetap lurus setelah transformasi oleh matriks, meskipun bentuknya berubah.

* Transformasi Matriks terhadap sebuah wilayah

Matriks yang digunakan: 

$$
A = \begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix}
$$ 

Matriks ini merupakan rotasi 90 derajat berlawanan arah jarum jam terhadap titik asal (0,0) dalam bidang kartesius.

* Komposisi Transformasi

Transformasi dapat digabung seperti fungsi:

$$
(T \circ S)(\vec{x}) = T(S(\vec{x}))$$

maka:

$$
(T \circ S)(\vec{x}) = AB\vec{x}
$$

Artinya, komposisi dua transformasi linier bisa direpresentasikan sebagai perkalian dua matriks.

* Ringkasan

- Urutan penting! Karena perkalian matriks tidak komutatif, maka 

$$ AB \ne BA $$
- Visualisasi transformasi sering dilakukan dengan melihat bagaimana unit square (persegi satuan) berubah.

- Transformasi non-linear tidak bisa direpresentasikan dengan matriks (contoh: translasi).

#### Tugas [Transformasi Matriks]

##### 1.

$$ A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} $$

##### Jawaban 1
- Diketahui :

$$[
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{y} = \begin{bmatrix} -1 \\ 2 \end{bmatrix}
]$$

- Penyelesaian :

$$[
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}
]$$


$$[
A\vec{x} = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix}
= \begin{bmatrix} 0 \\ 5 \end{bmatrix}
]$$


$$[
A\vec{y} = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} -1 \\ 2 \end{bmatrix}
= \begin{bmatrix} -3 \\ 4 \end{bmatrix}
]$$


##### 2. 

$$ B = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix} $$

##### Jawaban 2

Diketahui :

$$[
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{y} = \begin{bmatrix} -1 \\ 2 \end{bmatrix}, \quad
A = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix}
]$$

Penyelesaian :
$$[
A\vec{x} = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix}
\begin{bmatrix} 1 \\ 1 \end{bmatrix}
= \begin{bmatrix} 2 \cdot 1 + 0 \cdot 1 \\ -1 \cdot 1 + 3 \cdot 1 \end{bmatrix}
= \begin{bmatrix} 2 \\ 2 \end{bmatrix}
]$$

$$[
A\vec{y} = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix}
\begin{bmatrix} -1 \\ 2 \end{bmatrix}
= \begin{bmatrix} 2 \cdot (-1) + 0 \cdot 2 \\ -1 \cdot (-1) + 3 \cdot 2 \end{bmatrix}
= \begin{bmatrix} -2 \\ 7 \end{bmatrix}
]$$

Jadi hasilnya :

$$[
A\vec{x} = \begin{bmatrix} 2 \\ 2 \end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix} -2 \\ 7 \end{bmatrix}
]$$

##### Jawaban 5

Dari gambar diketahui transformasi berikut:

$$[
\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \rightarrow \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix} \rightarrow \begin{bmatrix} 1 \\ 3 \end{bmatrix}
]$$

Maka matriks transformasinya adalah:

$$[
A = \begin{bmatrix} 1 & 1 \\ 2 & 3 \end{bmatrix}
]$$

##### Jawaban 6
Dari gambar diketahui transformasi berikut:

$$[
\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \rightarrow \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix} \rightarrow \begin{bmatrix} -1 \\ 1 \end{bmatrix}
]$$

Maka matriks transformasinya adalah:

$$[
A = \begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}
]$$



