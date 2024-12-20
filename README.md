# Detection of Invasive Ductal Carcinoma (IDC)
Dit project richt zich op het ontwikkelen van een machine learning-model dat middels image processing in staat is om gezond borstweefsel (IDC negative) te onderscheiden van ongezond weefsel (IDC positive). Invasive Ductal Carcinoma (IDC) is de meest voorkomende vorm van borstkanker.
In de huidige wereld gaat Machine Learning en AI een steeds grotere rol spelen, ook binnen de medische wereld. Daarom is een machine learning-model die dergelijk onderscheid kan maken van groots belang.

## Dataset
De dataset bestaat uit data van 279 verschillende patiënten. Hierbij gaat het om foto's van histologische uitsnedes van weefsel uit de borstklier. <br><br>

De data is te vinden op: <br>
```bash
assemblix:/data/datasets/thema10/
```

De data is opgedeeld in 2 verschillende mappen:
- `idc_regular.zip`: per patiënt een map met daarin 2 submappen, `0` en `1`. In beide submappen zitten afbeeldingen van de 50*50 pixels.
- `complete_images.zip`: per patiënt één beeld met alle kleine tegels op de juiste plek geplaatst.

De betekenis van de twee klassen:
- **Klasse 0:** IDC negative weefsel
- **Klasse 1:** IDC positive weefsel

De naamgeving van de afbeeldingen in de `idc_regular.zip` map is als volgt:<br>
```bash
<patient_id>_idx5_<x-coord>_<y-coord>_class[01].png
```

Hierbij geldt:
- `<patient_id>` het unieke identificatienummer van een patiënt is.
- `<x-coord>` en `<y-coord>` de coördinaten zijn van de uitsnede
- `class0` en `class1` respectievelijk IDC negative en IDC positive uitsneden tonen

## Usage
1. Kloon de repo:
```bash
https://github.com/DemiOever/casus_d.git
```
2. Haal de data op (zie kopje 'Dataset') en pak de bestanden uit.
3. Zorg dat de data binnen de repository staat. 
4. Klik op `Run All` in het bestand `data_loading.ipynb`.
4. Klik op `Run All` in het bestand `model_training.ipynb`.
5. Klik op `Run All` in het bestand `yolo.ipynb`.

Let op: het downloaden van de data en het runnen van de bestanden heeft een behoorlijke tijd nodig.

## Dependencies
- Python 3.11.2 of nieuwere versies
- Numpy
- Tensorflow
- os
- Keras
- Seaborn
- Matplotlib
- cv2 uit opencv-python

## Support
Wanneer je tegen problemen aanloopt of vragen hebt, neem dan contact op met een of beide auteuren.

## Authors
    Giel Bakker - g.j.bakker@st.hanzel.nl
    Demi van 't Oever - d.van.t.oever@st.hanze.nl