---
layout: post
title: "Simple Linear Regression dengan R: Prediksi dan Hubungan Linier"
date: 2025-06-26
categories: [statistik, r]
tags: [r, regresi, statistik, linear-regression, prediksi]
---

**Regresi Linier Sederhana (Simple Linear Regression)** adalah metode statistik untuk memodelkan hubungan **linier** antara satu variabel independen (X) dan satu variabel dependen (Y).

---

## 📈 Apa itu Regresi Linier Sederhana?

Model regresi linier sederhana mengikuti bentuk umum:

\[
Y = \beta_0 + \beta_1 X + \varepsilon
\]

- $Y$: variabel dependen (yang diprediksi)  
- $X$: variabel independen (prediktor)  
- $\beta_0$: intercept (nilai Y saat X = 0)  
- $\beta_1$: slope (kemiringan garis regresi)  
- $\varepsilon$: error (residu)

---

## 🧪 Contoh di R

```r
# Contoh data
set.seed(123)
x <- rnorm(50, mean = 10, sd = 2)
y <- 3 * x + rnorm(50, mean = 0, sd = 5)

# Model regresi linier
model <- lm(y ~ x)

# Lihat ringkasan model
summary(model)
