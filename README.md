# Pathfinding Project

## About


The project consists in a implementation of the four well known pathfinding algorithms to create a navigation path between 2 points around Manhattan.

Algorithms used:

- Breadth First 
- Best-First-Search
- A*
- Dijkstra

## Start

- The project uses Python, Jupyter and Docker.

- Use the `map_osmnx.ipynb` notebook to run the project.


------


## Installation


First, install [docker](https://www.docker.com/). 

The OSMnx docker container image and usage instructions are available on [docker hub](https://hub.docker.com/r/gboeing/osmnx).

Usage

#### Pull the container image

`docker pull gboeing/osmnx`


#### Run the docker container


On Windows open a command prompt, change directory to location of notebook file, and run:

  `docker run --rm -it --name osmnx -p 8888:8888 -v %cd%:/home/jovyan/work gboeing/osmnx`
  
On Mac/Linux open a terminal window, change directory to location of notebook file, and run:

  `docker run --rm -it --name osmnx -p 8888:8888 -v "$PWD":/home/jovyan/work gboeing/osmnx`


#### Run a Jupyter notebook


Once the container is running as described above, open your computer's web browser and visit http://localhost:8888.

To run bash in this container

On Windows:

  `docker run --rm -it -u 0 --name osmnx -v %cd%:/home/jovyan/work gboeing/osmnx /bin/bash`

On Mac/Linux:

  `docker run --rm -it -u 0 --name osmnx -v "$PWD":/home/jovyan/work gboeing/osmnx /bin/bash`


## Overview

**OSMnx** is a Python package that lets you download spatial geometries and
model, project, visualize, and analyze street networks from OpenStreetMap's
APIs. Users can download and model walkable, drivable, or bikable urban
networks with a single line of Python code, and then easily analyze and
visualize them:

```python
import osmnx as ox
G = ox.graph_from_place('Manhattan Island, New York City, New York, USA', network_type='drive')
ox.plot_graph(G)
```
![](/docs/figures/manhattan.png)

In a couple lines of code you can examine intersection density, network
circuity, average block size, PageRank, betweenness centrality, connectivity,
spatial distribution of dead-ends or 4-way intersections, etc for anywhere in
the world:

```python
basic_stats = ox.basic_stats(G)
print(basic_stats['circuity_avg'])

extended_stats = ox.extended_stats(G)
print(extended_stats['pagerank_max_node'])
```

You can just as easily download and work with building footprints, elevation
data, street bearings/orientations, and network routing.



## Documentation

Documentation available at [readthedocs](https://osmnx.readthedocs.io).

Examples available in the [examples repo](https://github.com/gboeing/osmnx-examples).

