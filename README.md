# Vidhai

## What is Vidhai?
Vidhai is a collaborative open science initiative to identify, collect and create datasets for Tamil. Our objective is to enable and promote cutting edge AI research in Tamil by building foundation models and tools for native speakers of Tamil globally. We aim to have a single repository of Tamil datasets that could be used for different tasks like language modeling, QA, summarization etc.
All the datasets that are identified as part of the initiative will be added to [AI Tamil Nadu HuggingFace organization](https://huggingface.co/aitamilnadu).

## How to contribute to Vidhai?
It is going to be a life-long initiative, but to make it outcome based, we will run the initiative in phases with each phase focusing on different aspects of data curation. The primary language of contribution is Tamil, but we will also accept bilingual datasets aimed at specific tasks after detailed review.

### Phase 1
In `Phase 1`, our objective is to curate all the existing datasets (collect metadata) and find sources for creating new dataasets in Tamil that can enable further research. The different tasks that you could contribute to is listed below,

#### Task 1.1: Propose new datasets or share information about existing datasets 
You could propose creating a new dataset or sharing information about existing data subsets (which is part of a multilingual dataset or monolingual dataset). Upon submission of the [proposal form](https://forms.gle/uprWQiwEGzoDKwLq5), our team will review the dataset. 
- Once the data proposal is accepted, we will share the format in which the data has to be scraped (if new data) or converted (if existing data).
- You will then follow the guidelines and reformat the data, provide metadata through [metadata form](https://forms.gle/27MiJrjdzjQ3Qjwe9) and the data will be added to the final `vidhai_dataset`.

#### Task 1.2: Create datasets through webscraping or OCR
If you do not know where to start, you can feel free to choose from the [issues](https://github.com/aicbe/Vidhai/issues) and work on the listed sources and create datasets out of it.
- Once the data is scraped or text is obtained through OCR, it should be converted to the prescribed format and reviewed.
- Also, provide metadata through [metadata form](https://forms.gle/27MiJrjdzjQ3Qjwe9) and the data will be added to the final `vidhai_dataset`.

**Note:** If there are quality issues in `Phase 1` tasks, then this dataset will be moved to `Phase 2` for fixing them. Once quality issues are fixed, then the data will be added to the final `vidhai_dataset`.

### Guidelines for submitting data
Once the proposal form is submitted, the dataset is approved and the reformatting is done, follow the steps below to submit the dataset to the `Phase 1` of the initiative.

1. **Setup:**
   - First, [fork the repository](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) in GitHub! :fork_and_knife:
   - The repository will be forked and it will be under your GitHub repositories as `PATH_TO_YOUR_FORK`.
   - Next, [clone the forked repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository) and create a branch with the name of the dataset i.e.       `vidhai_<dataset_name>`,
      ```bash
      git clone $PATH_TO_YOUR_FORK
      cd Vidhai
      git checkout -b vidhai_<dataset_name>
      ```
2. **Creating folder structure for datasets:**
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
3. **Preprocessing data:**
   - Place the original dataset that you have scraped or identified in the `data_original` folder.
   - Create a python script with the name `vidhai_<dataset_name>_processor.py` and add the relevant code to perform any kind of preprocessing to the original data.
   - Once the preprocessing is completed and the data is reformatted to a agreed upon format, place the processed data in `data_processed`.
     
4. **Adding data card and requirements.txt:**
   - Create a detailed data card describing the dataset in detail and add it to `vidhai_<dataset_name>/README.md`. Refer to the [sample data card]() and fill in the relevant information.
   - If you intend to use external libraries for preprocessing, add them with their version numbers in `vidhai_<dataset_name>/requirements.txt`.
   
5. **Create a PR:**
   - First, commit and push your changes:
    ```bash
    git add vidhai_<dataset_name>/README.md
    git add vidhai_<dataset_name>/requirements.txt
    git add vidhai_<dataset_name>_processor.py
    git commit -m "Added new preprocessed dataset - vidhai_<dataset_name>"
    git push --set-upstream origin vidhai_<dataset_name>
    ```
    - Finally, [submit a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request). The last `git push` command prints a URL that can         be copied into a browser to initiate such a pull request.
    - Alternatively, you can submit a PR from the GitHub website. 
  
:sparkles: Congratulations, you've submitted a dataset to Vidhai! :sparkles:

### Phase 2
In `Phase 2`, our objective is to fix the quality issues in the approved datasets. We will need annotators, translators, NLP experts and linguists to work on the quality issues.

#### Task 2.1: Fix quality issues in the approved dataset
The datasets with quality issues from `Phase 1` will be moved to `Phase 2` for quality checking. For example, removing other language words, unwanted links or references from a scraped or OCRed Tamil dataset or even from existing multilingual subsets.
- If you're interested in this task, you can go to the [portal]() and sign up.
- Instructions will be provided on how to fix the quality issues on the portal.
- Follow the instructions and fix the issue of as many data points as you can.

## Who can contribute?
- Everyone can join and contribute to this initiative between _1st March 2024_ and _31st August 2024_.
- `Phase 1` will start first and once we start identifying the issues with quality of the submitted data, `Phase 2` will start then.
- If you’re able to contribute in a qualitative way according to our guidelines, you stand a chance to win some SWAGS, and become a co-author of our upcoming paper.

## Thank you! 
We greatly appreciate your help! We recognize that some datasets require more effort than others, so please reach out to us on [discord](https://discord.gg/ErRBRCsK) if you have any questions. Our goal is to be inclusive with credits and value everyone's time!

## Contact
For more information please reach us at coimbatoreai@gmail.com or [discord](https://discord.gg/ErRBRCsK).
