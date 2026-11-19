---
name: ora-parlo-io
description: Personalizza il meme fisso «Ora parlo io» sostituendone il soggetto con la persona di una foto fornita dall'utente e, solo su richiesta, cambiandone il testo.
---

# Ora parlo io

Usa sempre [assets/meme-originale.jpg](assets/meme-originale.jpg) di questa skill come immagine di partenza. Risolvi il percorso relativamente alla posizione di questo SKILL.md, non alla cartella di lavoro della chat. Non usare una variante già generata come nuova base, salvo richiesta esplicita dell'utente.

Il template è un'immagine orizzontale 1280 × 720: una persona a colori in primo piano, un collage scuro in bianco e nero sullo sfondo, una cornice con angoli arrotondati e la scritta «ORA PARLO IO» in basso. Sostituisci soltanto la persona a colori in primo piano; conserva le persone del collage sullo sfondo, salvo richiesta esplicita diversa. Mantieni il taglio a mezzo busto e la sovrapposizione della scritta davanti al soggetto. La scritta deve restare in maiuscolo, bianca e grigia, inclinata, con contorno e ombra come nell'originale; il testo predefinito da rendere è esattamente «ORA PARLO IO».

## Input

- Meme originale in `assets/meme-originale.jpg`. Se manca, chiedi di allegarlo e fermati prima di generare: non inventare o ricostruire il template.
- Foto della persona da inserire. Se manca e l'utente chiede di sostituire il soggetto, chiedi la foto. Se contiene più persone e il soggetto non è chiaro, chiedi quale usare.
- Testo facoltativo. Mantieni esattamente «ORA PARLO IO» se l'utente non chiede una modifica. Se chiede di cambiarlo senza indicare la nuova frase, chiedi quale frase usare. Non tradurre o riscrivere il testo fornito; usa le maiuscole per coerenza grafica salvo diversa indicazione esplicita.

È possibile cambiare solo il testo senza richiedere una foto, oppure cambiare il soggetto mantenendo il testo originale.

## Modifica

1. Osserva il meme originale e la foto fornita. Per immagini locali usa `view_image` prima di modificarle.
2. Usa lo strumento integrato `image_gen` per modificare il meme, specificando il ruolo di ogni immagine: il meme è il bersaglio della modifica; la foto è il riferimento per l'identità della persona.
3. Se tutte le immagini hanno un percorso locale, passale tramite `referenced_image_paths`. Altrimenti rendi visibile anche il meme locale con `view_image` e usa `num_last_images_to_include` con il minimo numero che includa tutti i riferimenti. Non usare i due parametri insieme. Se non è possibile includere tutti gli input, chiedi di riallegare quello mancante.
4. Sostituisci il soggetto del meme con la persona della foto, conservandone i tratti riconoscibili. Adatta la persona alla posa, alla prospettiva e al trattamento visivo del meme. Mantieni sfondo, composizione, inquadratura, proporzioni e gli altri elementi del template quanto più fedeli possibile. Non limitarti a incollare la foto come un riquadro.
5. Mantieni la scritta originale salvo modifica richiesta. Per una nuova frase, conserva posizione e stile tipografico del meme, adattando dimensione e a capo per renderla leggibile senza tagli.
6. Restituisci una variante per richiesta, salvo diverso numero indicato dall'utente. Non sovrascrivere mai il meme nella skill.

Nel prompt di modifica indica esplicitamente il testo finale tra virgolette, la persona da inserire e gli elementi del meme da conservare. Non aggiungere decorazioni, scritte o persone non richieste.

Controlla, quando l'output è ispezionabile, che identità, composizione e testo corrispondano alla richiesta; correggi eventuali errori evidenti con una modifica mirata. Mostra il risultato direttamente nella chat usando il meccanismo di restituzione dello strumento immagini. Non dichiarare una corrispondenza perfetta o una verifica che non hai potuto effettuare.
