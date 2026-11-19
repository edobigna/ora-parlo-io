# Ora parlo io

Una skill per Codex che personalizza il meme «ORA PARLO IO» usando la foto di una persona.

Sostituisce il soggetto a colori in primo piano e conserva il collage sullo sfondo, la cornice e lo stile della scritta. Il testo cambia soltanto se richiesto.

![Meme originale](assets/meme-originale.jpg)

## Installazione

Copia la cartella del repository in `~/.codex/skills/ora-parlo-io`, mantenendo insieme `SKILL.md` e `assets/`.

## Utilizzo

In una chat di Codex con lo strumento di modifica immagini disponibile, richiama `$ora-parlo-io` e allega la foto della persona da inserire.

Esempi:

- «Usa @ora-parlo-io con questa foto.»
- «Usa @ora-parlo-io con questa foto e cambia il testo in “ADESSO BASTA”.»
- «Usa @ora-parlo-io e cambia soltanto il testo in “TOCCA A ME”.»

La skill richiede lo strumento immagini integrato di Codex. Il risultato è una modifica generativa: la fedeltà al template e la resa del testo possono variare.

## Contenuto

- `SKILL.md`: istruzioni della skill.
- `assets/meme-originale.jpg`: immagine fissa di partenza.

L'immagine di partenza è stata fornita dall'utente; questo repository non ne dichiara la titolarità né concede una licenza sui diritti di terzi.
