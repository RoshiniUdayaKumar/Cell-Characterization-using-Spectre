# Cell-Characterization-using-Spectre

Characterizing and simulating the behavior of the pre-designed cells under various operating conditions is referred to as cell library characterization.

Cell design is commonly taken as SPICE circuit and SPICE technology models for cell library characterization.
The objective is to develop precise and accurate models that describe the electrical properties and performance parameters of the cells. Key electrical characteristics of the cells, including propagation delay, power consumption, input and output voltage levels, and noise margins, are measured and extracted during the characterization process. Specialized test circuits and equipment are used for this. The performance of the cell is then precisely represented by timing models, power models, and other behavioral models that are developed using the collected data.

Although there are many different characteristics that go into cell characterisation, some of the more important ones are propagation delay, power, area, timing restrictions. For sequential elements, input capacitance, and global parameters like PVT (Process, Voltage, Temperature), corner selection, etc. are crucial parameters. Conducting circuit simulations at the transistor level, we will only be addressing the propagation delay and input capacitance of a conventional cell in this project.

Steps: 
1. We will use Cadence Spectre as a simulation tool. 
Creating a time-domain system based on a collection of state variables and then solving it through numerical computation is the fundamental concept behind SPICE simulation. Among all established methods for circuit simulation, SPICE simulation has the highest accuracy. 

2. Writing simulation files using Spectre simulation language and running the simulations.
In this file, you need to define the netlist of your circuit, including necessary libraries, and write simulation controls.
3. The output is observed in WV(Waveform Viewer)


