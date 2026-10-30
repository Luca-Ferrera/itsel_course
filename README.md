# Laboratorio Data & AI — Piano B

Questo progetto crea un ambiente JupyterLite: un piccolo laboratorio di dati e intelligenza artificiale che funziona direttamente nel browser, senza installare programmi. È pensato come ambiente di riserva per studenti adulti principianti di un istituto tecnico.

Link per gli studenti:

| Notebook | Google Colab (account Google) | JupyterLite (nessun account) |
|---|---|---|
| 01 – Esplorazione dati | [![Apri in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Luca-Ferrera/itsel_course/blob/main/content/01_esempio_esplorazione_dati.ipynb) | [![Apri in JupyterLite](https://jupyterlite.rtfd.io/en/latest/_static/badge.svg)](https://luca-ferrera.github.io/itsel_course/lab/index.html?path=01_esempio_esplorazione_dati.ipynb) |

In Colab, prima di modificare il notebook, scegliere **File → Salva una copia in Drive**.

## Preparazione per il docente

1. Creare un repository **pubblico** su GitHub e caricare questi file nel ramo `main`.
2. In GitHub aprire **Settings → Pages** e, in **Source**, scegliere **GitHub Actions**.
3. Attendere la conclusione dell'azione nella scheda **Actions**.
4. Aprire il link per gli studenti indicato qui sopra.

Per aggiungere materiali, mettere notebook e dati nella cartella `content/`, poi eseguire il push: l'azione ricostruirà il sito.

## Anteprima locale

Per costruire il sito in locale:

```bash
source .venv/bin/activate
jupyter lite build --contents content --output-dir dist
```

Per servirlo localmente dopo la compilazione:

```bash
python -m http.server 8000 --directory dist
```

Poi aprire <http://localhost:8000/lab/index.html?path=01_esempio_esplorazione_dati.ipynb>.

## Indicazioni per gli studenti

1. Aprire il link del laboratorio e attendere il primo caricamento: può richiedere circa 30–60 secondi.
2. Eseguire una cella con **Shift+Invio**.
3. Al termine scaricare il proprio lavoro dal menu **File → Scarica / Download**.

Il lavoro resta nel browser: cancellare i dati del browser può eliminare file e modifiche locali. Per questo è importante scaricare il notebook alla fine.

## Fonte dei dati

Il notebook usa i dati nazionali COVID-19 del **Dipartimento della Protezione Civile**, distribuiti con licenza [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/deed.it). Dettagli e collegamenti sono in `content/data/FONTE.md`.
