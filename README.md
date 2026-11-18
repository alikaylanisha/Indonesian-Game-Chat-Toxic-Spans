## Toxic Spans Detection in Indonesian Game Chat using Named Entity Recognition and IndoBERT Model

A Research of toxic spans detection with Named Entity Recognition (NER) dataset derived and re-annotated from Indonesian Chat Dataset (https://www.kaggle.com/datasets/jprestiliano/indonesian-chat-dataset) on Kaggle.


## Repository Structure


├── DATA/	
│   ├── ALL_IOB_1.0.jsonl	
│   ├── ALL_IOB__encoded_1.0.jsonl	
│   ├── DATA_LICENSE                  	          # CDLA-Sharing-1.0 for derived data
│   ├── Neutral_IOB_1.0.jsonl	
│   └── Toxic_IOB_1.0.jsonl	
├── Data Processing/                             	# Notebooks for data curation
    ├── converting_ doccano to huggingface.ipynb	
│   └── eda.ipynb	
├── LICENSE                         	            # Code license (MIT)
├── model-training-toxic-span.ipynb	# Model training pipeline
├── requirements.txt  	                          # python dependencies for training
├── testing-grounds.ipynb	                        # Experimental notebook


## Overview

This repository contains an end-to-end Named Entity Recognition (NER) workflow designed to detect and analyze toxic spans in chat data. The project takes raw public chat datasets from Kaggle, curated and restructured the data into IOB formats.


The dataset in DATA/ is derived data created from a public dataset on Kaggle:

Original Dataset: Indonesia Chat Dataset
Original Author : Jasson Prestiliano, Azhari Azhari, Arif Nurwidyantoro
Original License: Community Data License Agreement – Sharing, Version 1.0 (CDLA-Sharing-1.0)

Summary of Modifications:

Sampling: Selected a curated subset of records rather than the full original dataset.
Schema Restructuring: Converted the original CSV of chat and category columns into IOB format in json
Re-annotation: Manually re-annotated the text spans to label specific named entities: [TOXIC]

Example:
{"tokens": ["gg", "main", "lo", "keren", "bro"], "ner_tags": ["O", "O", "O", "O", "O"]}

How to use:
Git clone : https://github.com/alikaylanisha/Indonesian-Game-Chat-Toxic-Spans.git

Licensing
	- Derived Data (DATA/): Distributed under the Community Data License Agreement – Sharing, Version 1.0 (CDLA-Sharing-1.0). See data/DATA_LICENSE or cdla.dev/sharing-1-0. Any downstream sharing or modification of this derived data must remain under CDLA-Sharing-1.0.
  - Source Code : Distributed under the MIT License. See LICENSE for details.
