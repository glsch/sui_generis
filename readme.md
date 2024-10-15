## _Sui Generis_: Large Language Models for Authorship Attribution and Verification in Latin

This repository contains the data and code for the paper ["Sui Generis: Large Language Models for Authorship Attribution and Verification in Latin"]() by Gleb Schmidt, Svetlana Gorovaia, and Ivan Yamshchikov. 
```bibtex
@inproceedings{sui_generis_2024,
  title={Sui Generis: Large Language Models for Authorship Attribution and Verification in Latin},
  author={Schmidt, Gleb and Gorovaia, Svetlana and Yamshchikov, Ivan P.},
  eventtitle={Natural Language Processing for Digital Humanities (NLP4DH), Miami, FL, 16 November 2024},
  eventdate = {2024-11-16},
  year={2024}
}
```
### Data
The data is available in the `data` folder. It contains the following files:
- `authorship_verification_dataset.pkl`: 660 pairs of randomly sampled texts from the dataset, which were prompted to the models, 220 pairs during each iterations. The file also contains the authorship labels as well as embeddings of the texts by `text-embedding-3-large` model (OpenAI).
- `authorship_verification_responses.tsv`: contains all the responses by the models (excluding those where the models failed to provide a correctly-structured output). `data_record_id` column contains the unique identifier of the text pair prompted to the model. Using this number, the pair can be retrieved from `authorship_verification_dataset.pkl`.
- `authorship_attribution_responses.csv`: contains all the responses by GPT-4on the authorship attribution task.