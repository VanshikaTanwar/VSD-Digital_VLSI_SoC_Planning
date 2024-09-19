# VSD-Digital_VLSI_SoC_Planning
NASSCOM DIGITAL SOC PROGRAM

# Table of Contents

- [Design](#Design)
- [Open Source Digital ASIC Design](#Open-Source-Digital-ASIC-Design)
- [Openlane](#Openlane)
- [OpenLANE ASIC Flow](#OpenLANE-ASIC-Flow)
- [OpenLane ](#OpenLane)
- [OpenLane design stages](#OpenLane-design-stages)
- [Day 1](#Day-1)
	- [Design Preparation Steps](#Design-Preparation-Steps)




## OpenLane 

OpenLane is an automated RTL to GDSII flow based on several components including OpenROAD, Yosys, Magic, Netgen, Fault and custom methodology scripts for design exploration and optimization.
For more information check [here](https://openlane.readthedocs.io/)

![openlane flow 1](https://user-images.githubusercontent.com/80625515/130246106-18f73ccc-e8e1-4061-a1b0-8c14bdf711f1.png)

### OpenLane design stages

1. Synthesis
	- `yosys` - Performs RTL synthesis
	- `abc` - Performs technology mapping
	- `OpenSTA` - Performs static timing analysis on the resulting netlist to generate timing reports
2. Floorplan and PDN
	- `init_fp` - Defines the core area for the macro as well as the rows (used for placement) and the tracks (used for routing)
	- `ioplacer` - Places the macro input and output ports
	- `pdn` - Generates the power distribution network
	- `tapcell` - Inserts welltap and decap cells in the floorplan
3. Placement
	- `RePLace` - Performs global placement
	- `Resizer` - Performs optional optimizations on the design
	- `OpenDP` - Perfroms detailed placement to legalize the globally placed components
4. CTS
	- `TritonCTS` - Synthesizes the clock distribution network (the clock tree)
5. Routing
	- `FastRoute` - Performs global routing to generate a guide file for the detailed router
	- `CU-GR` - Another option for performing global routing.
	- `TritonRoute` - Performs detailed routing
	- `SPEF-Extractor` - Performs SPEF extraction
6. GDSII Generation
	- `Magic` - Streams out the final GDSII layout file from the routed def
	- `Klayout` - Streams out the final GDSII layout file from the routed def as a back-up
7. Checks
	- `Magic` - Performs DRC Checks & Antenna Checks
	- `Klayout` - Performs DRC Checks
	- `Netgen` - Performs LVS Checks
	- `CVC` - Performs Circuit Validity Checks

# Introduction
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215343706-7823e1b9-93a4-4fd6-a22e-8f2cf3197330.jpg"></br>
   fig.1: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215343958-2c3ea6f8-b47e-4894-928b-5dc268a1f573.png"></br>
   fig.2: 
</p>

We usually in our daily life calling this thing as a chip but in industrial terms it is known as package.

And package are named as a QFN-48 or QUAD Flat No leads.

The size of this package is 7mm and 7mm.


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344029-f7e05b67-2bb1-456c-810d-da644b70e0c5.png"></br>
   fig.3: 
</p>

There is a chip which is assembled at the centre of the package and the chip is connected in this way as shown below.

And these connectrions are used to send the outside world signals or external signals to the chip

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344053-2ce6bab5-c95c-4627-baec-e7e7957f28f8.png"></br>
   fig.4: 
</p>

Inside this chip there are various components Die,pads,core,etc.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344362-2b689123-76e6-4dd2-9769-8514387247c3.png"></br>
   fig.5: 
</p>

PADS
Pads are something through which we can send the signal inside the chip or any signal can go outside from inside the chip to the outside through this pads .

Core
Core of the chip
Core is basically consist of different logics . A core is that place where all the digital logics are made or placed in this area like And ,or logic,etc.

Die
Die is basically the area of the chip . It is called as that die which is manufactured at the silicon wafer .





A typical Chip or an idea chip consist of SOC,SRAm,ADC,DAC,PLL,SPI and a couple of components.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344396-dbd9b676-807c-4863-b43a-93cd1fc6bd7b.png"></br>
   fig.6: 
</p>

Foundry IP’s

The word foundry means in terms of chip designing is factory .
It is a type of factory which consist of some machines and it is that place our chips actually got manufactured or fabricated .And IP here means is intellectual property .It is something which has some intelligence means an organization has made it with some unique intelligence which is new in market ,or which is latest which is updated , as others cannot have the right to copy it if anyone try to copy then copyright issue will be created to that person.

Macros 
Digital blocks here are called MACROS.Macros are basically a pure digital logic.As, shown in the figure below:- 
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/7a92c53f-d03d-45fc-b334-748dfb6151d7.png"></br>

   fig.7: 
</p>


# Open Source Digital ASIC Design

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344432-6bbbddcb-1bcb-4587-babd-9d3cccd248df.png"></br>
   fig.8: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344481-18fb4d53-2f78-479c-9996-ca91585c71b1.png"></br>
   fig.9: 
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344507-1f98e2a6-71ac-42ca-ac52-3c482bb5b090.png"></br>
   fig.10: 
</p>

# Openlane

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215344549-8040b71c-7584-4bf2-af4a-00145baef992.png"></br>
   fig.11: 
</p>

The main goal of using openlane is “To produce a clean GDSII with no human intervention (no-human-in-the-loop)

Here, clean means:-

    • No LVS Violations

    • No DRC Violations
    
    • No Timing Violations 

    
    • Openlane can also be used for harden macros and chips harden means to generate the GDSII Flow or Final Layout. 
   
    • Openlane has 2 modes of operation :-

    #Autonomous or interactive


# OpenLANE ASIC Flow

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215968264-df6f628b-14c9-41db-9539-0eb7d2cb63b5.PNG"></br>
   fig.11: 
</p>

OpenLane are based on several OpenSource Projects:-

OpenROAD, Magic VLSI Layout Tool, Fault,Yosys,Qflow, KLayout,etc.
