 # Social Network stress Visualization, Analysis and a Predicirion Model training

This repository contains an exploratory data analysis project focused on visualizing and analyzing social network stress data. The project includes the use of Jupyter Notebooks to analyze, visualize, and report insights from the dataset.

## Table of Contents

1. [Introduction](#introduction)
2. [Data Collection](#data-collection)
3. [EDA and Data Visualization](#eda-and-data-visualization)
4. [Environment](#environment)
5. [How to Use](#how-to-use)
6. [Conclusion](#conclusion)

## Introduction

This project leverages a dataset of labeled Reddit and Twitter posts, categorized as stressful or non-stressful, to analyze and visualize the data. Additionally, I will experiment with various machine learning techniques to train a model that achieves optimal performance on prediction quality metrics.

## Data Collection

The dataset was takem from Kaggle - https://www.kaggle.com/datasets/mexwell/stress-detection-from-social-media-articles/data


## EDA and Data Visualization

The data was explored using statistical methods and visualizations to gain an initial understanding of the data distribution and relationships between features.

The visualizations in this project include bar graphs, scatter plots, and line-plots that help reveal patterns and relationships within the data and assess training metrics. These visual aids are critical for understanding complex data sets and presenting findings effectively.

## Environment

To work and play around on ML/AI topics I use a `conda` environment which `env`-file looks like the following:
```yaml
name: ai
channels:
  - defaults
  - pytorch
  - free
  - conda-forge
  - conda-forge/label/gcc7
dependencies:
  - numpy
  - pandas
  - matplotlib
  - pillow
  - pip
  - plotly
  - scikit-learn
  - seaborn
  - python
  - jupyter
  - pytorch
  - transformers
  - gensim
  - arrow
  - umap-learn
  - keybert
  - langchain
  - ollama
  - chromadb
  - questionary
```
I didn't want to push it to not keep the same file within multiple projects. You can create this or similar environment wherever you want to run this notebook by copying the YAML in a file (say, `ai_env.yml`) and running:
```bash
conda env create -f ai_env.yml
```
Of course, that ☝️ requires having `conda` installed in your environment.
Otherwise, if you use `pipenv` or something else - you'll to make sure the libraries used in imports are installed.

## How to Use

To use this project, follow these steps:

1. Clone the repository: `git clone https://github.com/yourusername/social-net-stress-visuals-plt.git`
2. Install the required dependencies
3. Open the Jupyter Notebook file in your favorite code editor or directly in Jupyter Notebooks.
4. Run the cells to execute the code and generate visualizations.

## Conclusion

Using the analysis and visualizations, a couple of ML and NN techniques were chosen and tested to solve the problem of detecting "stressful" posts on social network (Reddit).

**Logistic Regression** on both - **Doc2Vec vectors** and **KeyBERT embeddings** demonstrated very good results, but KeyBERT-version was better still as it improved not only precision for both classes a bit, but also significantly improved the precision of the negative class with that improving the shape of the PR-curve (**AUPRC 99%+**).
