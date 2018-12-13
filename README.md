Labo Compressie 2018
====================
a project for [B-KUL-YI1328](https://onderwijsaanbod.kuleuven.be/syllabi/n/YI1328N.htm#activetab=doelstellingen_idp13619536)

# Usage FINAL VERSION
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







---
# LOGBOOK

This is my attempt on building an autoencoder in keras.
https://www.datacamp.com/community/tutorials/autoencoder-keras-tutorial

# Installation:
So I am still not really into docker, I' m pretty sure there is an easier way to do this, but hey this works as wel lol:
1. `docker pull ermaker/keras-jupyter`
2. `docker run -d -p 8888:8888 -v /notebook:/notebook ermaker/keras-jupyter`
3. browse for `http://localhost:8888/`
3. `docker container ls` note name of container
4. `docker exec -it <container name> bash` go into container
5. For some reason additional installation steps are required:
	* `pip install np_utils`
	* `pip install tensorflow --upgrade`
6. have fun!

# Progress 7-12-2018
So today we found out that the docker image doesn't use gpu, which makes training of the convolutional autoencoder very slow!
link: https://blog.keras.io/building-autoencoders-in-keras.html

# Progress 8-12-2018
Just found out `nvidia-docker` has to be installed to make use of gpu in docker.
We are going to use the keras docker image with makefile, as found on: https://github.com/keras-team/keras/blob/master/docker

# Progress 12-12-2018
Some code to download datasets from imagenet:
* `wget -i list_of_images.txt --no-clobber --timeout=1 --tries=1`
* `watch -d du -s imagenet/`
