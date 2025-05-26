---
title: ' Eigenvalue & Eigenvector '

---

##### Definisi Eigenvalue Eigenvector 

Eigenvalue atau Nilai eigen adalah Skalar yang digunakan untuk mengubah atau meregangkan vektor Eigen. Vektor eigen dan nilai eigen berkisar pada konsep matriks.Matriks digunakan dalam masalah pembelajaran mesin untuk mewakili sekumpulan besar informasi. Nilai eigen dan vektor eigen adalah tentang membangun satu vektor dengan satu nilai untuk mewakili matriks besar
* Misalkan  $A$ adalah matriks persegi misal $(n x n)$ ,maka Vektor tak nol $v$ disebut eigenvector dari $A$ ,jika :

$$ A \mathbf{v} = \lambda \mathbf{v} $$

Dimana:
* $A$ = Matriks
* $v$ = eigenvektor
* $\lambda$ = eigenvalue (skalar)

 Artinya,tranformasi matriks $A$ terhadap vekbor $v$ hanya mengubah skala vektor tersebut dikali dengan $\lambda$ ,arahnya tetap

##### Mencari **eigenvalue** dan **eigenvector** dari matriks:

$A = \begin{bmatrix} 2 & -1 \\ 4 & 3 \end{bmatrix}$

---

**Langkah 1: Mencari Eigenvalue**

Gunakan persamaan karakteristik:

$\det(A - \lambda I) = 0$

Kurangkan $\lambda I$ dari $A$:

$A - \lambda I = \begin{bmatrix} 2 - \lambda & -1 \\ 4 & 3 - \lambda \end{bmatrix}$

Hitung determinan:

$\begin{aligned}
\det(A - \lambda I) &= (2 - \lambda)(3 - \lambda) - (-1)(4) \\
&= (2 - \lambda)(3 - \lambda) + 4 \\
&= \lambda^2 - 5\lambda + 10
\end{aligned}$

Selesaikan persamaan kuadrat:

$\lambda = \frac{5 \pm \sqrt{(-5)^2 - 4(1)(10)}}{2(1)} = \frac{5 \pm \sqrt{-15}}{2} = \frac{5}{2} \pm \frac{i\sqrt{15}}{2}$

Jadi, dua nilai eigen:

$\lambda_1 = \frac{5}{2} + \frac{i\sqrt{15}}{2}$  
$\lambda_2 = \frac{5}{2} - \frac{i\sqrt{15}}{2}$

---

**Langkah 2: Mencari Eigenvector**

Gunakan nilai $\lambda_2 = \frac{5}{2} - \frac{i\sqrt{15}}{2}$

Matriks $A - \lambda_2 I$:

$\begin{bmatrix}
\frac{-1}{2} + \frac{i\sqrt{15}}{2} & -1 \\
4 & \frac{3}{2} + \frac{i\sqrt{15}}{2}
\end{bmatrix}$

Misal vektor eigen berbentuk:

$\vec{v} = \begin{bmatrix} x \\ 1 \end{bmatrix}$

Gunakan baris pertama:

$\left( \frac{-1}{2} + \frac{i\sqrt{15}}{2} \right)x - 1 = 0$

Selesaikan:

$x = \frac{1}{\frac{-1}{2} + \frac{i\sqrt{15}}{2}} = \frac{2}{-1 + i\sqrt{15}}$

Rasionalisasi:

$x = \frac{2(-1 - i\sqrt{15})}{(-1 + i\sqrt{15})(-1 - i\sqrt{15})} = \frac{-2 - 2i\sqrt{15}}{16} = \frac{-1 - i\sqrt{15}}{8}$

Maka, vektor eigen untuk $\lambda_2$:

$\vec{v}_2 = \begin{bmatrix} \frac{-1 - i\sqrt{15}}{8} \\ 1 \end{bmatrix}$

---

**Kesimpulan:**

- Eigenvalue:  
  $\lambda_1 = \frac{5}{2} + \frac{i\sqrt{15}}{2}$  
  $\lambda_2 = \frac{5}{2} - \frac{i\sqrt{15}}{2}$

- Eigenvector untuk $\lambda_2$:  
  $\vec{v}_2 = \begin{bmatrix} \frac{-1 - i\sqrt{15}}{8} \\ 1 \end{bmatrix}$

```python=
# Code untuk Konfirmasi
import numpy as np
from numpy import linalg as LA
input = np.array([[2,-1],[4,3]])
w, v = LA.eig(input)
print(w)
print(v)
```
```python=
Output:
[2.5+1.93649167j 2.5-1.93649167j]
[[ 0.1118034 -0.4330127j  0.1118034 +0.4330127j]
 [-0.89442719+0.j        -0.89442719-0.j       ]]
```


##### Ortogonal & Ortonormal

1. **Ortogonal**  
Dua vektor dikatakan ortogonal jika hasil *dot product* (perkalian titik) antara keduanya adalah nol.  
Secara matematis, jika ada dua vektor $u$ dan $v$, maka:

$u \cdot v = 0$

Artinya:
- Vektor $u$ dan $v$ saling tegak lurus (membentuk sudut 90°).
- Tidak harus memiliki panjang (norma) tertentu.

