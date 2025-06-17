# Rozpoznawanie gatunku ptaka po jego odgłosie
### Bartosz Kąkol

17.06.2025

## Co oznaczają pliki
- folder `models/` - zawiera wytrenowane modele
  - `model_epoch_11.keras` - model wytrenowany na 11 epokach z ostateczną architekturą (tą, która jest teraz w notebooku)
  - `model_epoch_50.keras` - model wytrenowany na 50 epokach z inną — mniejszą — architekturą (m.in. nie posiadała Droput, BatchNormalization, miała inaczej skonstruowane warstwy Conv2D, itd.)
  - `svm_model.joblib` - model SVM
  - ~~`randomforest_model.joblib` - model Random Forest Classifier~~ _model Random Forest zajmuje 22 GB, więc nie znajduje się w repozytorium._

### Modele nie zmieściły się w repo, ale można pobrać je z mojego dysku pod [tym linkiem](https://drive.google.com/drive/folders/1eoEdSqf7kAAjsAunKQ01dDNgc1TNo7Dd?usp=sharing).

- folder `results/` - zawiera wszelkie wyniki tekstowe oraz wykresy
  - folder `Conv/` zawiera wyniki dla modelu sieci konwolucyjnej
  - folder `MLP/` zawiera wyniki dla modelu Multi-Layer Perceptron
    - foldery `relu/` i `tanh/` zawierają wyniki dla aktywacji ReLU i Tanh
  - folder `RandomForestClassifier/` zawiera wyniki dla modelu Random Forest Classifier
  - folder `SVM/` zawiera wyniki dla modelu Support Vector Classifier

Pliki w `results/` mogą przechowywać:
- `acc.txt` - zapisane ręcznie dokładności modeli, jeżeli było ich kilka tego samego rodzaju
- `confusion_matrix.png` - macierz pomyłek dla danego modelu
- `learning.png`/`curve.png` - krzywe uczenia modelu
  - `learning_normalized.png` - krzywe uczenia modelu znormalizowane względem procentu przebiegu całego treningu
- `result.txt` - informacje o dokładności modelu na zbiorze testowym i czasie treningu