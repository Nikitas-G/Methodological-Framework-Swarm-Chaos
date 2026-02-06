CADI Framework
This repository contains the code for CADINet, a neural network that predicts how stable a swarm of robots will be when moving through a city.

Instead of running slow simulations every time, we use this model to get a "stability score" (CADI) just by looking at the map's geometry.

What it does:
Predicts stability: Uses city map data (from nuScenes) to see if a swarm will keep its cohesion.
Fast processing: Replaces heavy physics simulations with a quick neural network.
Real-world data: Tested on 17,698 actual road layouts from Singapore and Boston.
