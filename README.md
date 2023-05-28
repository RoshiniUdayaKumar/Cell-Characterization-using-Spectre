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

Results:
Cell Characterization for Inverter:
![InvPlot1](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/072a6f3b-bf56-4126-b29b-dfbfa89fa212)

Inverter Delay Table:

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/aa838020-36f7-4d44-8f98-ddbe90e9d6d6)

Inverter AC Simulations:

![Current values](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/625ef5b8-8ca8-46e2-a0f6-511fd22d496b)

AC Simulation Table:

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/76f33f4c-d7ef-4d57-867e-a22bbb7573b6)

Sink Capacitance: 3.27421E-15 (3.27fF)
