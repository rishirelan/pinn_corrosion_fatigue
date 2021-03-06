This repository is provided for replication of results presented in:

A. Dourado and F. A. C. Viana, "[Physics-Informed Neural Networks for Corrosion-Fatigue Prognosis](http://phmpapers.org/index.php/phmconf/article/view/814)," Proceedings of the Annual Conference of the PHM Society, Scottsdale,USA, September 21-26, 2019.

This repository includes the following:
- **corrosion_fatigue_model.py**: contains function that creates the proposed recurrent neural network.
- **run00_MLP_logC_training.py**: file that trains the multilayer perceptron for the logC estimation.
- **run00_MLP_m_training.py**: file that trains the multilayer perceptron for Walker's model exponent (m) estimation.
- **run01_rnn_training.py**: trains the proposed recurrent neural network using the pre-trained multilayer perceptron
- **run02_rnn_prediction.py**: predicts the crack length in the wing panels of the entire fleet at the 7 year (or 20.000 flights) of operation. 

In order to run the codes, you will need to:
1. Install the PINN python package: https://github.com/PML-UCF/pinn
2. Download the datasets at: De Piemonte Dourado, Arinan; Viana, Felipe, 2019, "Replication Data for: PINN corrosion-fatigue_PHM 2019", https://doi.org/10.7910/DVN/PZ7DRJ, Harvard Dataverse, V1, and extract files to the directory where this repository is cloned.

## Disclosure:
In the paper, we described a procedure for the multilayer perceptron initialization involving randomly generated planes. For simplicity this procedure is not reproduced here. Instead, we opt to use an illustrative plane whose data values are expressed in the "MLP_training_data.csv" and "MLP_val_data.csv" files. The goal is to illustrate the recurrent neural network presented in the referred citation (Dourado and Viana PHM 2019). In this example, we did not pursue optimizing any of the training parameters (multilayer perceptron configuration, learning-rate, number of epochs) to accurately reproduce the results illustrated in the manuscript. Nevertheless, we strongly encourage the user to experiment with the code in order to reproduce or even surpass the mentioned results.

## Citing this repository

Please, cite this repository using: 

    @misc{2019_dourado_viana_python_corrosion_fatigue,
        author    = {A. Dourado and F. A. C. Viana},
        title     = {Python Scripts for Physics-Informed Neural Networks for Corrosion-Fatigue Prognosis},
        month     = Aug,
        year      = 2019,
        doi       = {10.5281/zenodo.3355729},
        version   = {0.0.1},
        publisher = {Zenodo},
        url       = {https://github.com/PML-UCF/pinn_corrosion_fatigue}
        }
The corresponding reference entry should look like:

A. Dourado and F. A. C. Viana, Python Scripts for Physics-Informed Neural Networks for Corrosion-Fatigue Prognosis, v0.0.1, Zenodo, https://github.com/PML-UCF/pinn_corrosion_fatigue, doi:10.5281/zenodo.3355729.
