Labo Compressie 2018
====================
a project for [B-KUL-YI1328](https://onderwijsaanbod.kuleuven.be/syllabi/n/YI1328N.htm#activetab=doelstellingen_idp13619536)

# Usage
**tested on ubuntu 18.04**


* clone this repo `git clone https://github.com/JosseVanDelm/2018_labo_compressie_JosseVanDelm.git`
* install all dependencies for keras docker container e.g. `nvidia-docker` (cf. KerasREADME.md)
* run `make notebook` (note token output on terminal)
* go to `http://localhost:8888/` in a webbrowser, enter token from previous step here
* upload both `.ipynb`-files of this directory to the notebook.
* open the `Convolutional Autoencoder (Training).ipynb` file, this is the training-script.
Start the training process. (*takes about 30 minutes on CPU, and about 4 on GPU, depending on your system*)
* open the `Encoder and Decoder.ipynb` file.
This file uses the trained weights from the training phase to encode and decode any given image.
**You will notice however that this last script doesn't always provide the wanted outcome :(**
