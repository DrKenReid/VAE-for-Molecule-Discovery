# 🧪 Variational Autoencoder for Molecule Discovery

## 🔍 Overview
This project implements a Variational Autoencoder (VAE) for generating novel molecular structures. It's particularly useful in drug discovery, where the goal is to generate new potential drug candidates. The project is designed to run in Google Colab, leveraging GPU acceleration for efficient training and generation.

## ✨ Features
- **🧠 VAE Architecture**: Utilizes a Variational Autoencoder to learn a compact representation of molecular structures and generate new ones.
- **🧬 SMILES Representation**: Uses SMILES (Simplified Molecular-Input Line-Entry System) strings for molecular representation.
- **📊 QM9 Dataset**: Trains on the QM9 dataset, a standard benchmark in molecular machine learning.
- **👁️ Molecule Visualization**: Generates and visualizes molecular structures using RDKit.
- **⚗️ Property Calculation**: Computes basic molecular properties for generated molecules.
- **✅ Validity and Novelty Checks**: Assesses the validity of generated molecules and checks for novelty against the training set.
- **☁️ Google Colab Integration**: Designed to run in Google Colab for easy access to GPU resources.

## 🛠️ Requirements
- Google Colab environment
- Required libraries (automatically installed in the notebook):
  - PyTorch
  - RDKit
  - Pandas
  - Pillow
  - IPython

## 🚀 Usage
1. Open the notebook in Google Colab.
2. Run the cells in order, following the instructions in the notebook.
3. The notebook will guide you through:
   - Setting up the environment
   - Loading and preprocessing the QM9 dataset
   - Defining and training the VAE model
   - Generating new molecules
   - Visualizing and analyzing the generated molecules

## ⚙️ Configuration
You can modify the following parameters in the notebook:
- `hidden_dim`: Dimension of the hidden state in GRU layers
- `latent_dim`: Dimension of the latent space
- `batch_size`: Batch size for training
- `num_epochs`: Number of training epochs

## 📤 Output
The notebook generates several outputs:
1. Training loss plots
2. Generated SMILES strings
3. Visualizations of generated molecules
4. Analysis of molecular properties
5. Validity and novelty statistics

## ⚠️ Limitations
- The model's performance is limited by the size and diversity of the training dataset (QM9).
- Generated molecules may not always be synthetically feasible or stable.
- The current implementation focuses on small organic molecules.

## 🤝 Contributing
Contributions, issues, and feature requests are welcome. Feel free to open an issue or submit a pull request.

## 📄 License
This project is open-source and available under the MIT License.

## ⚖️ Disclaimer
This tool is for research and educational purposes only. Generated molecules should not be considered as actual drug candidates without further extensive testing and validation.
