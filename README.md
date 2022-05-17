# Testing VAE Robustness Against Semantic Transformations
This is the repository for the CS 521 project on Testing the Robustness of Variational Autoencoders Against Semantic Transformations by Rem Yang and Steven Pan.

## Setup
To test VAEs, only the following libraries are needed: `torch`, `numpy`, `scipy`, `matplotlib`.
To also train VAEs, please run: `pip install -r PyTorch-VAE/requirements.txt`

While the MNIST dataset should be automatically downloaded by torchvision's in-built dataset module, you may encounter errors when using the CelebA dataset. Please manually download the dataset from [this link](https://drive.google.com/file/d/1m8-EBPgi5MRubrm6iQjafK2QMHDBMSfJ/view?usp=sharing) and unzip it into the `Pytorch-VAE/Data` directory.

## Running Experiments
**Testing VAEs:** We provide pretrained VAEs for MNIST and CelebA in the `PyTorch-VAE/logs` directory, which are the networks used in our experiments. Reproducing our results is as simple as running the cells in `Test-VAE.ipynb` (which is annotated with explanations for each part of the code). The figures shown in our report are in the `results` directory.
**Training VAEs:** For training, we utilize the [PyTorch-VAE codebase](https://github.com/AntixK/PyTorch-VAE). To train a VAE, you need to run `cd Pytorch-VAE` then `python run.py configs/vae.yaml`. Currently, the codebase is setup to train an MNIST network. To train a CelebA network instead, go to `Pytorch-VAE/dataset.py` and comment out the part marked in `++ MNIST Dataset ++` and uncomment the part marked in ` == CelebA ==`.
