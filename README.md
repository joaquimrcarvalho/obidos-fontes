#  Óbidos


## Directory layout

```
├── database
│   ├── backups        backups of the project database
│   └── sqlite         SQLite database files
├── etc
│   └── doc            pointers to the ongoing documentation
├── extras             auxiliary project files: working documents, scripts,
│                      downloaded material and derived data
├── identifications    exports of the identification (record linking) process
├── inferences         inference rules used when processing the source files
├── mappings           mappings between Kleio groups and database tables
├── notebooks          Jupyter notebooks for working with the project data
├── sources            source files in Kleio notation (.cli, .kleio)
├── structures         structure files describing the internal structure of each
│                      type of source
└── .timelink-project  marker file: identifies this directory as a Timelink project
```

The core directories (`database`, `extras`, `inferences`, `notebooks`, `sources`,
`structures`) follow the single-project `timelink-home` layout. `etc`,
`identifications` and `mappings` are additional directories used by the Kleio
server and by the record-linking workflow.

See the [Timelink documentation](https://time-link.github.io/timelink-docs/) for details.

## What is Timelink?

Timelink, formerly known as MHK (Micro History with Kleio) is an information system designed for processing person related information collected from historical sources.

Timelink provides:

* a notation (kleio) for textual transcription of historical sources, capable of capturing complex information about people and their relations in any type of historical documents.
* a text processor that extracts information from the kleio transcriptions, infers personal attributes and relations from agent roles in historical events and generates data in formats suitable for database import.
* a database management system capable of processing time varying attributes and relations, assist in reconstructing biographies and networks from fragmentary information.

Timelink is open source MIT License software available at http://github.com/joaquimrcarvalho/timelink

## Source collections included in this repository

Parish and notarial records of Óbidos (Portugal), transcribed in Kleio
notation with the `gacto.str` structure: 462 source files (`.cli`) with
27,886 acts in all (16,347 baptisms, 2,640 marriages, 8,829 deaths and 70
notarial deeds) and more than 100,000 person entries, covering 1538–1800.
All files are UTF-8 encoded.

### Parish records (`sources/paroquiais`)

Baptisms, marriages and deaths of five parishes. Each parish has its own
subdirectory with `Baptismos`, `Casamentos` and `Óbitos` folders:

| Parish | Baptisms | Marriages | Deaths |
|---|---|---|---|
| Santa Maria (`santamaria`) | 6,206 (1562–1800) | 1,175 (1566–1800) | 3,705 (1562–1800) |
| São João (`sjoao`) | 4,858 (1556–1800) | 699 (1541–1800) | 3,220 (1538–1800) |
| São Pedro (`spedro`) | 3,279 (1654–1800) | 92 (1784–1800) | 721 (1765–1800) |
| São Tiago (`stiago`) | 2,004 (1600–1800) | 596 (1599–1800) | 831 (1599–1800) |
| Nossa Senhora da Piedade, Vau (`vau`) | — | 78 (1748–1800) | 352 (1747–1800) |

Known gaps: São Tiago has no baptisms for 1643–1685 and no marriages for
1644–1695; the São Pedro marriage and death books start much later than
the baptism book (1784 and 1765); Vau has no baptism books. File names
follow parish-specific conventions (e.g. `santamaria-1798-1800.cli`,
`SJ-cas1791-1800.cli`, `ST-c1793-1800.cli`).

### Notarial records (`sources/notariais`)

Notarial deeds (*escrituras*) of João Ferreira da Serra, notary of Óbidos,
for 1704 and 1705 (2 files, 70 deeds): mostly loans at interest (*dinheiro
a juro*), registering creditor, debtors and their spouses, the amount
lent, and the property given as guarantee with its confrontations
(boundaries).

## License

Timelink software is distributed under a MIT license that includes usage for commercial purposes.

Kleio transcriptions of historical sources are not distributed under the same license.

Each Kleio transcription file is copyright of the person or persons that produced the transcription.
