# Automated_Machine_Learning

# Project 1. Analiza Tunowalności Algorytmów Uczenia Maszynowego

## Wstęp
Celem projektu jest przeanalizowanie tunowalności hiperparametrów trzech wybranych algorytmów uczenia maszynowego (np. XGBoost, Random Forest, Elastic Net) na co najmniej czterech różnych zbiorach danych. Do optymalizacji hiperparametrów wykorzystano dwie różne techniki samplingu:  
1. Metody oparte na rozkładzie jednostajnym (np. Random Search, Uniform Grid Search).  
2. Techniki bayesowskie (np. BayesSearchCV z biblioteki `scikit-optimize` lub `SMAC3`).

Analiza opiera się na wynikach eksperymentów, które pozwolą na ocenę tunowalności algorytmów i ich hiperparametrów zgodnie z definicjami z artykułu *Tunability: Importance of Hyperparameters of Machine Learning Algorithms*.

---

## Metody Samplingu

### 1. **Rozkład jednostajny**
Metody polegające na równomiernym próbkowaniu przestrzeni hiperparametrów:  
- **Uniform Grid Search**: Regularna siatka punktów.
- **Random Search**: Losowe próbkowanie z rozkładu jednostajnego.

> **Uwaga:** Dla każdego algorytmu zastosowano tę samą siatkę hiperparametrów na wszystkich zbiorach danych.

### 2. **Technika bayesowska**
- **Bayesian Optimization**: Optymalizacja probabilistyczna oparta na modelowaniu funkcji celu.  
- Implementacja:  
  - `BayesSearchCV` z `scikit-optimize`.
  - `SMAC3` dla bardziej zaawansowanego dostosowania metod bayesowskich.

---

## Punkty Analizy

Na podstawie wyników eksperymentów przeanalizowano:

1. **Stabilność wyników**:
   - Liczba iteracji potrzebnych dla osiągnięcia stabilnych wyników w optymalizacji hiperparametrów.

2. **Zakresy hiperparametrów**:
   - Analiza zakresów dla każdego algorytmu na podstawie literatury i wyników eksperymentów.

3. **Tunowalność algorytmów**:
   - Ocena, które algorytmy są bardziej wrażliwe na tuning hiperparametrów.

4. **Tunowalność hiperparametrów**:
   - Które hiperparametry w największym stopniu wpływają na jakość modeli.

5. **Wpływ techniki samplingu**:
   - Analiza, czy różne techniki próbkowania (jednostajne vs. bayesowskie) wprowadzają różnice w wnioskach dotyczących tunowalności algorytmów i hiperparametrów.
   - Odpowiedź na pytanie: *Czy występuje bias sampling?*

---

## Rozszerzenia i Dodatkowe Analizy

- **Testy statystyczne**: Porównanie różnic wyników między technikami losowania hiperparametrów.
- **Critical Difference Diagrams**: Wykorzystanie diagramów do analizy większej liczby metod samplingu.
- **Wizualizacje**: Zaproponowanie alternatywnych wizualizacji wyników w porównaniu do cytowanego artykułu.

---

## Oczekiwany Wynik

Projekt obejmuje dwa główne elementy:

1. **Raport**: Szczegółowy opis metod i wyników eksperymentów (maksymalnie 4 strony A4).  
2. **Prezentacja**: Podsumowanie wyników i wniosków w formie prezentacji multimedialnej.

---
