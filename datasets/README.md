All the contributed datasets will be placed under this directory.

If you're working on a new approved dataset, please follow the below steps,

- Create a sub-folder with the dataset name in the format `vidhai_<dataset_name>`.
- Place the original and processed dataset within the `vidhai_<dataset_name>` folder under two sub-folders named `data_original` and `data_processed`.
	- Do not commit the datasets to Github, instead upload them to aitamilnadu organization on HuggingFace.
	- Each dataset link will be provided to you after approval.
	- Add the link to the original and processed data in the respective README files. 
- The code used for processing the dataset should be placed within a sub-folder called `scripts`.
- A detailed data card should be created on HuggingFace and the same should be copied in `vidhai_<dataset_name>/README.md'.

