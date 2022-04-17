<div id="top"></div>

<div style="text-align:center"><img src="images/cover2.jpg" /></div>

<!-- ABOUT THE PROJECT -->
## 1. Introduction

### 1.1 Overview

This project focuses on the development and analysis of a simplified neural
model that captures the core features of brain dynamics. Utilizing mathematical
equations and computational simulations, the model provides insights into the
fundamental aspects of neural activity and behavior.


### 1.2 Goal

Utilize mathematical and computational modeling to decipher fundamental aspects
of neural dynamics within the brain.


### 1.3 Model

A collection of interconnected equations that dictate a streamlined depiction of
the brain's structure and function.


### 1.4 Background

Science and inspiration by - [E.M.
Izhikevich](https://www.izhikevich.org/publications/spikes.htm)


<p align="right">(<a href="#top">back to top</a>)</p>


## 2 Simulations

## 2. Simulating One Brain Cell

1. Import libraries:

- numpy is imported as np for numerical operations.
- matplotlib.pyplot is imported as plt for plotting the results.


2. Define the parameters:

- a, b, c, and d are parameters for the neuron model.
- v represents the initial membrane potential.
- u is initialized as the product of b and v.

3. Initialize variables for the simulation:

- simulation_time is set to 1000, representing the total time for the simulation.
- memvolt and Iall are NumPy arrays initialized with zeros, which will store the
membrane voltage and stimulation values, respectively, for each time step.

4. Run the simulation:

- A loop iterates through the simulation_time.
- The variable I represents the external input to the neuron, which is set to -2
between time steps 200 and 400 and 7 otherwise.
- If the membrane potential v reaches or exceeds 30 mV, an action potential
occurs, causing v to reset to the value of c, and u is updated by adding d.
- The membrane voltage v and variable u are updated using the given equations.
- The updated membrane voltage v and input I are stored in their respective arrays
at the current time step.

5. Plot the results:

- A figure and axes are created using plt.subplots().
- The membrane potential (memvolt) and stimulation (Iall) are plotted against time.
- The x-axis is labeled 'Time (ms)', and the y-axis is labeled 'Membrane voltage (mV)'.
- The plot is displayed using plt.show().


The result is a visual representation of the neuron model's membrane potential
over time, allowing you to observe how the neuron responds to the input
stimulation.

<p align="center">
  <img src="images/ss0.png">
</p>



















<!-- CONTRIBUTING -->
## Contributing

If you would like to add any extra features to the optimisation simulation, feel free to fork and create a pull request. Thank you!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- CONTACT -->
## Contact

Erol Gelbul - [Website](http://www.erolgelbul.com) - erolgelbul@gmail.com

Project Link: [The Brain](https://github.com/ErolGelbul/the_brain)

<p align="right">(<a href="#top">back to top</a>)</p>
