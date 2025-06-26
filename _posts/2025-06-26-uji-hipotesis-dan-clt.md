---
layout: post
title: "Pengenalan Uji Hipotesis dan Central Limit Theorem"
date: 2025-06-26
categories: [statistik, konsep-dasar]
tags: [statistik, uji-hipotesis, central-limit-theorem, clt, inferensi]
---

Statistik inferensial membantu kita mengambil keputusan atau membuat kesimpulan berdasarkan data. Dua konsep penting yang mendasari banyak analisis statistik adalah **Uji Hipotesis** dan **Central Limit Theorem (CLT)**.

---

## 📌 Apa itu Uji Hipotesis?

**Uji Hipotesis** adalah prosedur statistik untuk mengevaluasi asumsi atau klaim tentang populasi berdasarkan data sampel.

### 📖 Langkah-langkah Uji Hipotesis:

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
