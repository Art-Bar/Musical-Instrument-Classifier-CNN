# Wyniki eksperymentów

Wyniki zostały opracowane na **zmniejszonym zbiorze danych**:

- **1000 próbek** ze zbioru treningowego  
- **500 próbek** ze zbioru walidacyjnego  
- **500 próbek** ze zbioru testowego

---

## 1. Prosty model CNN

![Prosty model CNN](image-3.png)

**Evaluation Metrics:**

- Accuracy:    0.7380  
- Sensitivity: 0.6620  
- Precision:   0.6409  
- F1-Score:    0.6165

![Prosty model CNN - wykres](image-4.png)

---

## 2. Złożony model CNN

![Złożony model CNN](image-10.png)

**Evaluation Metrics:**

- Accuracy:    0.6840  
- Sensitivity: 0.5983  
- Precision:   0.5699  
- F1-Score:    0.5287

![Złożony model CNN - wykres](image-11.png)

---

## 3. Dostrojony model VGG19

### 3.1 Pierwsza faza  
*(wszystkie warstwy części konwolucyjnej zamrożone)*

![VGG19 - pierwsza faza](image-5.png)

**Evaluation Metrics:**

- Accuracy:    0.4020  
- Sensitivity: 0.2125  
- Precision:   0.2253  
- F1-Score:    0.1405

![VGG19 - pierwsza faza wykres](image-6.png)

### 3.2 Druga faza  
*(odmrożone ostatnie 8 warstw części konwolucyjnej)*

![VGG19 - druga faza](image-7.png)

**Evaluation Metrics:**

- Accuracy:    0.6400  
- Sensitivity: 0.5979  
- Precision:   0.6460  
- F1-Score:    0.5463

![VGG19 - druga faza wykres](image-8.png)

---

## Uwagi i spostrzeżenia

- Uzyskane wyniki opierają się na podziale danych ustalonym przez twórców zbioru Medley-Solos-DB. 
- Powyższe wyniki uzyskano trenując sieci na zmniejszonym zbiorze danych zawierającym 2000 próbek. Próbki w podzbiorach treningowym, testowym i walidacyjnym pochodziły z odpowiadających im sekcji oryginalnego zbioru, choć proporcje liczebności tych podzbiorów nieco się różnią.
- Gdy ustalono **własny podział danych treningowych, testowych oraz walidacyjnych**, modele osiągały **znacznie wyższą dokładność**. Różnica wynika prawdopodobnie z faktu, że w podziale narzuconym przez twórców zbiory pochodzą z **różnych źródeł**, więc model jest zmuszony klasyfikować próbki wyłącznie po brzmieniu instrumentu.  

