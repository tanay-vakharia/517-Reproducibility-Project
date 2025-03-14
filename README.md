# Wikipedia AI Detection Reproducibility Project

## Overview
This repository contains code and datasets used for our reproducibility study on AI-generated content detection. We evaluate the performance of Binoculars and LLMDet on Wikipedia datasets, as well as additional datasets from Common Crawl. Our experiments involve scraping Wikipedia articles, processing the text, and running evaluations using these AI detection models. This is aiming to reproduce the results from this paper: https://arxiv.org/pdf/2410.08044 (The Rise of AI-Generated Content in Wikipedia)

## Running the Code on Google Colab
All experiments can be run directly in Google Colab. Follow these steps:
1. Open the provided Colab notebooks in the `Notebooks/` folder.
2. Ensure your runtime has GPU enabled (if needed for performance).
3. Run the notebook cells sequentially to:
   - Install dependencies
   - Download and preprocess data
   - Evaluate using Binoculars and LLMDet
   - Visualize results

## Dependencies
The notebooks handle installing dependencies automatically, but if needed, install manually these dependecies:
- `beautifulsoup4` (for web scraping)
- `requests` (for HTTP requests)
- `pandas` (for data handling)
- `numpy` (for numerical computations)
- `matplotlib` (for visualization)
- `Binoculars` and `LLMDet` (external repositories, see below)

## Data Download Instructions
### Wikipedia Data
1. Open the scraping notebooks in `Scraping/Wikipedia` in Google Colab.
2. Run each of the notebooks to collect Wikipedia articles for pre-2022, August 2023, August 2024, and February 2025

### Common Crawl Data
1. Open `Scraping/CommonCrawl.ipynb` in Google Colab.
2. Run the scraping script to collect datasets for January 2022, September 2023, August 2024, and February 2025

## Preprocessing
The scraping notebooks already preprocess the data to be used for evaluation

## Training (if applicable)
This project does not require training a model from scratch. Instead, we evaluate using pretrained models (Binoculars and LLMDet).

## Evaluation
### Using Binoculars
1. Open `Evaluation/Binoculars.ipynb` in a Colab notebook and run it
2. This will clone the binoculars repository, create a Binoculars instance, setup dependencies, and run evaluation on the scraped datasets on Wikipedia and Common Crawl

### Using LLMDet
1. Open `Evaluation/LLMDet.ipynb` in a Colab notebook and run it
2. This will clone the LLMDet repository, create a LLMDet instance, setup dependencies, and run evaluation on the scraped datasets on Wikipedia and Common Crawl

## Pretrained Models
Both Binoculars and LLMDet require pretrained models, which are automatically used when running evaluation scripts.
## Contributors
- Tanay Vakharia
- Phil Bedford
- Parker Gustafason


## Acknowledgments
We thank the authors of Binoculars and LLMDet for making their models available.

---
This README provides all necessary information to reproduce our experiments in Google Colab, including dependencies, data collection, preprocessing, evaluation, and visualization.

