# Distanziamento sociale

Un'applicazione web che utilizza la videocamera del dispositivo per rilevare persone troppo vicine tra loro e avvisare con un segnale acustico. Questo strumento si basa sull'uso di modelli di machine learning per monitorare il distanziamento sociale.

## Funzionalità principali

- **Riconoscimento delle persone:** Utilizzo del modello pre-addestrato COCO-SSD per rilevare le persone nell'inquadratura.
- **Avviso sonoro:** Genera un segnale acustico quando due o più persone sono troppo vicine tra loro.
- **Visualizzazione in tempo reale:** Evidenzia le persone rilevate con riquadri, differenziando quelle che rispettano o violano il distanziamento sociale.

## Prova il progetto

Puoi eseguire direttamente il progetto cliccando sul seguente link:  
[**Esegui il progetto Distanziamento Sociale**](https://frank4barb.github.io/DistanziamentoSociale/)

## Installazione

1. Scarica o clona il repository.
2. Apri il file `index.html` in un browser che supporta l'accesso alla webcam (es. Chrome).
3. Concedi il permesso al browser per accedere alla webcam.

## Utilizzo

1. Apri il file `index.html` in un browser.
2. Fai clic sul pulsante "Enable Webcam" e consenti l'accesso alla webcam.
3. L'applicazione inizierà a rilevare le persone e ti avviserà con un beep se sono troppo vicine.

## Librerie utilizzate

- [TensorFlow.js](https://cdn.jsdelivr.net/npm/@tensorflow/tfjs/dist/tf.min.js): Per il supporto al machine learning e al rilevamento degli oggetti.
- [COCO-SSD](https://cdn.jsdelivr.net/npm/@tensorflow-models/coco-ssd): Modello di deep learning per il rilevamento degli oggetti.

## File principali

- **index.html:** La struttura della pagina web.
- **script.js:** La logica principale dell'applicazione, inclusa l'integrazione del modello COCO-SSD.
- **style.css:** Foglio di stile per la personalizzazione dell'aspetto.

## Note tecniche

- Per il rilevamento viene utilizzata la funzione `model.detect(video)` del modello COCO-SSD.
- La distanza tra le persone viene calcolata in base alle coordinate dei riquadri di rilevamento.
- L'applicazione è progettata per browser moderni compatibili con l'API `getUserMedia`.

## Limitazioni

- Il rilevamento dipende dalla qualità della videocamera e dall'illuminazione.
- Non garantisce una misurazione precisa delle distanze effettive (i calcoli si basano su pixel nell'immagine acquisita).

## Autore

Progetto ispirato e basato sulla guida ufficiale di TensorFlow.js per il rilevamento di oggetti: [Codelabs TensorFlow.js Object Detection](https://codelabs.developers.google.com/codelabs/tensorflowjs-object-detection#6).

---
Contribuisci o segnala problemi nel repository!
