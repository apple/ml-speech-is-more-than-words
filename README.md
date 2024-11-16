# ContraProST

This repository includes the `ContraProST` benchmark and accompanies the paper [Speech is More Than Words: Do Speech-to-Text Translation Systems Leverage Prosody?](https://aclanthology.org/2024.wmt-1.119/). `ContraProSt` is a dataset designed to evaluate the prosody awareness of speech-to-text translation systems. The examples are double-contrastive, thus having two different prosodies and two different translations. It includes translations from English to 3 languages (German, Spanish, Japanese) and 5 different prosodic phenomena (Sentence Stress, Prosodic Breaks, Intonation Patters, Emotion Prosody, Politeness).

## Data Format

The data is provided in CSV format (`data/en_de.csv`, `data/en_es.csv`, `data/en_ja.csv`), where each examples has the following attributes:

| Column Name | Description |
|---|---|
| sentence | The original English sentence. |
| category | Category of the sentence (e.g., "Sentence Stress"). |
| subcategory | Subcategory of the sentence, providing more specific context. (e.g., "Focus-Sensitive Operators") |
| domain | Domain of the sentence (e.g., "Legal"). |
| ID | Unique identifier for the sentence. |
| audio quality | 1 for passing quality, and 2 for good quality. For more information please refer to Appendix C. |
| prosody1 | First prosodic variation of the sentence. |
| meaning1 | Corresponding meaning of the first prosodic variation. |
| translation1 | Corresponding translation of the first prosodic variation. |
| audio1 | Path to the audio file for the first prosodic variation. |
| prosody2 | Second prosodic variation of the sentence. |
| meaning2 | Corresponding meaning of the second prosodic variation. |
| translation2 | Corresponding translation of the second prosodic variation. |
| audio2 | Path to the audio file for the second prosodic variation. |

## Using the data

The intended use of the data is to assess whether a system prefers the correct pair of audio-translation over the incorrect ones, through contrastive evaluation. Please refer to section 3 "Contrastive Evaluation" in the paper.

## Citing this work

Please cite this work as:

Ioannis Tsiamas, Matthias Sperber, Andrew Finch, and Sarthak Garg. 2024. [Speech Is More than Words: Do Speech-to-Text Translation Systems Leverage Prosody?](https://aclanthology.org/2024.wmt-1.119/). In Proceedings of the Ninth Conference on Machine Translation, pages 1235–1257, Miami, Florida, USA. Association for Computational Linguistics.