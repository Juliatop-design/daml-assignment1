# 19th-Century English Novels Dataset

## 2a) Data description

This repository contains a dataset of 20 English-language
novels from the 19th century, collected from Project Gutenberg.

Each novel is stored as a separate text file in the data folder.
Information about the novels is stored in metadata.csv.

## 2b) Motivation

I created this dataset to collect and organise a small selection of English-language novels from the 19th century. The aim is to make it easier to compare novels written by different authors and published in different years.

The dataset could help answer research questions such as: How are the novels distributed across different authors and publication decades? How does vocabulary use differ between the selection of novels?

## 2c) Selection Criteria

The dataset includes 20 English-language novels originally published between 1800 and 1899. All texts were selected from Project Gutenberg because they are freely accessible and available as plain text files.

The novels were chosen to include different authors, publication years and types of fiction. This way I can compare the writing styles and vocabulary between authors, as well as possible differences in language use across publication periods and types of fiction.  

Books originally published in other languages or outside the 19th century were excluded to keep the dataset focused and to make comparisons between novels easier. By selecting books from the same century and originally written in the same language, differences in language use can be studied without introducing additional variation from different languages or historical periods.

The dataset represents a small selection of 19th-century English-language literature. However, it is not representative of all novels from this period, as many other authors, lesser-known works and books that are not available on Project Gutenberg are missing.

## 2d) Data Collection Process

The 20 novels were collected from Project Gutenberg on 14 November 2026. Each novel was downloaded manually by visiting its Project Gutenberg page and selecting the plain text (.txt) version under "Other formats & older devices".

After downloading, the files were renamed using their unique Project Gutenberg eBook numbers (e.g., gut1342.txt) and stored in the data folder. The original source URL for each novel was recorded in metadata.csv.

No web scraping was used during the collection process.

## 2e) Cleaning and Preprocessing

No cleaning or preprocessing was performed on the original texts. The downloaded books were kept in their original form, including the Project Gutenberg headers and licence information.

The files were only renamed using their unique Project Gutenberg IDs and organised in the data folder. A separate metadata.csv file was created to store information about each novel in a consistent format.

## 2f) Structure and Codebook

### Folder Structure 
The dataset is organised into the following files and folders:

data/: Contains the 20 original text files, with one file per novel. Each file is named using its unique Project Gutenberg ID (e.g., gut1342.txt).

metadata.csv: Contains information about each of the 20 novels, with one row per novel.

create_metadata.ipynb: Jupyter Notebook used to create the metadata.csv file.

check_dataset.ipynb: Jupyter Notebook used to check the dataset, including file paths, unique IDs, missing values and basic summary statistics.

requirements.txt: Lists the Python packages needed to run the notebooks.

README.md: Provides documentation about the dataset.

### Codebook
The metadata.csv file contains eight columns. The table below explains the meaning, data type, expected format and missing-value conventions for each column.

| Column | Description | Type | Allowed values / Expected format | Missing values |
|---|---|---|---|---|
| id | Unique identifier for each novel | String | gut followed by the Gutenberg ID, e.g. gut1342 | Not allowed |
| file | Relative path to the text file | String | data/gut[number].txt | Not allowed |
| source | Original source of the novel | String (URL) | Project Gutenberg eBook URL | Not allowed |
| licence | Copyright status of the text in the USA | String | Public domain in the USA | Empty if unknown |
| title | Title of the novel | String | Text | Empty if unknown |
| author | Name of the author | String | Author's name | Empty if unknown |
| publication_year | Original publication year | Integer | 1800-1899 | Empty if unknown |
| language | Language of the novel | Categorical | ISO 639-1 language code (en) | Empty if unknown |

## 2g) Uses and Limitations

This dataset can be used to explore differences in vocabulary and writing styles between 19th-century English-language novels. It could also be used to compare novels written by different authors or published in different decades. 

However, the dataset contains only 20 selected novels and is not representative of all English-language literature from the 19th century. Well known authors may be overrepresented, while less known works and novels unavailable on Project Gutenberg are excluded. Another important point is that the original text files still contain Project Gutenberg headers and licence information. These would need to be removed before conducting accurate text analysis, as they could affect results such as word frequencies.

## 2h) Ethical and Legal Aspects

The dataset contains publicly available historical novels and does not intentionally collect private or sensitive information about living individuals. However, some novels contain outdated language and social attitudes that should be considered when analysing and interpreting the texts.

The copyright status of the 20 novels was checked using the Project Gutenberg information, the downloaded text files and Dutch copyright rules. All 20 novels are identified as public domain in the United States by Project Gutenberg. In the Netherlands, copyright generally expires 70 years after the author's death. All selected authors died more than 70 years ago, so their original works are in the public domain in the Netherlands.

Some downloaded editions also contain historical introductions, illustration references or old copyright notices. These were checked for possible restrictions, and no clear additional copyright obstacles were identified.

The Project Gutenberg terms of use and licence were checked on 18 November 2026. Project Gutenberg explains that its works can be shared without charge while keeping them "with its attached full Project Gutenberg-tm License". The original text files have not been modified, and their licence information has been preserved. Each novel's source URL is recorded in metadata.csv.

Project Gutenberg licence: https://www.gutenberg.org/policy/license

## 2i) Licence and Citation

The original novels are in the public domain in the United States and the Netherlands. The downloaded text files are redistributed under the applicable Project Gutenberg conditions. Their original licence information has been preserved, and the source of each novel is recorded in metadata.csv.

The metadata and documentation created for this dataset are shared under the Creative Commons Attribution 4.0 International (CC BY 4.0) licence. This allows others to reuse and adapt this material, provided that appropriate credit is given.

Licence: https://creativecommons.org/licenses/by/4.0/

If you use this dataset, please cite it as follows:

Juliatop-design. (2026). 19th-Century English Novels Dataset [Dataset]. GitHub. [Repository URL]

When using individual novels, users should also acknowledge the original authors and Project Gutenberg as the source.