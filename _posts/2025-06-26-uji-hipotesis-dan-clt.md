---
layout: post
title: "Pengenalan Uji Hipotesis dan Central Limit Theorem"
date: 2025-06-26
categories: [statistik, konsep-dasar]
tags: [statistik, uji-hipotesis, central-limit-theorem, clt, inferensi, tailed test]
---

Statistik inferensial membantu kita mengambil keputusan atau membuat kesimpulan berdasarkan data. Dua konsep penting yang mendasari banyak analisis statistik adalah **Uji Hipotesis** dan **Central Limit Theorem (CLT)**.

---

## Apa itu Uji Hipotesis?

**Uji Hipotesis** adalah prosedur statistik untuk mengevaluasi asumsi atau klaim tentang populasi berdasarkan data sampel.

### Langkah-langkah Uji Hipotesis:

1. **Tentukan Hipotesis Nol ($H_0$)**: klaim awal yang ingin diuji.  
2. **Tentukan Hipotesis Alternatif ($H_1$)**: klaim yang akan diterima jika $H_0$ ditolak.  
3. **Tentukan Taraf Signifikansi ($\alpha$)**: misalnya 0.05 (5%).  
4. **Hitung Statistik Uji**: bergantung pada jenis uji (z-test, t-test, dll).  
5. **Tentukan p-value atau nilai kritis**.  
6. **Ambil keputusan**:  
   - Jika p-value < $\alpha$ → **Tolak $H_0$**  
   - Jika p-value ≥ $\alpha$ → **Gagal menolak $H_0$**

---

### 🧪 Contoh Uji Hipotesis di R:

```r
# Misal kita ingin menguji apakah rata-rata nilai berbeda dari 70
data <- c(72, 68, 74, 71, 69, 67, 73, 70, 72, 68)
t.test(data, mu = 70)  # uji t satu sampel
```

---

## One-Tailed vs Two-Tailed Test

### 1. **Two-Tailed Test**

Digunakan jika kita ingin mengetahui **apakah nilai berbeda** dari suatu nilai tertentu, tanpa arah tertentu.

- **Hipotesis**:  
  - $H_0$: $\mu = \mu_0$  
  - $H_1$: $\mu \neq \mu_0$  
- **Contoh**: Apakah rata-rata nilai siswa **berbeda** dari 70?

```r
t.test(data, mu = 70, alternative = "two.sided")
```

### 2. **One-Tailed Test**

Digunakan ketika kita ingin mengetahui apakah nilai rata-rata **lebih besar atau lebih kecil** dari suatu nilai tertentu. Tes satu sisi memiliki **arah yang jelas**.

#### 🔸 **Left-Tailed Test** (sisi kiri)

Menguji apakah rata-rata **lebih kecil dari** nilai tertentu.

- **Hipotesis**:  
  - $H_0$: $\mu \geq \mu_0$  
  - $H_1$: $\mu < \mu_0$
  
- **Contoh**: Apakah rata-rata nilai siswa **kurang dari 70**?

```r
t.test(data, mu = 70, alternative = "less")

