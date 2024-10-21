
# Healthy-Unhealthy Leaf Classification

This repository contains code and experiments conducted for the [Codalab competition](https://codalab.lisn.upsaclay.fr/competitions/16245), where the task was to classify plant leaves as healthy or unhealthy using a dataset of 5200 images. The project tackles the challenges of small dataset size, class imbalance, and high similarity between classes using data augmentation, transfer learning, and various deep learning techniques.

## Table of Contents
- [Project Overview](#project-overview)
- [Task Details](#task-details)
- [Repository Structure](#repository-structure)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The goal of this project is to develop a convolutional neural network (CNN) that can accurately classify images of plant leaves into two categories: healthy and unhealthy. The dataset consists of 5200 images, later reduced to 4800 after cleaning. The key challenges addressed in this project include:
- **Class Imbalance**: 3199 healthy vs. 2001 unhealthy samples.
- **Limited Data**: Augmentation techniques were employed to artificially increase the dataset size.
- **High Similarity Between Classes**: Advanced models were used to extract subtle features for classification.

## Task Details
This project was part of the Codalab competition on leaf classification. The key objectives were:
- **Data Augmentation**: Traditional techniques such as rotation, flipping, and brightness adjustment, as well as advanced methods like MixUp and CutMix, were applied to help the model generalize better.
- **Transfer Learning**: Pre-trained models like ResNet-50 and ConvNext were fine-tuned on this dataset to leverage their feature extraction capabilities.
- **Ensemble Methods**: Various models were combined using weighted ensemble techniques to improve performance.

## Repository Structure
- `adaboost.ipynb`: Implements the AdaBoost algorithm as part of an alternative model exploration.
- `augmentation_and_finetuning.ipynb`: Implements data augmentation strategies and fine-tuning of pre-trained models.
- `convnext_finetuning.ipynb`: Fine-tuning ConvNext architecture for this classification task.
- `hyperparameters-tuner.ipynb`: Hyperparameter tuning for optimal model performance.
- `models_retrained_from_zero.ipynb`: Training models from scratch.
- `random_oversampling_RESNET_50.ipynb`: Using random oversampling to handle class imbalance with the ResNet-50 architecture.
- `weighted_ensemble.ipynb`: Combines model outputs via a weighted ensemble for improved accuracy.
- `report.pdf`: Full description of the problem, methodology, and results of the competition.

## Setup and Installation
To run the notebooks in this repository, follow these steps:
1. Ensure Python 3.x and Jupyter Notebook are installed.
2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
Each notebook can be run independently:
- **For data augmentation and fine-tuning**: Run `augmentation_and_finetuning.ipynb`.
- **For ConvNext fine-tuning**: Run `convnext_finetuning.ipynb`.
- **To explore ensemble learning techniques**: Run `weighted_ensemble.ipynb`.

Open each notebook in Jupyter and execute the cells sequentially to see the code and output.

## Results
The final model achieved significant improvements in classification accuracy through the use of transfer learning and data augmentation techniques. The ensemble approach further boosted performance by combining multiple models' predictions. The detailed results and analysis are provided in the [`report.pdf`](./report.pdf).

## Contributing
Contributions are welcome! If you have suggestions or encounter any issues, feel free to open an issue or submit a pull request.

## License
This repository is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
