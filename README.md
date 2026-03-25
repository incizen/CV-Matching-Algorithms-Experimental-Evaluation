# CV-Matching-Algorithms-Experimental-Evaluation

## Overview
This is an experimental evaluation of algorithms that are uses for resume-job description matching.

## Pipelines
There are 3 pipelines for 3 different algortithms used for comparison:
- TF–IDF + Cosine Similarity
- BM25
- Sentence-BERT (SBERT)

## Structure
- EvaluationMetrics.ipynb → Main notebook for running evaluation
- Evaluation_summary.csv → Final results (MRR, precision and Hit Rate.)
- GroundTruth_FinalVer.csv → Manually labeled
- TF_IDF_and_Cosine_Similarity.ipynb, Sentence_BERT_(SBERT).ipynb, BM25.ipynb → Testing Pipelines
- TF-IDF_TestingResults.csv, BM25_Results.csv, SBERT_Results.csv → Ranking output results from the pipelines

## Requirements 
- Python 3.9+

## Datasets
Resume dataset: CareerCorpus.xlsx from https://data.mendeley.com/datasets/wzzwn37gmd/1 (already in repo).

Joob descriptions dataset: https://huggingface.co/datasets/lang-uk/recruitment-dataset-job-descriptions-english (Needs to be downloaded).

Ground truth spreadsheet: was created manually and is labeled as 1 (relevant) and 0 (not relevant).


## How to Run
- Clone the repository
- Install requirements
- Load the huggingface dataset using this code

     ```
   from datasets import load_dataset
     data = load_dataset("lang-uk/recruitment-dataset-job-descriptions-english")['train']
   ```

## Results
Combined final results are all in the Evaluation_summary.csv
