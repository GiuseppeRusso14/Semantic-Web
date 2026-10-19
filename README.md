# EtnaOnto

Ontologia OWL 2 con regole SWRL per il monitoraggio sismico e vulcanico dell'Etna.

Progetto per l'esame di **Semantic Web**, Corso di laurea magistrale in Informatica, Università degli Studi di Catania (a.a. 2026/27, prof.ssa Marianna Nicolosi Asmundo).

Autore: Giuseppe Russo

## Obiettivo

L'ontologia integra in un'unica base di conoscenza dati reali sull'Etna:

- il catalogo dei terremoti dell'area etnea (INGV);
- la rete di stazioni sismiche che li registra (INGV);
- gli episodi eruttivi documentati nei comunicati dell'INGV – Osservatorio Etneo.

Su questi dati il reasoner classifica i terremoti per magnitudo e profondità, li localizza nei comuni, li collega agli episodi eruttivi in corso e ne individua le sequenze. L'ontologia riusa SOSA/SSN e OWL-Time del W3C.

## Struttura

| Cartella | Contenuto |
|---|---|
| `ontologia/` | ontologia (TBox e regole SWRL) e individui |
| `dati/` | dati scaricati dai servizi web INGV (`grezzi/`) ed episodi eruttivi con le fonti |
| `script/` | download dei dati e conversione in Turtle |
| `query/` | query SPARQL e relativi risultati |
| `figure/` | diagrammi e schermate di Protégé |
| `relazione/` | relazione (sorgenti LaTeX e PDF) |
| `slide/` | slide della discussione |

## Strumenti

- Protégé 5.6, con i reasoner HermiT e Pellet e il plugin SWRLTab
- Python 3.9 o successivo, solo per scaricare e convertire i dati:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Stato

In sviluppo.
