**All the contributed datasets will be placed under this directory.**

If you're working on a new approved dataset, please follow the below steps,

## Creating folder structure for datasets:
   - Get into the `datasets` folder and create sub-folder with the dataset name.
     ```bash
        cd datasets
        mkdir vidhai_<dataset_name>
        git checkout -b vidhai_<dataset_name>
      ```
   - Create two sub-folders under vidhai_<dataset_name> namely `data_original` and `data_processed`. 
     ```bash
        cd vidhai_<dataset_name>
        mkdir data_original
        mkdir data_processed
     ```
## Preprocessing data:
   - Place the original dataset that you have scraped or identified in the `data_original` folder.
   - Create a python script with the name `vidhai_<dataset_name>_processor.py` and add the relevant code to perform any kind of preprocessing to the original data.
   - Once the preprocessing is completed and the data is reformatted to a agreed upon format, place the processed data in `data_processed`.
     
## Adding data card and requirements.txt:
   - Create a detailed data card describing the dataset in detail and add it to `vidhai_<dataset_name>/README.md`. Refer to the [sample data card]() and fill in the relevant information.
   - If you intend to use external libraries for preprocessing, add them with their version numbers in `vidhai_<dataset_name>/requirements.txt`.

## Points to remember
- Do not commit the datasets to Github, instead upload them to the datasets under [aitamilnadu organization on HuggingFace](https://huggingface.co/aitamilnadu).
- Each dataset link will be provided to you after approval. You can upload the processed data (data stored under `data_processed`) along with the `requirements.txt` and `vidhai_<dataset_name>_processor.py` to the repository.
- A detailed data card should be created on HuggingFace by copying the content of the `vidhai_<dataset_name>/README.md`.
- Add the HF link of the dataset in the `vidhai_<dataset_name>/README.md` as well.

