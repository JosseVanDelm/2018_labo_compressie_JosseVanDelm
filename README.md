Labo Compressie 2018
====================
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

# progress 7-12-2018
So today we found out that the docker image doesn't use gpu, which makes training of the convolutional autoencoder very slow!
link: https://blog.keras.io/building-autoencoders-in-keras.html
