<a id="readme-top"></a>

<br />
<div align="center">
<img src="images/logo.png" alt="Logo" width="150" height="100">

<h1 align="center">GTZAN Music Genre Classification</h1>
</div>

<details open="open">
<summary>Table of Contents</summary>
<ol>
  <li>
    <a href="#about-the-project">About The Project</a>
    <ul>
      <li><a href="#dataset">Dataset</a></li>
    </ul>
  </li>
  <li>
    <a href="#getting-started">Getting Started</a>
    <ul>
      <li><a href="#clone-the-repository">Clone the repository</a></li>
      <li>
      <a href="#prerequisites">Prerequisites</a>
     <ul>
       <li><a href="#requirementstxt">requirements.txt</a></li>
       <li><a href="#download-the-dataset">Download The Dataset</a></li>
     </ul>
      </li>
    </ul>
  </li>
  <li>
    <a href="#usage">Usage</a>
    <ul>
      <li><a href="#code-guide">Code Guide</a></li>
    </ul>
  </li>
  <li><a href="#contributing">Contributing</a></li>
  <li><a href="#acknowledgments">Acknowledgments</a></li>
  <li><a href="#license">License</a></li>
</ol>
</details>


## About The Project
This repo aims to find a high accuracy classification model for classifying 10 popular music genres (blues, classical, country, disco, hiphop, jazz, metal, pop, reggae, rock) from the famous <a href = "https://short-link.me/RGU5">GTZAN dataset</a> by using Machine Learning libraries to visualize, preprocess, and train the data. It is worth noting that instead of only tuning hyperparameters or adding more preprocessing, normalization and regularization steps to improve the model's performance and generalization this project implements a code for extracting <a href= "https://en.wikipedia.org/wiki/Spectral_flux">Spectral Flux</a> features(mean and var) from the same dataset.

### Dataset
The original dataset is the popularly known GTZAN Dataset provided by <a href = https://webhome.csc.uvic.ca/~gtzan/index.html#>George Tzanetakis</a> and presented in his 2002 paper <a href = https://dspace.library.uvic.ca/server/api/core/bitstreams/d7457cdf-e42f-4772-b9ee-801adf43f949/content>Musical genre classification of audio signals</a> which was a part of his PhD thesis at Princeton University. However, dataset used in this project is a Kaggle reproduction available at this <a href="https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification/data">link</a>.

This dataset, consists of 100 tracks containing 10 different music genres, along with two CSV files comprising the features of each audio, and an image folder containing the visualization for every audio file.

## Getting Started

### Clone the repository
clone the repo using this command in your pereferred environment's command line:

```sh
git clone https://github.com/Amir-Abed/Music-Recommender-System-With-FastAPI.git
```

### Prerequisites
#### requirements.txt
Install the required libraries with the following command :

```sh 
pip install -r requirements.txt 
```
Ensure that all files necessary for ```pip install``` are kept in the root directory of this project.

#### Download The Dataset
You should be able to download the dataset through `Downloading the GTZAN dataset from Kaggle` section from `gtzan_music_genre_classification.ipynb` file but in case you have problems doing that follow these below steps :
1. Refer to <a href="https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification">this link</a> to download it manually.
3. Extract the `Data` folder from the downloaded ZIP file into the root directory of this project.

## Usage

### Code Guide
`gtzan_music_genre_classification.ipynb` is the main file for this project and contains visualization steps to get familiar with the data and its structure, preprocessing steps to prepare our data for training, and evalution steps with graphs to check how good our model performed. This file uses five different models(CNN, Random Forest, Gradient Boosted Trees, SVM, KNN) to train on the dataset. The models are compared against each other by various metrics like accuracy and recall to identify the best-performing one. Also hyperparameters are tuned in a way to give all models an equal chance in the training phase.

For detailed instructions and code explanations refer to the comments within each file.

## Contributing
Contribution is welcome. This helps the community grow and for everyone to learn :) .

Please feel free to open an issue or submit a pull request.

## Acknowledgments
[Andrada](https://www.kaggle.com/andradaolteanu) : For providing the dataset that sereved as the basis of this project.

[othneildrew](https://github.com/othneildrew/Best-README-Template) : For help in creating this readme file.

Some concepts were inspired by this kaggle notebook : [Andrada | Work w/ Audio Data: Visualise, Classify, Recommend](https://www.kaggle.com/code/andradaolteanu/work-w-audio-data-visualise-classify-recommend)

## License
[MIT](LICENSE) © Amirreza Abedini
