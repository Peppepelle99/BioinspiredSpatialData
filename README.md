[Log files]: https://drive.google.com/drive/folders/1Ede9fJmXHnCEz62aHWoU3I9lkkEsXb4f?usp=sharing

This is the repository for the project "Bioinspired Spatial Data". \
Log files for all NNI experiments and Fast-Denser are available [here][Log files]. \
The report file for the project is available [here](./report.pdf).

# Usage
## PyTorch+SNNTorch: NNI experiments (local)
1. Clone the repository
2. Install the requirements 
3. Move to `nni_configs` folder
4. Select the configuration file for the experiment you wish to perform, and then execute the following command: \
  ```nnictl create --config <config_file>.yml --port 5001```

## Keras+NengoDL: NNI experiments (local)
1. Clone the repository
2. Install the requirements
3. Move to `src/nengo_conversion` folder
4. Execute the following comand: \
    ```nnictl create --config nni_snn_config.yml --port 5001```

# Test
In `test` folder there are notebooks to test the code, specifically Fast-Denser net search, all the NNI experiments performed in this project and then models evaluation for Pytorch+SNNTorch pipeline. Please download it and run it on Google Colab. \
**NOTE:** the results that comes out from Colab are slightly different in terms of accuracy and training time from the ones that come from experiments performed locally with a NVIDIA GTX 1080Ti.

# Experiment log summary on PyTorch CNN + SNNTorch pipeline:
[Here][Log files] are the logs of the NNI experiments. Following that, a summary of the experiments and trials. In the same folder, there are also CSV file generated by Fast-Denser framework to find **CNN_K**.

## CNN experiments for searching hyper parameters:
- **CNN_PT_1** hyperparameters: trial `pOdyC`
- **CNN_PT_2** hyperparameters: trial `hndeI`

## SNN experiments (optimized with MSE Count Loss, without weight transfer): 
- **QrbKOuWJ** experiments on **SNN_PT_2**
- **1RSZuxno** experiments on **SNN_PT_1**

## SNN experiments (optimized with Cross Entropy Count Loss, with weight transfer):
- **Z19hnw4u** experiments on **SNN_PT_1**
  - Best accuracy: trial `U6mOB`
  - Best tradeoff accuracy/num_steps: trial `yxecs`
- **ZdQn9mbD** experiments on **SNN_PT_2**
  - Best accuracy: trial `lcOk8`
  - Best tradeoff accuracy/num_steps: trial `CQdzk`

# Experiment log summary on Fast-Denser3+Nengo-DL pipeline:
- **fykmsgad**, NNI experiments on **SNN_K**:
  - Best accuracy: trial `PJTSF`



