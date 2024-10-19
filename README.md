# Hugging-Face-Dataset-Cleaner

A Jupyter notebook to clean and preprocess Hugging Face JSON datasets by removing unannotated sentences and reassigning ID numbers.

## Overview

This tool is designed to process Hugging Face JSON datasets, specifically for Named Entity Recognition (NER) tasks. It performs the following operations:

1. Removes sentences that have no annotations (i.e., only contain 0 in the `ner_tags` list).
2. Reassigns ID numbers to the remaining sentences.
3. Maintains the original JSON structure and formatting.
4. Provides statistics on the cleaning process.

## Features

- Efficiently processes large JSON datasets
- Preserves the original JSON structure
- Provides detailed statistics on the cleaning process
- Interactive Jupyter notebook for easy customization and experimentation

## Requirements

- Python 3.6 or higher
- Jupyter Notebook
- Required Python libraries (specified in the notebook)

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/SakibAhmedShuva/Hugging-Face-Dataset-Cleaner.git
   ```
2. Navigate to the project directory:
   ```
   cd Hugging-Face-Dataset-Cleaner
   ```
3. Install required dependencies (if not already installed):
   ```
   pip install jupyter numpy pandas
   ```

## Usage

1. Start Jupyter Notebook:
   ```
   jupyter notebook
   ```
2. Open the `hf_cleaner.ipynb` notebook in your browser.
3. Follow the instructions in the notebook to load your dataset and run the cleaning process.

## Notebook Contents

The `hf_cleaner.ipynb` notebook contains:

- Detailed explanations of each step in the cleaning process
- Code cells to load, process, and save the dataset
- Visualizations and statistics about the dataset before and after cleaning

## Output

The notebook will display the following statistics:

- Total sentences found
- Total sentences with no annotation deleted
- Final remaining sentences

It will also save the cleaned dataset to a new JSON file.

## Example

Input JSON format:
```json
{"id":"0","tokens":["-"],"ner_tags":[0]}
{"id":"1","tokens":["Example","sentence"],"ner_tags":[1,0]}
```

Output JSON format:
```json
{"id":"0","tokens":["Example","sentence"],"ner_tags":[1,0]}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Hugging Face for their excellent NLP resources and datasets

## Contact

If you have any questions or feedback, please open an issue in this repository.
