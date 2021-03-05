# Applied_Machine_Learning

## Assessment Requirements

### Cyber Threat Detection Competition using Machine Learning
Software to detect cyber threats and protects a computer system (e.g. IoT, AV and UAV) from various cyber-attacks. The task of cyber threat detector learning is to build a predictive model (i.e. a machine-learning classifier) capable of distinguishing between “intrusive” traffic, called threats or attacks, and “good” normal traffic.

The Aegean WiFi Intrusion/threat Dataset (AWID) project was prepared and managed by George Mason University and University of the Aegean. The objective was to survey and evaluate research in cyber threat detection. A standard set of data to be audited, which includes real traces of both normal and intrusive 802.11 traffic with a wide variety of cyber threats/intrusions simulated in a physical lab which realistically emulates a typical SOHO infrastructure, was provided.

Details of the dataset can be found here: http://icsdweb.aegean.gr/awid/draft-Intrusion-Detection-in-802-11-Networks-EmpiricalEvaluation-of-Threats-and-a-Public-Dataset.pdf

AWID dataset categorises the attacks according to the methodology of execution. Attacks that have similar patterns of expression fall under one of the groups:

a. injection attacks,

b. flooding attacks,

c. impersonation attacks,

d. passive attacks.

We will use the reduced CLS portion of the AWID dataset because it serves as a useful starting point for preliminary research, and affords a baseline against which the new built models can be compared with the state-of-the-art Deep Feature Extraction and Selection (DFES) method, and other methods using the same reduced CLS portion.

Although flooding and injection attack signatures are also available within the AWID-CLS dataset, impersonation attacks were our focus as Hirte, Honeypot and EvilTwin impersonation attacks have previously been identified as the most severe threats to a network5 and have been the focus of earlier research. As a result, detecting impersonation attacks as the focus of our work will allow us to directly compare the performance of our model to others, a key weakness within the current body of machinelearning-based IoT IDS research. 

## Aim of the Assessment
The aim of this assessment is to provide a hands-on, practical, assessment of your machine learning skills for cyber threat detection application.

## Description of Task to be Completed
Your task is to build a predictive model (i.e. a machine learning classifier) capable of distinguishing between “intrusive” traffic, called threats/intrusions or attacks, an
“good” normal traffic. There is a research element in this coursework (e.g. creating additional features).

### Downloading dataset
The dataset for this project is available on VLE. You need to use train_imperson_without4n7_balanced_data.csv for training and test_imperson_without4n7_balanced_data.csv for testing. The first row of each dataset gives variable numbers (this may need to be removed). The original dataset has 154 input variables and 1 target variable however two of the input variables numbered 4 and 7 (frame.time_epoch and frame.time_relative) have been removed from both datasets as they provide temporal information which may cause unfair prediction. The training set has 97044 observations while testing set has 40158 observations.

### Constructing and Selecting Features

- Create additional features using a representation learner (e.g. Autoencoder, VAEs, SAEs, GAN etc). The latent space representation, simply a representation of compressed data by a representation leaner, may contain important information needed to represent original data point.

- Combine the additional features with original dataset. The combined dataset should have 154 (original features) + additional features. For example, if you created 10 features using SAE, the new combined dataset must have 164 input features + 1 target. 

- Apply feature selection techniques (e.g. filter, wrapper and embedded) and see if any of the additional features created by a representation learner are selected.

### Building ML algorithms

- Select candidate algorithms. Discuss the selection strategies for the candidate algorithms.

- Finding the best configuration for these hyperparameters in such a high dimensional space is not a trivial challenge. Consider the model design components (e.g. no of layers, no of units per layer, loss function, activations, optimisers, dropout layer etc) as well as the hyperparameters (e.g. learning rate, dropout rate, batch size etc). Perform model-specific optimisations and iteratively debug model as complexity is added. Discuss the selection strategies for searching for the best configuration (e.g. trial and error, grid search, random search, Bayesian optimisation etc).

### Evaluating model and analysing the results.

- Evaluate the classification performance (e.g. accuracy, detection rate, false alarm, type II error, MCC and TBM (time has taken to build model) and TTM (time has taken to test model) – go beyond these measures if necessary) of the selected models on the test data and interpret the results. 

- Discuss general model trade-offs (accuracy vs speed vs interpretability) of the chosen models considering a particular application (e.g. IoT, autonomous vehicle, etc) and propose two models (e.g. features selected and ML classifiers) and provide justification of choice. 
