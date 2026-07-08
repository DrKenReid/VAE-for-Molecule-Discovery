# Variational Autoencoder for Molecule Discovery

A Variational Autoencoder (VAE) that learns a continuous latent representation of molecular structures and generates novel candidates. Trained on the QM9 benchmark dataset using SMILES notation, with validity and novelty assessment of generated molecules.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrKenReid/VAE-for-Molecule-Discovery/blob/main/Variational_Autoencoder_for_Molecule_Discovery.ipynb)

## Techniques Demonstrated

| Category | Details |
|---|---|
| **Generative Modelling** | Variational Autoencoder with KL-divergence regularisation |
| **Molecular Representation** | SMILES encoding/decoding, character-level tokenisation |
| **Deep Learning** | PyTorch GRU-based encoder/decoder, teacher forcing, KL annealing, mixed-precision training, latent-space sampling and interpolation |
| **Cheminformatics** | RDKit molecule parsing, canonicalisation, property calculation, structure visualisation |
| **Evaluation** | Train/validation/test split, held-out reconstruction accuracy, raw (unrepaired) validity, canonical novelty against the training set, property distributions |
| **Reproducibility** | Fixed random seeds, version-pinned dependencies, deterministic data splits |
| **Dataset** | QM9 — standard benchmark for small organic molecules |

## How to Use

1. Open the notebook in Google Colab using the badge above (GPU recommended for faster training).
2. Run cells in order (*Runtime → Run all*) — the QM9 dataset is downloaded automatically and split into train/validation/test sets.
3. The notebook walks through environment setup, data preprocessing, model training (with a validation loop), and molecule generation.
4. Generated molecules are visualised with RDKit and assessed for reconstruction accuracy, raw validity, and canonical novelty; a latent-space interpolation shows the smoothness of the learned representation.

> The committed notebook has its outputs cleared — run all cells in Colab to regenerate them.

## Configuration

Key parameters you can adjust:

- `hidden_dim` — GRU hidden state dimension
- `latent_dim` — latent space dimensionality
- `batch_size` — training batch size
- `num_epochs` — number of training epochs
- `SEED` — global random seed for reproducible splits, training, and sampling

## A Note on Molecular Generation

Generating valid SMILES strings is a hard problem — the syntax is strict, and most random character sequences are chemically meaningless. The VAE learns to navigate this by encoding known molecules into a smooth latent space where nearby points tend to decode into similar, valid structures. This is the core insight behind latent-space drug discovery: instead of searching a discrete combinatorial space, you optimise over a continuous manifold. The gap between "valid molecule" and "viable drug candidate" remains vast, but the approach demonstrates why generative models have become central to computational chemistry.

## License

This project is open-source and available under the [MIT License](LICENSE).

## Related

- [CNN X-ray Image Classifier](https://github.com/DrKenReid/CNN-Tutorial---X-ray-image-classifier) — deep learning for medical imaging
- [Generalized Analysis of Text Data](https://github.com/DrKenReid/Generalized-Analysis-of-Text-Data) — NLP reference notebook with 13 techniques
- [kenreid.co.uk/data_science](https://www.kenreid.co.uk/data_science.html) — all projects, publications, and CV

## Author

**Ken Reid** — Data Scientist, photographer, and avid reader.

- [kenreid.co.uk](https://www.kenreid.co.uk) — Portfolio & blog
- [@kenreid.co.uk](https://bsky.app/profile/kenreid.co.uk) — Bluesky
- [@DrKenReid](https://github.com/DrKenReid) — GitHub
