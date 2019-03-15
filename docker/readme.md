# OSMnx Docker Image

First, install [docker](https://www.docker.com/). 

The OSMnx docker container image and usage instructions are available on [docker hub](https://hub.docker.com/r/gboeing/osmnx).

Usage
Run the docker container

On Windows open a command prompt, change directory to location of notebook file, and run:

  `docker run --rm -it --name osmnx -p 8888:8888 -v %cd%:/home/jovyan/work gboeing/osmnx`
  
On Mac/Linux open a terminal window, change directory to location of notebook file, and run:

  `docker run --rm -it --name osmnx -p 8888:8888 -v "$PWD":/home/jovyan/work gboeing/osmnx`

Run a Jupyter notebook

Once the container is running as described above, open your computer's web browser and visit http://localhost:8888.

To run bash in this container

On Windows:

  `docker run --rm -it -u 0 --name osmnx -v %cd%:/home/jovyan/work gboeing/osmnx /bin/bash`

On Mac/Linux:

  `docker run --rm -it -u 0 --name osmnx -v "$PWD":/home/jovyan/work gboeing/osmnx /bin/bash`