2. **Ortonormal**  
Sekumpulan vektor dikatakan ortonormal jika mereka ortogonal satu sama lain **dan** masing-masing memiliki panjang (norma) 1.

Syarat ortonormal:
- Ortogonal antar vektor: $u \cdot v = 0$ jika $u \ne v$
- Norma 1 untuk setiap vektor: $||u|| = 1$

Misal $\vec{u}, \vec{v} \in \mathbb{R}^n$, maka:

$\vec{u} \cdot \vec{v} = 0$ jika $\vec{u} \ne \vec{v}$  
$||\vec{u}|| = 1$ dan $||\vec{v}|| = 1$

---

**Contoh:**  
Misalkan kita punya matriks simetris 2x2:

$A = \begin{bmatrix} 4 & 1 \\ 1 & 3 \end{bmatrix}$

**Langkah: Cari Eigenvalue**  
Hitung determinan:

$\det(A - \lambda I) = \left| \begin{array}{cc} 4 - \lambda & 1 \\ 1 & 3 - \lambda \end{array} \right| = (4 - \lambda)(3 - \lambda) - 1 = 0$

Maka:

$\lambda^2 - 7\lambda + 11 = 0$

Gunakan rumus kuadrat:

$\lambda = \frac{7 \pm \sqrt{49 - 44}}{2} = \frac{7 \pm \sqrt{5}}{2}$

Jadi:

$\lambda_1 = \frac{7 + \sqrt{5}}{2}, \quad \lambda_2 = \frac{7 - \sqrt{5}}{2}$

---

**Langkah: Cari Eigenvector**  
Misal untuk $\lambda_1 \approx 5.618$:

$A - \lambda_1 I \approx \begin{bmatrix} -1.618 & 1 \\ 1 & -2.618 \end{bmatrix}$

Ambil baris pertama:

$-1.618x + y = 0 \Rightarrow y = 1.618x$

Maka vektor eigen (belum dinormalisasi):

$\vec{v}_1 = \begin{bmatrix} 1 \\ 1.618 \end{bmatrix}$

Norma:

$||\vec{v}_1|| = \sqrt{1^2 + (1.618)^2} \approx \sqrt{3.618} \approx 1.902$

Normalisasi:

$\vec{u}_1 = \frac{1}{1.902} \begin{bmatrix} 1 \\ 1.618 \end{bmatrix} \approx \begin{bmatrix} 0.526 \\ 0.851 \end{bmatrix}$

---

Lakukan hal serupa untuk $\lambda_2 \approx 1.382$:

$A - \lambda_2 I \approx \begin{bmatrix} 2.618 & 1 \\ 1 & 1.618 \end{bmatrix}$

Ambil salah satu baris:

$2.618x + y = 0 \Rightarrow y = -2.618x$

Maka vektor eigen:

$\vec{v}_2 = \begin{bmatrix} 1 \\ -2.618 \end{bmatrix}$

Norma:

$||\vec{v}_2|| = \sqrt{1^2 + (-2.618)^2} = \sqrt{7.854} \approx 2.802$

Normalisasi:

$\vec{u}_2 = \frac{1}{2.802} \begin{bmatrix} 1 \\ -2.618 \end{bmatrix} \approx \begin{bmatrix} 0.357 \\ -0.934 \end{bmatrix}$

---

**Hasil Akhir: Basis Ortonormal dari Eigenvektor**

Dua vektor ortonormal hasil normalisasi eigenvektor:

$\vec{u}_1 = \begin{bmatrix} 0.526 \\ 0.851 \end{bmatrix}, \quad \vec{u}_2 = \begin{bmatrix} 0.357 \\ -0.934 \end{bmatrix}$

Verifikasi:
1. $\vec{u}_1 \cdot \vec{u}_2 = 0$ (ortogonal)  
2. $||\vec{u}_1|| = 1$, $||\vec{u}_2|| = 1$ (norma 1)  
3. Jadi keduanya adalah **ortonormal**  
4. Dan merupakan **eigenvektor dari A**

</small>

```python=
# Kode Phython Konfirmasinya
import numpy as np

# Matriks simetris
A = np.array([[4, 1],
              [1, 3]])

# Cari eigenvalue dan eigenvektor
eigenvalues, eigenvectors = np.linalg.eig(A)

# Tampilkan hasil
print("Eigenvalue:")
print(eigenvalues)
print("\nEigenvektor (sebelum dinormalisasi):")
print(eigenvectors)

# Normalisasi eigenvektor untuk jadi ortonormal
normalized_vectors = []
for v in eigenvectors.T:  # per kolom (karena np.linalg.eig mengembalikan kolom sebagai vektor)
    norm = np.linalg.norm(v)
    normalized_vectors.append(v / norm)

# Konversi ke array NumPy
normalized_vectors = np.array(normalized_vectors)

print("\nEigenvektor yang sudah dinormalisasi (ortonormal):")
print(normalized_vectors)
```

```python=
Output:

Eigenvalue:
[4.61803399 2.38196601]

Eigenvektor (sebelum dinormalisasi):
[[ 0.85065081 -0.52573111]
 [ 0.52573111  0.85065081]]

Eigenvektor yang sudah dinormalisasi (ortonormal):
[[ 0.85065081  0.52573111]
 [-0.52573111  0.85065081]]
```
