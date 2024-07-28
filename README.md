
# COVID-19 Contact Tracing Using ML/DL Methods

**Project Goal**: Focus on COVID-19 contact tracing using machine learning and deep learning methods.

**Documentation and Paper**: To be published soon.

**Description**: This repository contains codes related to research on data synthesis and machine learning model development to fight COVID-19. Each step in the development process is documented and will be updated soon. The process is broken down into a chain of notebooks as described below.

## Phases of the Project:

1. **Data Cleaning**
   - **Notebook**: `CV19_Cleaning.ipynb`
   - **Purpose**: This notebook is dedicated to cleaning the COVID-19 dataset to make it suitable for analysis and modeling.
   - **Content**: 
     - Import necessary libraries like pandas and seaborn.
     - Read the raw data and perform various data cleaning steps such as handling missing values, reindexing, and ensuring data consistency.
     - Define functions to clean the dataset by removing entries with critical missing values and replacing missing identifiers with appropriate values.

2. **Data Exploration**
   - **Notebook**: `CV19_Dataset_Explore.ipynb`
   - **Purpose**: This notebook is for exploring the COVID-19 dataset.
   - **Content**: 
     - Mount Google Drive to access the dataset.
     - Load the dataset and perform exploratory data analysis (EDA) using visualization techniques.
     - Identify trends and patterns in the data to inform further analysis and model development.

3. **Dataset Building**
   - **Notebook**: `CV19_Dataset.ipynb`
   - **Purpose**: This notebook handles the dataset preparation for COVID-19 contact tracing.
   - **Content**: 
     - Install dependencies and define data structures.
     - Prepare the dataset for modeling by creating appropriate data loaders and preprocessing steps using PyTorch Geometric.

4. **Model Building**
   - **Notebook**: `CV19Net.ipynb`, `CV19_RNNNet.ipynb`
   - **Purpose**: These notebooks focus on setting up neural networks for COVID-19 contact tracing using PyTorch Geometric and RNN (Recurrent Neural Network) respectively.
   - **Content**: 
     - Install necessary packages and set up the environment for PyTorch Geometric.
     - Implement neural network architectures, including Seq2Seq models with attention mechanisms.
     - Define encoder and decoder classes for building the models.

5. **Candidate Models**
   - **Notebook**: `CV19Net.ipynb`, `CV19_RNNNet.ipynb`
   - **Purpose**: Evaluate different candidate models for effectiveness in contact tracing.
   - **Content**: 
     - Define various model configurations and hyperparameters.
     - Train and evaluate multiple candidate models to determine the best performing ones.
     - Save model parameters and configurations for further analysis.

6. **Training and Evaluation**
   - **Notebook**: `CV19Net.ipynb`, `CV19_RNNNet.ipynb`
   - **Purpose**: Train and evaluate the selected models.
   - **Content**: 
     - Implement training loops and evaluation metrics.
     - Use functions for batch training and evaluation.
     - Track and save training and validation losses for each iteration.
     - Evaluate models on random sentences and visualize attention mechanisms.

7. **Analysis of Models**
   - **Notebook**: `CV19_result_analysis.ipynb`
   - **Purpose**: Analyze the results obtained from the COVID-19 models.
   - **Content**: 
     - Import necessary libraries and set up the analysis environment.
     - Visualize results using matplotlib and other visualization tools.
     - Interpret model performance and identify areas for improvement.

## Technical Introduction to Models

### Seq2Seq Model with Attention Mechanism
- **Overview**: A Sequence to Sequence (Seq2Seq) model is used for predicting sequences. It consists of an encoder and a decoder, both typically implemented as Recurrent Neural Networks (RNNs).
- **Encoder**: Reads the input sequence and summarizes the information into a context vector.
- **Decoder**: Generates the output sequence based on the context vector provided by the encoder.
- **Attention Mechanism**: Enhances the Seq2Seq model by allowing the decoder to focus on different parts of the input sequence at each step, rather than relying solely on the context vector.

### Recurrent Neural Networks (RNN)
- **Overview**: RNNs are neural networks that excel in modeling sequential data. They maintain a hidden state that captures information about previous elements in the sequence.
- **Application**: Used in the project to model the temporal patterns in COVID-19 contact tracing data.

### PyTorch Geometric
- **Overview**: A library for deep learning on irregular structures like graphs. It extends PyTorch to provide tools for handling graph-structured data.
- **Application**: Used to build and train models that can leverage the graph-like structure of COVID-19 contact networks.

### Training and Evaluation Strategies
- **Training**: Implementing loops to train the models on batches of data, optimizing the weights to minimize loss.
- **Evaluation**: Using metrics such as loss and accuracy to assess the performance of the models. Visualization techniques are employed to interpret the results and improve the models iteratively.

## Notebooks Summary:

1. **CV19Net.ipynb**
   - **Content**: Neural network setup for COVID-19 contact tracing using PyTorch Geometric, including Seq2Seq models, encoder-decoder architecture, and training loops.

2. **CV19_Cleaning.ipynb**
   - **Content**: Data cleaning steps for the COVID-19 dataset, handling missing values, and ensuring data consistency.

3. **CV19_RNNNet.ipynb**
   - **Content**: Implementation of an RNN for COVID-19 contact tracing, including Seq2Seq models with attention mechanisms and training procedures.

4. **CV19_result_analysis.ipynb**
   - **Content**: Analysis of model results, visualization, and interpretation of model performance.

5. **CV19_Dataset.ipynb**
   - **Content**: Dataset preparation for modeling, defining data structures, and creating data loaders using PyTorch Geometric.

6. **CV19_Synthesis_Latest.ipynb**
   - **Content**: Data synthesis steps, visualization, and analysis for the COVID-19 project.

7. **CV19_Synthesis.ipynb**
   - **Content**: Data synthesis and visualization for the COVID-19 project.

8. **CV19_Dataset_Explore.ipynb**
   - **Content**: Exploratory data analysis, loading the dataset, cleaning it, and visualizing trends.
