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

Waveforms of IV_in and IV_out indicating rising delay and falling delay of Inverter:

![InvPlot1](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/072a6f3b-bf56-4126-b29b-dfbfa89fa212)

Inverter Delay Table:

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/aa838020-36f7-4d44-8f98-ddbe90e9d6d6)

Inverter AC Simulations:

![Current values](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/625ef5b8-8ca8-46e2-a0f6-511fd22d496b)

AC Simulation Table:

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/76f33f4c-d7ef-4d57-867e-a22bbb7573b6)

Sink Capacitance: 3.27421E-15 (3.27fF)

Cell Characterization for NAND:

Waveforms of IV_in and IV_out indicating rising delay and falling delay of NAND:

![NAND2_output1](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/fced1285-7602-49d4-8ede-abe892fe5ac5)

NAND Delay Table:		

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/596ccefa-19a4-4e3c-aa31-c941d716671f)

![NAND2_delay](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/caf6a88b-5b8e-4048-99ff-04043c9901f2)

AC Simulations:

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/250814d7-36a3-4212-8cb3-6e1c4de914dd)

Sink Capacitance: 4.33519E-15 (4.33fF)

![NAND simcap](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/644b0327-3b8f-4f58-b443-f5b0a7ee8782)

Cell Characterization for XOR:

Waveforms of IV_in and IV_out indicating rising delay and falling delay of XOR:

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/c2a02829-0b42-44e0-bc2a-d436f0cb706c)

Delay Table:

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/056e5081-6c5f-425f-86ac-296a56b6e86f)

AC Simulations:

Frequency Delay Table		

![image](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/e60cc390-b777-4bd6-9329-cb66e58da18c)

![Finalplot](https://github.com/RoshiniUdayaKumar/Cell-Characterization-using-Spectre/assets/133715179/ba866560-83ce-41fe-a21d-c1f7d32dc9f7)

Notes on writing the files:

1.The cell.spi file is the standard cell description file which is written in the spectre format.

The cell under consideration is written as a sub-circuit defining the inputs and outputs.

We could use M1,M2 as the naming conventions for the transistors.

We will also define the terminals of these transistors in the order of drain, gate, source and body.

We could also define the length(l) and width(w).

2.Simulation file:

We shall include the libraries required to run the simulation (which is a model card ie., model.spi and cell sub circuit which is cell.spi)

We shall include the voltage sources VDD and GND and the node declaration is done as: 

Name (node1 … nodeN) master [ [param1 = value1] … [paramN = valueN] ]

To observe the outputs, lets include vpwl which is a voltage piecewise linear waveform. 

The standard cells are denoted as X1 and the connection of its terminals are defined following the convention as above.

Component R1 is a resistor with 1Ω.

Component C1 is a capacitor with 100fF. Note ‘f’, femto, indicate 1.0e-15.

The last two sentences claim the running time and the step accuracy of the simulation.

