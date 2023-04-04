---
title: Geometria e algebra lineare
hide:
  - toc
---

!!! warning

    I contenuti pubblicati rappresentano dei test e non si assicura la correttezza delle soluzioni riportate.

Attualmente è presente il solo [compito del 25 novembre 2022](2022-11-25.md) (test).

## Workflow di pubblicazione

[Immagine di input](https://t.me/c/1739191444/266) prelevata dal gruppo Telegram "Compiti DFA".

Utilizzando la utility `imagemagick` si è convertita la [foto del compito](img/2022-11-25.jpg) (`JPG`) in PDF

```
convert 2022-11-25.jpg 2022-11-25.pdf
```

Successivamente il PDF è stato convertito in LaTeX sfruttando il servizio [CLI di MathPix](https://mathpix.com/mpx-cli)


```
mpx convert 2022-11-25.pdf 2022-11-25.tex
```

e infine si ottiene il file markdown (che fa da sorgente a queste pagine web) passando per [Pandoc](https://pandoc.org/)

```
pandoc -s -f latex -t markdown -o 2022-11-25.md 2022-11-25.tex
```

Il file di output è stato modificato manualmente per personalizzare l'intestazione e aggiungere i box relativi alle soluzioni e agli svolgimenti.

## Segnalazioni

Se dovessi trovare un errore o vuoi segnalare qualche problema, puoi [aprire una issue da qui](https://github.com/UNICT-DMI/DFA-compiti/issues/new). Grazie!
