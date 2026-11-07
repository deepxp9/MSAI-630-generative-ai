# MSAI-630 – Generative AI with Large Language Models

Course projects built on the notebooks from David Foster, *Generative Deep Learning* (2nd ed.)
([book repository](https://github.com/davidADSP/Generative_Deep_Learning_2nd_Edition)).
Both notebooks were run on Google Colab (T4 GPU) and are saved with their outputs.

| Notebook | Project | Highlights |
|---|---|---|
| [`cgan_blond_hair.ipynb`](cgan_blond_hair.ipynb) | **Project 1 – Conditional GAN** (conditional WGAN-GP on CelebA, conditioned on `Blond_Hair`) | `train_step` modified so the generator gets a one-hot label `(batch, 2)` and the critic an image-shaped label map `(batch, 64, 64, 2)`. A separate classifier shows a **conditional accuracy of 85.9%** (87.0% of "blond" faces classified blond vs 15.2% of "not blond" faces). |
| [`lstm_recipes.ipynb`](lstm_recipes.ipynb) | **Assignment 4 – LSTM text generation** (Epicurious Recipes) | Text cleaned and tokenized (10,000-word vocabulary), LSTM trained for 25 epochs (loss 4.16 → 1.53), recipes generated word by word at **temperature 0.5 and 1.5** and compared. |

## Running the notebooks
Open a notebook in Google Colab, choose **Runtime ▸ Change runtime type ▸ GPU**, and select **Run all**.
The datasets are downloaded automatically with `kagglehub`
(`jessicali9530/celeba-dataset`, `hugodarwood/epirecipes`).

*Note: the images in the CGAN notebook are stored as JPEG to keep the file small enough to view on GitHub.*
