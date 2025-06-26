---
layout: post
title: "Analisis Korelasi dengan R: Memahami Hubungan antar Variabel"
date: 2025-06-26
categories: [statistik, r]
tags: [r, korelasi, statistik, pearson, hubungan-variabel]
---

Dalam analisis data, penting untuk memahami bagaimana dua variabel saling berhubungan. Salah satu cara untuk mengukur **kekuatan dan arah hubungan linier** antara dua variabel numerik adalah melalui **analisis korelasi**.

---

## 🔗 Apa itu Korelasi?

**Korelasi** adalah ukuran statistik yang menunjukkan **seberapa kuat dan ke arah mana** hubungan antara dua variabel.

Koefisien korelasi paling umum adalah **Pearson correlation coefficient ($r$)**, dengan nilai antara:

- **-1**: Korelasi negatif sempurna (semakin besar X, semakin kecil Y)
- **0**: Tidak ada korelasi linier
- **+1**: Korelasi positif sempurna (semakin besar X, semakin besar Y)

---

## 📊 Interpretasi Nilai Korelasi

| Nilai r          | Interpretasi              |
|------------------|---------------------------|
| -1.0             | Korelasi negatif sempurna |
| -0.7 s/d -0.9    | Korelasi negatif kuat     |
| -0.4 s/d -0.6    | Korelasi negatif sedang   |
| -0.1 s/d -0.3    | Korelasi negatif lemah    |
| 0                | Tidak ada korelasi        |
| 0.1 s/d 0.3      | Korelasi positif lemah    |
| 0.4 s/d 0.6      | Korelasi positif sedang   |
| 0.7 s/d 0.9      | Korelasi positif kuat     |
| 1.0              | Korelasi positif sempurna |

---

## 🧪 Contoh Analisis Korelasi di R

```r
# Membuat dua variabel yang berkorelasi positif
set.seed(123)
x <- rnorm(50, mean = 10, sd = 2)
y <- 3 * x + rnorm(50, mean = 0, sd = 5)

# Hitung koefisien korelasi Pearson
cor(x, y, method = "pearson")
