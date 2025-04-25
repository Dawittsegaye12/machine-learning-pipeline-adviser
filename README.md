# SmartML Blueprint

SmartML Blueprint is a meta-learning assistant designed to recommend machine learning pipelines for end-to-end ML projects. It provides suggestions for preprocessing steps, model selection, evaluation metrics, and deployment strategies based on dataset characteristics.

## Features

- **Dataset Metadata Extraction**: Extracts key characteristics of datasets, such as the number of features, missing values, and data types.
- **Notebook Parsing**: Analyzes Kaggle notebooks to identify preprocessing steps and models used.
- **Pipeline Recommendations**: Suggests preprocessing techniques, machine learning models, and deployment methods tailored to the dataset.
- **Throttled API Requests**: Ensures compliance with Kaggle API rate limits.

## Project Structure

- `dataset.ipynb`: A Jupyter Notebook demonstrating how to use OpenML datasets and save them locally.
- `scraper.py`: A Python script to scrape Kaggle datasets and notebooks for metadata and preprocessing/model information.
- `requirements.txt`: Lists the dependencies required for the project.
- `titanic_dataset.csv`: A sample dataset fetched from OpenML.

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd SmartML_Blueprint
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up Kaggle API:
   - Download your Kaggle API token (`kaggle.json`) from your Kaggle account settings.
   - Place the file in the appropriate directory:
     - Windows: `C:\Users\<YourUserName>\.kaggle\`
     - Linux/Mac: `~/.kaggle/`

## Usage

### 1. Scraping Kaggle Datasets and Notebooks

Run the `scraper.py` script to fetch metadata for datasets and notebooks:
```bash
python scraper.py
```
- The script saves dataset metadata to `kaggle_datasets.csv`.
- Notebook metadata is saved to `kaggle_notebooks.csv`.

### 2. Parsing Notebooks for Preprocessing and Models

Replace the placeholder `example_notebook_id` in `scraper.py` with a valid Kaggle notebook ID (e.g., `username/notebook-title`).
Run the script to extract preprocessing steps and models used in the notebook.

### 3. Working with OpenML Datasets

Use the `dataset.ipynb` notebook to fetch datasets from OpenML and save them locally. For example, the Titanic dataset is saved as `titanic_dataset.csv`.

## Contributing

Contributions are welcome! If you have ideas for improving the project, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

- [OpenML](https://www.openml.org/) for providing datasets and metadata.
- [Kaggle](https://www.kaggle.com/) for hosting datasets and notebooks.
- The Python community for libraries like `pandas` and `kaggle`.