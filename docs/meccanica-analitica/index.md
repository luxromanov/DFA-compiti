---
title: Meccanica analitica
hide:
  - toc
---

Utilizza il **pannello di navigazione** sinistro per raggiungere il compito di tuo interesse oppure utilizza la **barra di ricerca**.

!!! warning

    La versione web dei testi dei compiti potrebbe contenere errori derivanti dalla conversione automatica dei contenuti (vd. [Workflow di pubblicazione](#workflow-di-pubblicazione)). Se noti imprecisioni, per favore segnalale (vd. [Segnalazioni](#segnalazioni))

[Vai ai compiti :material-arrow-right:](2013-06-13.md){ .md-button }

## Ringraziamenti

Si ringrazia il prof. [Massimo Trovato](https://www.dmi.unict.it/trovato/) per aver concesso la pubblicazione dei testi dei compiti di **Meccanica Analitica**.

È possibile raggiungere alcuni testi anche dal suo sito tramite il seguente bottone

[:fontawesome-regular-file-pdf: Download](https://www.dmi.unict.it/trovato/Testi_compiti.pdf){ .md-button }

## Come contribuire

Puoi contribuire al progetto fornendo gli **svolgimenti** in LaTeX dei problemi online o caricando nuovi compiti.

Le note dettagliate sul come fare sono disponbili [qui](../note). Di seguito un piccolo riassunto:

1. Crea un account GitHub (puoi farlo da [qui](https://github.com/signup));
2. fai click sul pulsante di modifica che trovi in ogni pagina in alto a destra (:material-file-edit-outline:);
3. apporta le tue modifiche inserendo il _LaTeX_ tra dollari (`$F=ma$`);
4. segui le istruzioni per effettuare una "Pull Request"

## Segnalazioni

Se dovessi trovare un **errore** o vuoi segnalare qualche problema, puoi [aprire una issue da qui](https://github.com/UNICT-DMI/DFA-compiti/issues/new). Grazie!

[Fai una segnalazione :material-arrow-right:](https://github.com/UNICT-DMI/DFA-compiti/issues/new){ .md-button }

## Workflow di pubblicazione

Di seguito qualche nota sulla costruzione di questo **spazio**.

1. Si è effettuata conversione da PDF a LaTeX sfruttando il servizio [CLI di MathPix](https://mathpix.com/mpx-cli)
```
mpx convert compito.pdf compito.tex
```

2. Successivamente è stato decompresso l'archivio `.zip` che il comando precedente produce 
```
unzip compito.tex.zip
```

3. Infine è stato ottenuto il file markdown (che fa da sorgente a queste pagine web) passando per [Pandoc](https://pandoc.org/)
```
pandoc -s -f latex -t markdown -o compito.md compito.tex
```

I file di output sono stati modificati manualmente per personalizzare l'intestazione e aggiungere i box relativi alle soluzioni e agli svolgimenti.