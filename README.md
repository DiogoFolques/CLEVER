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
| **Total Documents** | 1,308 |
| **Average Length** | 542.8 words per document |
| **Total Claims** | 463 |
| **Total Non-Claims** | 4,393 |

Data Format

Example (JSON excerpt)

Annotation Guidelines

Dataset Access

