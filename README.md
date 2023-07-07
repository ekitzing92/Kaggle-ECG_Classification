# Kaggle-ECG_Classification

The goal of this notebook is to predict arrhytmia on ECG. It is based on the MIT-BIH dataset.

In particular, this notebook aims at having a first assessment of the impact of adding an LSTM with an attention mechanism compared to the single CNN implemented in https://www.kaggle.com/code/gregoiredc/arrhythmia-on-ecg-classification-using-cnn.

The idea of using LSTM + attention for such issues come from articles like :
   - Jiang M, Gu J, Li Y, Wei B, Zhang J, Wang Z, Xia L. HADLN: Hybrid Attention-Based Deep Learning Network for Automated Arrhythmia Classification. Front Physiol. 2021 Jul 5;12:683025. doi: 10.3389/fphys.2021.683025. PMID: 34290619; PMCID: PMC8289344.
   - Ghool, S. and Rocke, S., 2023, June. Exploring the Effectiveness of LSTM and Self-Attention Models for Artifact Detection in PPG Signals. In 2023 5th International Conference on Bio-engineering for Smart Technologies (BioSMART) (pp. 1-4). IEEE.
   - He, T., Chen, Y., Chen, J., Wang, W. and Zhou, Y., 2022. SEVGGNet-LSTM: a fused deep learning model for ECG classification. arXiv preprint arXiv:2210.17111.

The notebook is structured as follows:
 - Loading of the dataset
 - Resampling of the data to counter class imbalance
 - Addition of Gaussian noise to help generalization
 - Définition of the network
 - Training
 - Evaluation in terms of accuracy and confusion matrix

Compared with using only the CNN, the results show a lower accuracy but higher confusion values for the least well predicted classes. These first findings seem to suggest that the use of the LSTM and the attention mechanism is likely to be effective for pathologies that are difficult to detect.

This study was carried out by evaluating only one relatively simple and arbitrarily defined architecture. For a more in-depth study of the usefulness of using LSTM and the attention mechanism, other architectures with other hyperparameters should be evaluated.
