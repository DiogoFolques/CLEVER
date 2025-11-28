## CLEVER
Repository for the paper CLEVER: Portuguese Dataset for Claim Detection and Verification in Election News

## Overview

We introduce CLEVER, a dataset of European Portuguese news articles annotated for factual claims and their assessed veracity. Comprising 228 articles and 1185 individual annotations. Unlike most existing resources based on social media or parliamentary transcripts, CLEVER focuses on journalistic content, collected through a partnership with LUSA, the Portuguese News Agency. To ensure annotation quality, two trained annotators labeled each article, with a curator validating all annotations according to a newly proposed scheme. Afterwards, each claimed was verified in it's veracity, while providing the sources on the veredict sources. By releasing CLEVER, we aim to advance research on low-resource fact-checking and enhance understanding of misinformation in news media.


## Repository Structure
``` 
├── dataset_sample/
│ ├── annotations.jsonl
│ ├── annotations.pretty.json
│ ├── news_articles/
│ │ └── *.txt
├── CLEVER Verification Manual.pdf
├── LICENSE
└── README.md

```
---
## Corpus Statistics

| Property | Description |
|-----------|--------------|
| **Total Documents** | 228 |
| **Average Length** | 483.4 words per document |
| **Total Claims** | 115 |
| **Total Non-Claims** | 1,072 |

---

## Data Format


The **ClaimPT** dataset is provided in **JSONL** format, where each line corresponds to an annotated span.  

| Field | Description |
|--------|-------------|
| `document` | News article filename |
| `news_article_topic` | Topic of the news article |
| `publication_time` | Date of the news publication |
| `claim` | Boolean indicating whether the annotation is a claim (`true`) or non-claim (`false`) |
| `begin_character` | Begin character offset of the annotated text span |
| `end_character` | End character offset of the annotated text span |
| `text_segment` | Text segment corresponding to the annotated span |
| `claim_topic` | Topic of the news article (e.g., politics, environment, health) |
| `claim_span` | Object containing `text`, `begin`, and `end` positions of the claim span |
| `claim_object` | Text and character offsets of the claim’s object  |
| `claimer` | Text and offsets of the entity making the claim |
| `time` | Temporal expression associated with the claim |
| `id` | Unique identifier for each claim or non-claim |

---

## Example (JSON excerpt)


```json
[
    {
    "document": "news_0004.txt",
    "news_article_topic": "politics",
    "publication_time": "05 mai 2025",
    "items": [
      {
        "claim": true,
        "begin_character": 664,
        "end_character": 746,
        "text_segment": "Eu lembro que Cavaco Silva, 13 dias antes de o BES cair, disse que estava tudo bem",
        "claim_topic": "politics",
        "claim_span": {
          "text": "Cavaco Silva, 13 dias antes de o BES cair, disse que estava tudo bem",
          "begin": 678,
          "end": 746
        },
        "claim_object": {
          "text": "disse que estava tudo bem",
          "begin": 721,
          "end": 746
        },
        "claimer": [
          {
            "text": "O líder do PS",
            "begin": 138,
            "end": 151
          },
          {
            "text": "Pedro Nuno Santos",
            "begin": 409,
            "end": 426
          }
        ],
        "time": {
          "text": "hoje",
          "begin": 161,
          "end": 165
        },
        "id": "news_0004_c1"
      },
      {
        "claim": false,
        "begin_character": 1067,
        "end_character": 1116,
        "text_segment": "eu sou genuíno, eu sou aquilo que as pessoas veem",
        "id": "news_0004_c2"
      },
      {
        "claim": false,
        "begin_character": 1118,
        "end_character": 1139,
        "text_segment": "Luís Montenegro não é",
        "id": "news_0004_c3"
      },
      {
        "claim": false,
        "begin_character": 1143,
        "end_character": 1296,
        "text_segment": "[Estas acusações são] de um homem que não está de forma séria na política, que está habituado a mentir e a enganar as pessoas e acha que são todos iguais",
        "id": "news_0004_c4"
      },
      {
        "claim": false,
        "begin_character": 1298,
        "end_character": 1353,
        "text_segment": "Eu não engano ninguém, eu sou genuíno, sou transparente",
        "id": "news_0004_c5"
      }
    ]
  },
]
```
---

## Annotation Guidelines

Detailed annotation instructions, including procedures, quality-control measures, and schema definitions, are available in the document:

📄 [CLEVER Verification Manual (PDF)]()

This manual describes:

* The annotation process and methodology
* The annotation scheme and entity structures
* The definition of a claim
* Metadata and label taxonomy
* Examples and boundary cases
* The verification process and methodology

Researchers interested in replicating the annotation or training models should refer to this guide.

---

## Dataset Access

### Sample Dataset

A sample subset (20 annotated articles) is included in the repository under the dataset_sample/ directory

### Full Dataset

The complete dataset (228 articles) will be made available once the research paper is published.


