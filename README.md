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

## 2.1 Simulating One Brain Cell

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

## 2.2 Simulating 1000 Neurons

This section represents the implementation of a neural circuit consisting of
1000 neurons, including both excitatory and inhibitory neurons. The code sets up
the parameters and initial conditions for the neural circuit and defines the
synaptic weights matrix.

1. Define the number of neurons:

- Ne represents the number of excitatory neurons (800).
- Ni represents the number of inhibitory neurons (200).

2. Generate random values for re and ri:

- re is an array of random values of size Ne (800) for excitatory neurons.
- ri is an array of random values of size Ni (200) for inhibitory neurons.

3. Set up parameters for the neurons:

- a, b, c, and d are arrays representing the parameters for each neuron in the
circuit. The np.hstack() function is used to concatenate the values for
excitatory and inhibitory neurons.

The parameters for excitatory neurons are based on the random values in re,
while those for inhibitory neurons are based on the random values in ri.

4. Initialize membrane potential v and variable u:

-v is initialized as an array of -65 mV for all neurons, both excitatory and
inhibitory.
- u is computed as the product of the b parameter and v.

5. Define the synaptic weights matrix S:

- S is a matrix of size (Ne+Ni, Ne+Ni) representing the all-to-all synaptic
weights between neurons in the circuit.
- The first part (.5*np.random.rand(Ne+Ni, Ne)) represents the synaptic weights
between excitatory neurons and all neurons in the circuit. The values are
randomly generated and scaled by 0.5.
- The second part (-np.random.rand(Ne+Ni, Ni)) represents the synaptic weights
between inhibitory neurons and all neurons in the circuit. The values are
randomly generated and negated to indicate inhibitory connections.

In summary, this code sets up a neural circuit of 1000 neurons with distinct
excitatory and inhibitory properties, initializes the membrane potential and
variable u, and defines the synaptic weights matrix for all-to-all connections.


## 2.3 Visualize

This code snippet is responsible for visualizing the firing activity of the
neurons in the circuit using a raster plot. It displays a plot where the x-axis
represents time (in milliseconds), and the y-axis represents the neuron number
(1 to 1000). Each dot in the plot corresponds to a firing event, with the neuron
number on the y-axis and the time of firing on the x-axis.


1. Create a figure and axes:
   - fig, ax = plt.subplots(1, figsize=(10, 7)): This line creates a new figure with one subplot (axes) and sets the figure size to 10 inches wide and 7 inches tall. 
   
2. Plot the firing events:
   - plt.plot(firings[0, :], firings[1, :], 'k.', markersize=1): This line plots the firing events as black dots (indicated by 'k.') with a marker size of 1. The time of firing is retrieved from the first row of the firings array (firings[0, :]), while the neuron number is retrieved from the second row (firings[1, :]).

3. Set the axis labels:
   - plt.xlabel('Time (ms)'): This line sets the x-axis label to "Time (ms)".
   - plt.ylabel('Neuron #'): This line sets the y-axis label to "Neuron #".

4. Display the plot:
   - plt.show(): This line displays the generated raster plot.

The resulting raster plot provides a visual representation of the firing activity of each neuron in the circuit over time, allowing for the observation of patterns and dynamics within the neural circuit.

<p align="center">
  <img src="images/ss1.png">
</p>


## 2.4 Visualize the Population Spiking Activity


















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
