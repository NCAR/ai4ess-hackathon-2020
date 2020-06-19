# AI4ESS Summer School Hackathon 2020

This repository contains Jupyter notebooks for the challenge problems of the 2020 [AI for Earth System Science Summer School](https://www2.cisl.ucar.edu/events/summer-school/ai4ess/2020/artificial-intelligence-earth-system-science-ai4ess-summer-school). 

## Contributors
* Aaron Bansemer
* Charlie Becker
* Chih-Chieh (Jack) Chen
* David John Gagne
* Gabrielle Gantos
* Andrew Gettelman
* Matt Hayman
* Alma Hodzic
* Karthik Kashinath
* Rich Loft
* Keely Lawrence
* Taysia Peterson
* Gunther Wallach
* Siyaun Wang

## Challenge Problems

* GOES [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NCAR/ai4ess-hackathon-2020/blob/master/notebooks/goes16.ipynb): Predict the probability of lightning in the next hour from GOES-16 infrared imagery.

* HOLODEC [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NCAR/ai4ess-hackathon-2020/blob/master/notebooks/holodec.ipynb): Accelerate the processing of an airborne holographic cloud particle imager with deep learning.

* GECKO [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NCAR/ai4ess-hackathon-2020/blob/master/notebooks/gecko.ipynb): Emulate the GECKO-A complex organic chemistry model with a simpler machine learning approach.

* Microphysics [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NCAR/ai4ess-hackathon-2020/blob/master/notebooks/microphysics.ipynb): Emulate the warm rain processes within the Tel Aviv University (TAU) spectral bin microphysics scheme for use within the Community Atmosphere Model.

## Requirements
The hackathon notebooks require the following Python libraries and at least Python 3.7 installed:
* numpy
* pip
* scipy
* matplotlib
* pandas
* tqdm
* s3fs
* pyyaml
* netcdf4
* xarray
* h5netcdf
* dask
* pyarrow
* tensorflow
* scikit-learn
* goes16ci
* mlmicrophysics
* jupyter

## Setup
The hackathon notebooks can be run from 3 platforms: Jupyterhub, Google Colab, and locally. Jupyterhub and Google Colab run entirely within the browser, so all you will require is a modern internet browser and a strong web connection. Advanced users can install and run on their local machine, but deep learning training performance may be degraded by the lack of GPU.

### Jupyterhub
If you registered for the hackathon, we will send you an email with a link to the jupyterhub website. There you can log in with the Gmail or G-Suite account you provided at registration. A progress bar will then appear, followed by a Jupyter lab instance. The notebooks will be preinstalled in the ai4ess-hackathon-2020/notebooks directory. Your instance come with 30 GB of storage that will persist over the course of the Hackathon even if you log out. Tensorflow and scikit-learn are the main ML libraries being used in the Hackathon. PyTorch is also installed on 

### Google Colab
If you are not part of the hackathon, you can still run the hackathon notebooks in the cloud through Google Colab. For a given hackathon problem, click the Open in Colab link above to open a challenge problem notebook in Colab. To install needed dependencies, run the `! pip install ...` cell at the beginning of the notebook. If you want to save the changes you made to a notebook, under the File menu you can save to Google Drive, Github, or your local computer. 

### Local Machine
You can also run the notebooks on your own computer or a remote cluster. First install [Miniconda](https://docs.conda.io/en/latest/miniconda.html). Then install the main dependencies with 

`conda install -c conda-forge numpy scipy matplotlib pandas tqdm s3fs pyyaml netcdf4 xarray h5netcdf dask pyarrow scikit-learn jupyter ipython pip`. 

You will need need pip to install the remaining libraries: 

`pip install tensorflow goes16ci mlmicrophysics`. 

Next, clone this repository locally with 

`git clone https://github.com/NCAR/ai4ess-hackathon-2020.git`.

Finally start Jupyter Lab in your home directory

`jupyter lab`

Inside jupyter lab navigate to ai4ess-hackathon-2020/notebooks to access the hackathon notebooks. You will need internet access to load the data. **Some of the datasets are 10-20 GB in size, so please be careful about streaming or downloading them locally if you have data caps from your internet service provider.**