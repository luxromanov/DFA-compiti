---
title: Geometria e algebra lineare
hide:
  - toc
---

Utilizza il **pannello di navigazione** sinistro per raggiungere il compito di tuo interesse oppure utilizza la **barra di ricerca**.

!!! warning

    Sito in costruzione. La versione web dei testi dei compiti potrebbe contenere errori derivanti dalla conversione automatica dei contenuti (vd. [Workflow di pubblicazione](#workflow-di-pubblicazione)). Se noti imprecisioni, per favore segnalale (vd. [Segnalazioni](#segnalazioni))

[Vai ai compiti :material-arrow-right:](2021-07-09.md){ .md-button }

## Come contribuire

Puoi contribuire al progetto fornendo gli **svolgimenti** in LaTeX dei problemi online o caricando nuovi **compiti**.

Le note dettagliate sul come fare sono disponbili [qui](../note).

[Contribuisci :material-arrow-right:](../note){ .md-button }

## Segnalazioni

Se dovessi trovare un errore o vuoi segnalare qualche problema, puoi [aprire una issue da qui](https://github.com/UNICT-DMI/DFA-compiti/issues/new). Grazie!

[Fai una segnalazione :material-arrow-right:](https://github.com/UNICT-DMI/DFA-compiti/issues/new){ .md-button }

## Workflow di pubblicazione

Immagini di input prelevate dal gruppo Telegram "Compiti DFA".

1. Utilizzando la utility `imagemagick` si è convertita la [foto del compito](images/2022-11-25.jpg) (`JPG`) in PDF
```shell
convert 2022-11-25.jpg 2022-11-25.pdf
```
1. Successivamente il PDF è stato convertito in LaTeX sfruttando il servizio [CLI di MathPix](https://mathpix.com/mpx-cli)
```shell
mpx convert 2022-11-25.pdf 2022-11-25.tex
```
1. infine si è ottenuto il file markdown (che fa da sorgente a queste pagine web) passando per [Pandoc](https://pandoc.org/)
```shell
pandoc -s -f latex -t markdown -o 2022-11-25.md 2022-11-25.tex
```

Il file di output è stato modificato manualmente per personalizzare l'intestazione e aggiungere i box relativi alle soluzioni e agli svolgimenti.
