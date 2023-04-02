# Meccanica analitica

!!! warning

    I contenuti pubblicati rappresentano dei test e non si assicura la correttezza delle soluzioni riportate.


## Workflow di pubblicazione

Essendo nella directory `docs/meccanica-analitica`, si converte il PDF del compito in LaTeX sfruttando il servizio [CLI di MathPix](https://mathpix.com/mpx-cli)

```
mpx convert pdf/2019-03-01-ts.pdf tex/2019-03-01-ts.tex
```

Segue la decompressione dell'archizio `.zip` di output

```
unzip tex/2019-03-01-ts.tex.zip
```

e infine si ottiene il file markdown (che fa da sorgente a queste pagine web) passando per [Pandoc](https://pandoc.org/)

```
pandoc -s -f latex -t markdown -o 2019-03-01.md tex/2019-03-01/ts.tex
```

Il file di output è stato modificato manualmente per personalizzare l'intestazione e aggiungere i box relativi alle soluzioni e agli svolgimenti.

## Segnalazioni

Se dovessi trovare un errore o vuoi segnalare qualche problema, puoi [aprire una issue da qui](https://github.com/UNICT-DMI/DFA-compiti/issues/new). Grazie!