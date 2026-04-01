# Analiza Ryzyka Chorób Układu Krążenia – Projekt Badawczy

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![ML](https://img.shields.io/badge/Machine%20Learning-XGBoost-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## Opis projektu
Projekt został zrealizowany w ramach **pracy inżynierskiej**. Skupia się na wykorzystaniu zaawansowanych technik uczenia maszynowego do predykcji wystąpienia chorób sercowo-naczyniowych na podstawie danych medycznych (np. ciśnienie krwi, cholesterol, wiek, wzrost).

Głównym atutem projektu jest nie tylko wysoka skuteczność modelu, ale także jego **interpretowalność** dzięki zastosowaniu metod **Explainable AI (XAI)**.

---

## Stack Technologiczny
* **Język:** Python
* **Analiza danych:** `Pandas`, `NumPy`
* **Wizualizacja:** `Seaborn`, `Matplotlib`
* **Statystyka:** `SciPy`, `Statsmodels` (testy chi-kwadrat, korelacja Persona)
* **ML & XAI:** `XGBoost`, `SHAP`, `Scikit-learn`

---

## Kluczowe Etapy Analizy

### 1. Czyszczenie i przygotowanie danych
* **Konwersja jednostek:** Wiek przeliczony z dni na lata dla lepszej czytelności.
* **Feature Engineering:** Obliczenie wskaźnika **BMI**.
* **Usuwanie błędów:** Eliminacja rekordów z błędnie wpisanym ciśnieniem (np. `ap_hi` < `ap_lo`).
* **Filtracja Outlierów:** Zastosowanie metod statystycznych do usunięcia wartości skrajnych dla wzrostu i wagi.

### 2. Eksploracyjna Analiza Danych (EDA)
* Badanie rozkładów cech ilościowych.
* Analiza istotności statystycznej cech jakościowych za pomocą **testu Chi-kwadrat**.
* Wizualizacja korelacji parametrów medycznych z występowaniem chorób.

### 3. Modelowanie i Wyjaśnialność (XAI)
Zastosowano model **XGBoost**, który został poddany analizie za pomocą wartości **SHAP** (Shapley Additive Explanations). Dzięki temu wiemy, że:
* **Najważniejsze czynniki:** Największy wpływ na ryzyko chorób ma **ciśnienie skurczowe**, **wiek** oraz **poziom glukozy**.
* **Zgodność kliniczna:** Wyniki modelu pokrywają się z aktualną wiedzą medyczną, co potwierdza jego wiarygodność.

---

## Struktura plików
* `inzynierka (2).ipynb` – Główny plik z kodem, analizą i modelem.
* `cardio_train.csv` – Zbiór danych wejściowych.
* `dane_z_wiekiem_w_latach.csv` – Przetworzony zestaw danych.

---
