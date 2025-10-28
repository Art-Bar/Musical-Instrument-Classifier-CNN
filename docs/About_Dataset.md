# Konwolucyjna sieć neuronowa (CNN) wytrenowana na Medley-Solos-DB

Zamieszczone w tym repozytorium **konwolucyjne sieci neuronowe (ang. Convolutional Neural Network, CNN)** zostały wytrenowane na zbiorze danych **Medley-Solos-DB**.

## O zbiorze Medley-Solos-DB

**Medley-Solos-DB** to kolekcja **3-sekundowych monofonicznych klipów audio**, w których każdy klip zawiera tylko **jeden instrument**. Składa się z:

- **Danych treningowych**: wyodrębnionych ze zbioru danych **MedleyDB** (Bittner i in., ISMIR 2014)
- **Zbioru testowego**: wyodrębnionego ze zbioru **solosDB** (Essid i in., IEEE TASLP 2009)

Taki podział danych pozwala sprawdzić, czy wytrenowany model potrafi **uogólniać wiedzę na nagrania z innych źródeł niż te ze zbioru treningowego**.

## Przygotowanie danych do treningu

W celu wytrenowania sieci neuronowych dla każdej próbki wygenerowano **mel frequency spectrogram**:

- Jest to widmo częstotliwościowe sygnału audio, przedstawione w **skali mel**, która jest bliższa percepcji ludzkiego ucha.
- W skali mel:
  - **Wyższe częstotliwości** są "ściśnięte"
  - **Niższe częstotliwości** przedstawione są bardziej szczegółowo

## Przykładowy spektrogram

![Przykładowy spektrogram](image.png)