---
title: Alcune note su questo spazio
hide:
    - navigation
---

## Come contribuire

Questo sito è basato su [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), un generatore di siti statici che rende facile pubblicare contenuti online a partire da file di testo markdown. L'intero progetto è disponibile su [GitHub](https://github.com/unict-dmi/DFA-compiti) (fai click sull'icona :simple-git: posizionata in alto a destra) ed è possibile contribuire (nelle modalità di seguito descritte) solo dopo aver creato un account; puoi farlo da [qui](https://github.com/signup). Grazie a chiunque contribuirà al progetto!

[Registrati a GitHub :material-arrow-right:](https://github.com/signup){ .md-button }


### Sono unə docente

Se sei unə docente, puoi:

1. effettuare il caricamento di un nuovo compito ([vai alla sezione](#voglio-caricare-un-nuovo-compito));
2. aggiungere le soluzioni di un compito esistente ([vai alla sezione](#voglio-aggiungere-delle-soluzioni));
3. modificare le soluzioni esistenti ([vai alla sezione](#voglio-modificare-delle-soluzioni));

Di seguito vengono aggiunti i dettagli per ognuna di queste eventualità. Puoi saltare da una sezione all'altra dall'indice posizionato sulla destra

#### Voglio caricare un nuovo compito

Ammettiamo che il tuo compito sia stato scritto in LaTeX e il file che lo contiene sia denominato `compito.tex`. Sarà necessario convertire il file LaTeX in markdown. Ci sono tanti modi per farlo; per esempio puoi usare uno dei tanti tool online su cui atterri dopo aver cercato "latex to markdown converter online". Se invece vuoi effettuare la conversione da terminale, sotto un approfondimento.

??? example "Conversione da terminale"
    Puoi effettuare la conversione anche da terminale e per farlo ci affideremo a [Pandoc](https://pandoc.org/), un'utility utilizzabile da linux. Se usi Windows, ti sarà utile lavorare con un terminale Linux e per farlo ti basterà seguire [questa guida di Microsoft](https://learn.microsoft.com/it-it/windows/wsl/install). 

    1. Installa Pandoc
    ```shell
    sudo apt-get install pandoc
    ```
    1. Converti il tuo compito da LaTeX a markdown
    ```shell
    pandoc -s -f latex -t markdown -o compito.md compito.tex
    ```

!!! warning
    Se il tuo documento contiene delle immagini, assicurati che queste siano posizionate in una cartella denominata `images/`. Il tuo documento markdown conterrà allora delle espressioni del tipo
    ```markdown title="compito.md"
    Sotto si allega un'immagine

    ![](images/img-1.png)
    ```

Ottimo, adesso siamo prontə per caricare il nuovo compito su GitHub.

!!! tip 
    Prima di effettuare il caricamento del file su GiHub, potresti rinominare il file `compito.md` in `YYYY-MM-DD.md` ovvero anno-mese-giorno del compito.

1. Fai click sull'icona di Git (:simple-git:{.default-icon-color}) posizionata in alto a destra di questa pagina (ed effettua il login al tuo account GitHub facendo click su [Sign in](https://github.com/login) nel caso in cui non fossi loggatə);
1. Si aprirà una pagina dalla quale potrai accedere a tutti i file di questo sito.
    - Fai click sulla cartella :material-folder:{.default-icon-color} *docs* e poi dirigiti nella cartella della materia per cui vuoi caricare il compito.
    - Fai click su **`Add file`** e poi su **`Upload files`**. Adesso puoi trascinare il tuo `YYYY-MM-DD.md` nell'apposita finestra oppure potrai fare click su **`choose your files`** per aprire il tuo file explorer.
    - Dopo aver trascinato il file `YYYY-MM-DD.md` oppure averlo selezionato dal file explorer, aggiungi una descrizione (facoltativa), fai click su :octicons-git-pull-request-16:{.default-icon-color} `Create a new branch for this` e poi su **`Propose changes`**
1. Se il tuo compito contiene delle immagini, ripeti la stessa procedura del punto precedente posizonandoti però nella cartella `materia-scelta/images` ad esempio `geometria/images`.

!!! tip
    Se vuoi, puoi anche effettuare il caricamento del codice sorgente LaTeX e del testo del compito in formato PDF.

Una persona che mantiene il progetto riceverà le tue modifiche e le pubblicherà il prima possibile. Grazie!

!!! example "GitHub"
    Se vuoi evitare di seguire la procedura tramite la versione web di GitHub puoi comunque ottenere lo stesso risultato utilizzando [GitHub Desktop](https://desktop.github.com/) oppure il [terminale](https://git-scm.com/downloads).


#### Voglio aggiungere delle soluzioni

1. Individua il compito per cui vuoi aggiungere le soluzioni semplicemente navigando il sito;
1. fai click sul pulsante di modifica che trovi in ogni pagina in alto a destra (:material-file-edit-outline:);
1. individua lo spazio che è stato predisposto per le *soluzioni* e per lo *svolgimento* che sarà del tipo:
```markdown title="2021-08-09.md"
??? success "Visualizza le soluzioni"
    {bla % bla include-markdown bla "../placeholder/soluzioni.md" bla % bla}

??? note "Visualizza lo svolgimento"
    {bla % bla include-markdown bla "../placeholder/svolgimento.md" bla % bla}
```
1. rimuovi il testo tra parentesi graffe e aggiungi le tue soluzioni scrivendo in LaTeX tra dollari. Sotto un esempio:
```markdown title="2021-08-09.md"
??? success "Visualizza le soluzioni"
    - $F_1 = 1 \; N$
    - $F_2 = 2 \; N$
    - $F_3 = 3 \; N$

??? note "Visualizza lo svolgimento"
    Per determinare bla bla, è sufficiente sfruttare il teorema bla bla

    - $F_1 = m a_1$
    - $F_2 = m a_2$
    - $F_3 = m a_3$
```
L'output sarà il seguente:

    ??? success "Visualizza le soluzioni"
        - $F_1 = 1 \; N$
        - $F_2 = 2 \; N$
        - $F_3 = 3 \; N$

    ??? note "Visualizza lo svolgimento"
        Per determinare bla bla, è sufficiente sfruttare il teorema bla bla

        - $F_1 = m a_1$
        - $F_2 = m a_2$
        - $F_3 = m a_3$
1. fornisci una descrizione (facoltativa);
1. fai click su :octicons-git-pull-request-16:{.default-icon-color} `Create a new branch for this` e poi su **`Propose changes`**

#### Voglio modificare delle soluzioni

1. Individua il compito per cui vuoi modificare le soluzioni semplicemente navigando il sito;
1. fai click sul pulsante di modifica che trovi in ogni pagina in alto a destra (:material-file-edit-outline:);
1. individua lo spazio che è stato predisposto per le *soluzioni* e per lo *svolgimento* che sarà del tipo:
```markdown title="2021-08-09.md"
??? success "Visualizza le soluzioni"
    - $F_1 = 1 \; N$
    - $F_2 = 2 \; N$
    - $F_3 = 3 \; N$

??? note "Visualizza lo svolgimento"
    Per determinare bla bla, è sufficiente sfruttare il teorema bla bla

    - $F_1 = m a_1$
    - $F_2 = m a_2$
    - $F_3 = m a_3$
```
1. effettua le tue modifiche;
1. fornisci una descrizione (facoltativa);
1. fai click su :octicons-git-pull-request-16:{.default-icon-color} `Create a new branch for this` e poi su **`Propose changes`**.

Una persona che mantiene il progetto riceverà le tue modifiche e le pubblicherà il prima possibile. Grazie!

### Sono unə studentə

Puoi:

1. Caricare un nuovo compito ([vai alla sezione](#voglio-caricare-un-nuovo-compito-1));
2. aggiungere le soluzioni di un compito esistente ([vai alla sezione](#voglio-aggiungere-delle-soluzioni));
3. modificare le soluzioni esistenti ([vai alla sezione](#voglio-modificare-delle-soluzioni));

#### Voglio caricare un nuovo compito

Se sei unə studentə, la procedura per caricare un nuovo compito è un po' più macchinosa rispetto a quella per ə docenti in quanto spesso non si ha a disposizione il codice sorgente LaTeX. La nostra materia prima saranno file PDF o peggio, immagini dei compiti scritti (vd. Gruppo Telegram "Compiti DFA").

Immaginiamo di avere un'immagine di un compito denominata `compito.jpg`. Armiamoci di terminale e iniziamo a convertire un paio di documenti per alimentare l'archivio.  

1. Installa  la utility `imagemagick` (che sarà utile per convertire `JPG` in `PDF`) lanciando
```shell
sudo apt update
sudo apt install imagemagick
```
1. Utilizza `imagemagick` per convertire la foto del compito (`JPG`) in `PDF`
```
convert compito.jpg compito.pdf
```
1. Registrati a [MathPix](https://mathpix.com) (se utilizzi l'account universitario potrai accedere gratuitamente all'educational plan che offre più vantaggi rispetto a quello basic).
1. Installa il servizio [CLI di MathPix](https://mathpix.com/mpx-cli)
```shell
sudo apt install npm
sudo npm install -g @mathpix/mpx-cli
```
1. Converti il PDF in LaTeX sfruttando MathPix
```
mpx convert compito.pdf compito.tex
```
1. Installa [Pandoc](https://pandoc.org/)
```shell
sudo apt-get install pandoc
```
1. Ottieni il file markdown (che fa da sorgente a queste pagine web) passando per Pandoc
```
pandoc -s -f latex -t markdown -o compito.md compito.tex
```

!!! example "Tool"
    Se vuoi lanciare tutti i comandi precedenti scrivendo **una sola riga** da terminale, puoi usare il tool [`tomkd`](https://github.com/dennisangemi/tomkd) ([leggi qui](https://github.com/dennisangemi/tomkd#set-up) se vuoi installarlo).<br>Essendo posizionati nella cartella `analisi-2`, ad esempio, possiamo convertire un compito di *Analisi 2* semplicemente lanciando:
    ```bash
    tomkd -i pdf/to_be_converted/3dicembre2018.pdf -o 2018-12-03.md -t "Giuseppa Rita Cirmi"
    ```
    in cui:

    - con `-i` si indica il file di input (`pdf/to_be_converted/3dicembre2018.pdf`);
    - con `-o` si indica il file di output (`2018-12-03.md`);
    - con `-i` il tag che in questo caso coincide con il nome e il cognome del/la docente che ha somminisrato il compito.

    Verrà generato automaticamente il file `2018-12-03.md` e, se presenti, verranno estratte anche tutte le immagini incluse nel documento `pdf` di input organizzandole appositamente in una directory `images/`.

Arrivatə a questo punto, puoi seguire la procedura per caricare il file markdown (con le eventuali immagini) su GitHub seguendo gli stessi step dellə docenti ([vedi step](#voglio-caricare-un-nuovo-compito)).

#### Voglio aggiungere delle soluzioni
[Leggi qui :material-arrow-right:](#voglio-aggiungere-delle-soluzioni){ .md-button }

#### Voglio modificare delle soluzioni
[Leggi qui :material-arrow-right:](#voglio-modificare-delle-soluzioni){ .md-button }

## Segnalazioni

Se dovessi trovare un **errore** o vuoi segnalare qualche problema, puoi [aprire una issue da qui](https://github.com/UNICT-DMI/DFA-compiti/issues/new). Grazie!

[Fai una segnalazione :material-arrow-right:](https://github.com/UNICT-DMI/DFA-compiti/issues/new){ .md-button }

## Credits
Questo sito è mantenuto da [Dennis Angemi](https://twitter.com/DennisAngemi) che lo ha costruito con il supporto della community [Open Data Sicilia](https://opendatasicilia.it) (qui un [boilerplate](https://github.com/opendatasicilia/ods-mkdocs-material)). Sentiti liberə di contribuire!
