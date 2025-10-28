## CLEVER
Repository for the paper CLEVER: Portuguese Dataset for Claim Detection and Verification in Election News

## Overview

We introduce CLEVER, a dataset of European Portuguese news articles annotated for factual claims and their assessed veracity. Comprising 228 articles and xxx individual annotations. Unlike most existing resources based on social media or parliamentary transcripts, CLEVER focuses on journalistic content, collected through a partnership with LUSA, the Portuguese News Agency. To ensure annotation quality, two trained annotators labeled each article, with a curator validating all annotations according to a newly proposed scheme. Afterwards, each claimed was verified in it's veracity, while providing the sources on the veredict sources. By releasing CLEVER, we aim to advance research on low-resource fact-checking and enhance understanding of misinformation in news media.


## Repository Structure
``` 
├── dataset_sample/
│ ├── annotations.jsonl
│ ├── annotations.pretty.json
│ ├── news_articles/
│ │ └── *.txt
├── Annotation_Guidelines.pdf
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
| `publication_time` | Date of the news publication |
| `claim` | Boolean indicating whether the annotation is a claim (`true`) or non-claim (`false`) |
| `begin_character` | Begin character offset of the annotated text span |
| `end_character` | End character offset of the annotated text span |
| `text_segment` | Text segment corresponding to the annotated span |
| `claim_topic` | Topic of the news article (e.g., politics, environment, health) |
| `claim_span` | Object containing `text`, `begin`, and `end` positions of the claim span |
| `claim_object` | Text and character offsets of the claim’s object  |
| `claimer` | Text and offsets of the entity making the claim |
| `Time` | Temporal expression associated with the claim |

---

## Example (JSON excerpt)


```json
[
  {
    "document": "input_part008.txt",
    "publication_time": "04 dez 2023",
    "claim": true,
    "begin_character": 501,
    "end_character": 685,
    "text_segment": "foi convidado para aderir não pelo lado monárquico, no qual, aliás, não insistiam muito, mas por se empenhar, acima de tudo, na defesa do ambiente e na preservação da qualidade de vida",
    "claim_topic": "politics",
    "claim_span": {
      "text": "foi convidado para aderir não pelo lado monárquico, no qual, aliás, não insistiam muito, mas por se empenhar, acima de tudo, na defesa do ambiente e na preservação da qualidade de vida",
      "begin": 501,
      "end": 685
    },
    "claim_object": {
      "text": "por se empenhar, acima de tudo, na defesa do ambiente",
      "begin": 594,
      "end": 647
    },
    "claimer": {
      "text": "Pinto Balsemão",
      "begin": 438,
      "end": 452
    },
    "Time": ""
  }
]
```
---

## Annotation Guidelines

Detailed annotation instructions, including procedures, quality-control measures, and schema definitions, are available in the document:

📄 [Annotation Manual (PDF)](https://github.com/LIAAD//blob/main/ClaimPT%20Annotation%20Manual.pdf)

This manual describes:

* The annotation process and methodology
* The annotation scheme and entity structures
* The definition of a claim
* Metadata and label taxonomy
* Examples and boundary cases

Researchers interested in replicating the annotation or training models should refer to this guide.

---

## Dataset Access

### Sample Dataset

A sample subset (20 annotated articles) is included in the repository under the dataset_sample/ directory

### Full Dataset

The complete dataset (1,308 articles) is protected by a **Data Use Agreement** and will be made available through the following DOI once the research paper is published:



Please visit the DOI link for access details and usage terms.


Dataset Access

