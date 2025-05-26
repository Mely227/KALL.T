---
title: Sistem Persamaan Linier

---

##### Sistem Persamaan Linier
Sistem Persamaan Linier (SPL) adalah kumpulan dua atau lebih persamaan linier yang memiliki variabel yang sama, dan solusi dari sistem tersebut adalah nilai variabel yang memenuhi semua persamaan secara bersamaan.

* Contoh SPL 

$$\begin{aligned}
    x + 2y + z &= 9 \\
    2x + y - z &= 3 \\
    3x - y + 2z &= 8
\end{aligned}$$


* Metode Penyelesaian
Substitusi, eliminasi, matriks, atau eliminasi Gauss.

1. Eliminasi Gauss
Eliminasi Gauss adalah metode untuk menyelesaikan sistem persamaan linear dengan mengubahnya ke bentuk eselon baris menggunakan operasi baris elementer.
Metode ini mempermudah penyelesaian SPL dengan menghilangkan variabel secara bertahap hingga tersisa satu variabel yang bisa disubstitusi kembali.

* Langkah-Langkah Eliminasi Gauss
1. Tulis Matriks Augmentasi
-Ubah SPL menjadi matriks augmentasi.
-Contoh:

$$\begin{aligned}
    x + 2y + z &= 9 \\
    2x + y - z &= 3 \\
    3x - y + 2z &= 8
\end{aligned}$$

*Menjadi*

$$\begin{bmatrix} 
1 & 2 & 1 & | 9 \\ 
2 & 1 & -1 & | 3 \\ 
3 & -1 & 2 & | 8 
\end{bmatrix}$$

2. Bentuk eslon Baris
-Gunakan Operasi Baris Elementer (OBE) untuk menghasilkan bentuk eselon baris:
* Elemen pivot (elemen pertama non-nol pada suatu baris) harus berada di kanan elemen pivot baris sebelumnya.
* Baris nol (jika ada) berada di bawah baris non-nol.

3. Subtitusi Balik
-Setelah matriks dalam bentuk eselon baris, lakukan substitusi balik untuk menemukan nilai variabel


##### SPL 3 PERSAMAAN
* Sistem dengan Satu Solusi : 

$$\begin{aligned}
    x + y + z &= 6 \\
    2x +3y + z &= 14 \\
    3x + 2y + 2z &= 17
\end{aligned}$$

* Penyelesaian:
1.  dalam bentuk Matriks Augmented

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
2 & 3 & 1 & | 13 \\ 
3 & 2 & 2 & | 17 
\end{bmatrix}$$

2. Eliminasi Gauss:
* Kurangi baris 2 dengan 2 x baris 1:

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
0 & 1 & -1 & | 1 \\ 
3 & 2 & 2 & | 17 
\end{bmatrix}$$

* Kurangi baris 3 dengan 3 x baris 1:

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
0 & 1 & -1 & | 1 \\ 
0 & -1 & -1 & | -1 
\end{bmatrix}$$

* Tambahkan baris 3 dengan baris 2:

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
0 & 1 & -1 & | 1 \\ 
0 & 0 & -2 & | 0
\end{bmatrix}$$

3. Substitusi Balik:
* Dari baris 3:
$2z = 0 \Rightarrow z = 0.$
* Dari baris 2:
$y-z=1 \Rightarrow y-0=1 \Rightarrow y=1$
* Dari baris 1:
$x+y+z=6 \Rightarrow x+1+0=6 \Rightarrow x=5$

4. Solusi: 
$(x,y,z)=(5,1,0)$

Sistem Memiliki **satu solusi unik**

5. Gambar Geogebra

<iframe scrolling="no" title="Satu Solusi (Berpotongan)" src="https://www.geogebra.org/material/iframe/id/mrkw38a5/width/1272/height/546/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="1272px" height="546px" style="border:0px;"> </iframe>


* Sistem dengan Solusi Tak Hingga: 

$$\begin{aligned}
    x + 2y + z &= 5 \\
    2x +4y + z &= 10 \\
    3x + 6y + 3z &= 13
\end{aligned}$$

* Penyelesaian:
1.  dalam bentuk Matriks Augmented

$$\begin{bmatrix} 
1 & 2 & 1 & | 5 \\ 
2 & 4 & 2 & | 10 \\ 
3 & 6 & 3 & | 15 
\end{bmatrix}$$

2. Eliminasi Gauss:
* Kurangi baris 2 dengan 2 x baris 1:

$$\begin{bmatrix} 
1 & 2 & 1 & | 5 \\ 
0 & 0 & 0 & | 0 \\ 
3 & 6 & 3 & | 15 
\end{bmatrix}$$

* Kurangi baris 3 dengan 3 x baris 1:

$$\begin{bmatrix} 
1 & 2 & 1 & | 5\\ 
0 & 0 & 0 & | 0 \\ 
0 & 0 & 0 & | 0
\end{bmatrix}$$

3. Analisis:

* Baris 2 dan baris 3 semuanya nol, menunjukkan bahwa sistem memiliki **solusi tak hingga**.

* Variabel bebas: 
$y dan z$

4. Solusi Umum:
Dari baris 1: $x+2y+z=5$,kita dapat menyatakan $x$ dalam bentuk $ydanz$:
$x=5-2y-z$

Solusi umum:
$(x,y,z)=(5-2a-b,a,b)$

5. Gambar Geogebra
<iframe scrolling="no" title="Solusi Tak Hingga" src="https://www.geogebra.org/material/iframe/id/ayyuvd9d/width/1272/height/546/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="1272px" height="546px" style="border:0px;"> </iframe>

* Sistem Tanpa Solusi : 

$$\begin{aligned}
    x + y + z &= 6 \\
    2x +3y + z &= 13 \\
    3x + 4y + 2z &= 20
\end{aligned}$$

* Penyelesaian:
1.  dalam bentuk Matriks Augmented

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
2 & 3 & 1 & | 13 \\ 
3 & 4 & 2 & | 20
\end{bmatrix}$$

2. Eliminasi Gauss:
* Kurangi baris 2 dengan 2 x baris 1:

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
0 & 1 & -1 & | 1 \\ 
3 & 4 & 2 & | 20 
\end{bmatrix}$$

* Kurangi baris 3 dengan 3 x baris 1:

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
0 & 1 & -1 & | 1 \\ 
0 & 1 & -1 & | 2 
\end{bmatrix}$$

* Tambahkan baris 3 dengan baris 2:

$$\begin{bmatrix} 
1 & 1 & 1 & | 6 \\ 
0 & 1 & -1 & | 1 \\ 
0 & 0 & 0 & | 1
\end{bmatrix}$$

3. Analisis:
* Baris 3 menunjukkan $0=1$, yang tidak mungkin. Ini berarti sistem **tidak memiliki solusi**.

4. Gambar Geogebra
<iframe scrolling="no" title="Tanpa Solusi" src="https://www.geogebra.org/material/iframe/id/ewttf4f4/width/630/height/538/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="630px" height="538px" style="border:0px;"> </iframe>


