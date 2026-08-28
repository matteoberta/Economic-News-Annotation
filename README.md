# Economic News Annotation

Dataset release accompanying:

> **From Experts to Open-Weight Models: a Validated LLM Pipeline for Institutional Economic News Annotation**
> Michele Petrocelli, Andrea Rollin, Matteo Berta, Francesca Zafonte, Simone Monaco, Daniele Apiletti, Tania Cerquitelli
> *EMNLP 2026, Industry Track*

This repository accompanies the paper above, which introduces a human-annotated dataset of Italian economic news labeled by domain experts for **sentiment** and **topic**, and a statistically validated pipeline for scaling those labels with large language models. This repository releases a sample of the resulting annotations.

## What's in this repository

A sample of the annotated dataset, containing:

| Field | Description |
|---|---|
| `article_id` | Article identifier on the Factiva database |
| `publication` | Source publication |
| `publication_date` | Publication date |
| `sentiment` | Sentiment score, 1–5 ordinal scale (0.5 increments); 1 = very negative, 5 = very positive |
| `topic` | Dominant topic category (see below) |

### Topic categories

Each article is assigned a single dominant topic from six mutually exclusive categories:

- Monetary Policy and Central Banks
- Fiscal Policies and Taxes
- Financial Markets
- Geopolitics and Social Impact
- Inflation and Prices
- Labour Market

## What's *not* included

**Raw article text is not released.** The corpus was collected through the Factiva database, whose licensing terms prohibit redistribution of full-text content. The `factiva_id` field is provided so that researchers with their own Factiva access can retrieve the original articles.

Annotation guidelines, prompting templates, and training/LoRA configurations used in the pipeline are documented in the paper's appendices rather than released as separate files in this repository.

## License

This dataset is released under [**CC BY-NC-SA 4.0**](https://creativecommons.org/licenses/by-nc-sa/4.0/) (Attribution–NonCommercial–ShareAlike). You are free to share and adapt the material for non-commercial purposes, provided you give appropriate credit and distribute any derivative works under the same license.

## Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{petrocelli-etal-2026-from-experts,
    title = "From Experts to Open-Weight Models: a Validated {LLM} Pipeline for Institutional Economic News Annotation",
    author = "Petrocelli, Michele  and
      Rollin, Andrea  and
      Berta, Matteo  and
      Zafonte, Francesca  and
      Monaco, Simone  and
      Apiletti, Daniele  and
      Cerquitelli, Tania",
    editor = "TODO",
    booktitle = "Proceedings of the 2026 Conference on Empirical Methods in Natural Language Processing: Industry Track",
    month = oct,
    year = "2026",
    address = "Budapest, Hungary",
    publisher = "Association for Computational Linguistics",
    url = "TODO",
    doi = "TODO",
    pages = "TODO",
    ISBN = "TODO"
}
```

## Contact

For questions about the dataset, please contact the corresponding author: `matteo.berta@polito.it`.
