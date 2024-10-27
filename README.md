# VSD-Digital_VLSI_SoC_Planning
NASSCOM DIGITAL SOC PROGRAM-In this workshop, we will dive into the process of creating an Application Specific Integrated Circuit (ASIC), from the Register Transfer Level (RTL) to the Graphical Data System (GDS). 



> A two-week workshop on digital VLSI SoC design and planning, covering the entire RTL2GDSII flow, is being offered by VSD in association with NASSCOM.



# DAY 1 ( Inception of Opensource EDA , OpenLANE and SKY130 PDK )

### Theory

<details>
  <summary>
Expand or Collapse
  </summary>

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


   fig.7: ![macros ss1](https://github.com/user-attachments/assets/8457b72e-88d0-416d-9d3d-86ff1fc6eb0d)

</p>

# ISA (Instruction Set Architecture)

A C program must follow a precise flow when it is executed on a particular hardware layout, such as the inside of a chip in your laptop.
The assembly language program for this specific C application is first compiled using RISC-V ISA (Reduced Instruction Set Compting - V Intruction Set Architecture).
After that, the machine language program—which is the binary language of 0 and 1 that the computer hardware understands—is created from the assembly language program.

After that, we have to use an RTL (a Hardware Description Language) to implement this RISC-V specification. Lastly, there is a typical PnR or RTL to GDSII flow from the RTL to Layout.

</p>
<p align="center">

  ![ISA1](https://github.com/user-attachments/assets/f7b8cf73-c597-4912-8afa-9f1224cb1ff1)


   fig.7: 

</p>





1. The execution of application software on hardware involves several critical processes. Initially, the application enters a segment known as system software, which translates the application program into binary code. System software comprises multiple layers, with the primary components being the Operating System (OS), Compiler, and Assembler.

2. The OS first generates small functions in programming languages such as C, C++, Visual Basic, or Java. These functions are then processed by the corresponding compiler, which translates them into instructions. The syntax of these instructions is dependent on the hardware architecture of the system in use.

3. Subsequently, the assembler's role is to convert these instructions into their binary representation, commonly referred to as a machine language program. Ultimately, this binary code is supplied to the hardware, enabling it to comprehend and execute the specific functions dictated by the received binary instructions.

</p>
<p align="center">

  

![system software ss1](https://github.com/user-attachments/assets/a6055454-b7fe-4bfe-8b64-1f1c0579455a)

   fig.7: 

</p>

Let us take an example , Consider there is a stopwatch application running on a RISC-V core. The operating system's output may consist of a concise C function that is processed by the compiler, resulting in RISC-V instructions. Subsequently, the assembler generates binary code, which is then integrated into the chip layout.

The input and output of the compiler and assembler for the aforementioned stopwatch are as follows.

</p>
<p align="center">


![stopwatch ss](https://github.com/user-attachments/assets/aec8acce-5ba7-4851-814d-f9f8e40c7fa3)


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

OpenLane are based on several OpenSource Projects:


OpenROAD, Magic VLSI Layout Tool, Fault,Yosys,Qflow, KLayout,etc.

</details>


## Implementation

As, in my ubuntu setup , vsdflow and other tools are already installed so, i have put its screenshots ....
as, I have done some old trainings ....thats why its already installed on my ubuntu setup.


</p>
<p align="center">



</p>


<p align="center">


</p>


Checking all the respective tools inside Openlane 

![image](https://github.com/user-attachments/assets/9490c16d-f8c6-49e2-bffe-168d56888f79)

cd designs 
ls -ltr
![image](https://github.com/user-attachments/assets/e4d4cbec-af3e-4de1-850f-c61c2de95356)

cd picorv32a 

![image](https://github.com/user-attachments/assets/fb685f57-9474-4cc7-9f18-ab29863f7504)

ls-ltr
![image](https://github.com/user-attachments/assets/a9829a2b-fc67-4f6e-9d4e-5a42c2861ddc)


## Task 1 

(1) To Run 'picorv32a' design synthesis using OpenLANE flow and generate the respective outputs.

(2) To calculate the Flop Ratio 

- For Calculating the Flop Ratio ,with reference of number of D flip flops to number of cells , the following formula has been used 
```math
Flop\ Ratio = \frac{Number\ of\ D\ Flip\ Flops}{Total\ Number\ of\ Cells}
```
```math
Percentage\ of\ DFF's = Flop\ Ratio * 100
```

- How to open the Openlane Tool 

a) First of all, open the terminal and change the directory to openlane where , openlane exists 

```cd Desktop/work/tools/openlane_working_dir/openlane```

b) Invoke the OpenLANE flow docker sub-system by running below command

 `docker`

c) After accessing the OpenLANE flow contained docker sub-system, we are able to initiate the OpenLANE flow in the Interactive mode by using the command below:

`./flow.tcl -interactive`

d) When the openlane opens, now , we need to enter the required packages for the proper functionality of openlane flow 

`package require openlane 0.9`

e) Now, our openlane flow is ready with package 0.9 , In order to execute any design, we need to start by preparing the design, which involves creating essential files and directories to run a particular design, as in our case it is 'picorv32a.' design
This step is performed for setting up the files for preparing the respective design 


`prep -design picorv32a`

Note:- For cross checking and verifying that our design is prepared or not, finally, check that after completion of above command it will show "preapration completion " or Check the creation of file ,so a run folder is created within picorv32a

Since, today’s date is 24th September 2024 so a folder created is titled as “23-09_20-24” within the picorv32a Directory.

f) Now, our design is prepared and ready , we can proceed for running the synthesis now , by running the following command which is given below:-
as, all the LEF's have been merged in the design , so, we are proceeding for synthesis process now..

`run_synthesis`

this synthesis command will run for sometime , approximately 2-5 mins , we need to wait 
when it becomes successful check for the "Number of Cells", Number of D flip Flop " and "The chip area for the module - picorv32a "

g) To exit from openlane flow 

`exit`

h) To exit from openlane flow docker sub-system , run this command :-

`exit`





# Screenshots of running every command mentioned above 


![image](https://github.com/user-attachments/assets/57332469-ed7c-411e-8fd5-52b779db6a9c)

![image](https://github.com/user-attachments/assets/ad1aff13-6d94-47da-a9ec-5345d7452353)

![image](https://github.com/user-attachments/assets/edf3b703-4a5b-48af-aea0-0c7cee10b3c4)

Number of Cells :- 14876
![image](https://github.com/user-attachments/assets/60ba3a53-8a5d-4a01-bd1b-70fbd674724d)

Number of D Flip-Flop :- 1613
![image](https://github.com/user-attachments/assets/3d5f7799-5768-48ec-9f38-04d2e41b07ad)

The Chip Area for the Module - PICORV32a
![image](https://github.com/user-attachments/assets/f39535a6-8d19-46c0-8687-7aeecd82377b)

![image](https://github.com/user-attachments/assets/d2993dbb-09bf-40f8-b694-98d5a3607c47)

2) Calculation of Flop Ratio and Percentage of D Flip-Flop from synthesis statistics report 

To see synthesis report go to this directory work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/23-09_20-24/reports/synthesis/1-yosys_4.stat.rpt

![image](https://github.com/user-attachments/assets/ea40a957-2232-4f7a-b90e-92d555778575)


```math
Flop\ Ratio = \frac{1613}{14876} = 0.108429685
```
```math
Percentage\ of\ DFF's = 0.108429685 * 100 = 10.84296854\ \%
```

## File View of Synthesis Result 

![image](https://github.com/user-attachments/assets/46c06fe7-cbe5-4ee4-85c7-2ab2698bcb6c)



### Note

<details>
  <summary>
Expand or Collapse
  </summary>

### *Note:- For confirming that our design is prepped and ready or not after performing steps (e)* 

![image](https://github.com/user-attachments/assets/cc1fc29a-feb6-4e1d-ab03-c7500c4e8570)

also, check that a run folder has been created inside picorv32a folder 

![image](https://github.com/user-attachments/assets/8090fc3d-f2c4-4361-a056-951f398a1ac3)

this folder is created inside picorv32a/runs with todays date i.e., 24th September 2024 so ,a folder created is titled as “23-09_20-24” 

![image](https://github.com/user-attachments/assets/ba085089-cd66-4b37-ad9e-127c317c1dc0)



</details>
 

# DAY 2 ( Good Floorplan vs Bad Floorplan and Introduction to Library Cells )


### Theory

<details>
  <summary>
Expand or Collapse
  </summary>

Consideration of chip Floorplan

![image](https://github.com/user-attachments/assets/c7491ddc-88a8-4769-8e96-a548cca0c86a)

The height and width of the core and die areas must first be determined in order to calculate the Utilisation Factor and Aspect Ratio.

#### Core
Core of the chip
Core is basically consist of different logics . A core is that place where all the digital logics are made or placed in this area like And ,or logic,etc.

#### Die
Die is basically the area of the chip 
It is called as that die which is manufactured at the silicon wafer .

The design's netlist will determine the core area's height and width. The number of components needed to carry out the logic will determine it, and the die area's height and width will depend on the height and width of the core area.


![image](https://github.com/user-attachments/assets/82fecd85-a554-4c85-a7bd-04242fd45029)


2 parameters are important mainly in floorplanning .These are:-

Utilization Factor and Aspect Ratio.

               • Utilisation Factor =  Area occupied by netlist
   
                                      __________________________
                      
                                          Total area of core

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215687478-3fa3bf8c-2905-4d2f-b5f9-efa36007d737.png"></br>
   fig.52
</p>

A utilization Factor of 1 signifies 100% utilization leaving no space for extra cells/logics such as to add buffer. However, practically , we only use utilization factor approximately 50%-60% or 0.5-0.6.

   • Aspect Ratio
   • Aspect ratio = Height/Width 

* Height of the core , 
* width of the core ,

Aspect ratio 1 means that the chip is squared shaped. Any value which is another than 1 means it implies the rectangular shaped. It also means that when anything comes other than  1 then, the core is 50% utilized and the remaining area or extra amount of area is used to place the additional cells.

--> Core utilization =area of netlist/total area of cell

Here, FP_CORE_UTIL=50 means floorplan core utilization is 50%.

Aspect ratio is 1.


Note:- ## The Utilisation Factor should never be "1" for a good floor plan since at that point, there won't be any room for further reasoning to be added if necessary, and the floor plan will be considered poor.



</details>


## Task 2

Section 2 tasks:- 
1. Run 'picorv32a' design floorplan using OpenLANE flow and generate necessary outputs.
2. Calculate the die area in microns from the values which are given in floorplan def file.
3. Load generated floorplan def in magic tool and explore the floorplan.
4. Run 'picorv32a' design congestion aware placement using OpenLANE flow and generate necessary outputs.
5. Load generated placement def in magic tool and explore the placement.

```math
Area\ of\ die\ in\ microns = Die\ width\ in\ microns * Die\ height\ in\ microns
```
  

1. To run the Floorplan of "picorv32a" design using Openlane

`run_floorplan`






















# Screenshots of running every command mentioned above 


#### Note :-
<details>
  <summary>
Expand or Collapse
  </summary>

Before running the floorplan change the `VMetal` and `HMetal` Layers as in openlane "Layer number are 1 less than the actual layer "


![image](https://github.com/user-attachments/assets/fd467835-07b4-46a5-bb67-403845b3a091)

In the above image , Left:- config.tcl, inside picorv32a has been modified 
                     Right:- Floorplan.tcl in openlane configuration 

</details>



![image](https://github.com/user-attachments/assets/ad11d158-bd3a-4972-bf67-43b9ed7363b9)

![image](https://github.com/user-attachments/assets/fffb43be-2e06-4deb-be41-300ee6498a0f)

<details>
  <summary>
Expand or Collapse
  </summary>


Now, to check which library are used in synthesis, what is maximum fanout, what files are there in floorplan etc.
Just go to this directory :- `cd Desktop/work/tools/openlane_working_dir/openlane/configurations` and run the given command as shown in image below:-  
![image](https://github.com/user-attachments/assets/e346acad-6dc8-4fbe-8e6d-d0bbd66e395f)


This s given for Synthesis , 
![image](https://github.com/user-attachments/assets/6c29dde0-22b8-4032-8d74-a0b2178ac242)

For Floorplan , what all files are there inside it ,for example:- core util, aspect ratio, etc.  it is listed below:- 

![image](https://github.com/user-attachments/assets/59ccc78f-a754-4900-8fe6-1e1f57cbeb9e)

then, for placement, 
![image](https://github.com/user-attachments/assets/edba9518-2234-435a-9727-da1455138a8c)

Then, for CTS , Routing, etc. everything is given in this readme.md

![image](https://github.com/user-attachments/assets/125f2cdf-586c-461b-9123-848b9a016285)

</details>

 ### 2. To calculate the Die area in microns from the values which are given in floorplan.def file

Conetnt of floorplan.def is given below :-

`cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/23-09_20-24/results/floorplan/picorv32a.floorplan.def `

![image](https://github.com/user-attachments/assets/58e0b01d-408d-44f6-b7a8-bca1a51276c2)

According to floorplan def
```math
1\ Micron = 1000\ Unit\ Distance
```
```math
Die\ width\ in\ unit\ distance = 660685 - 0 = 660685
```
```math
Die\ height\ in\ unit\ distance = 671405 - 0 = 671405
```
```math
Distance\ in\ microns = \frac{Value\ in\ Unit\ Distance}{1000}
```
```math
Die\ width\ in\ microns = \frac{660685}{1000} = 660.685\ Microns
```
```math
Die\ height\ in\ microns = \frac{671405}{1000} = 671.405\ Microns
```
```math
Area\ of\ die\ in\ microns = 660.685 * 671.405 = 443587.212425\ Square\ Microns
```



### 3. Load generated floorplan def in magic tool and explore the floorplan.

Commands to load floorplan def in magic in another terminal

```bash
# Change directory to path containing generated floorplan def
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/17-03_12-06/results/floorplan/

# Command to load the floorplan def in magic tool
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```

Screenshots of floorplan def in magic

![image](https://github.com/user-attachments/assets/a9f79e54-ee6a-43ef-bc35-cffcc029d1aa)

This is the Floorplan Layout in Magic which is shown above as well as below 

![image](https://github.com/user-attachments/assets/f47233bb-822e-4dd4-93fc-15e49b0821e9)

--> Equidistant Placement of Ports

![image](https://github.com/user-attachments/assets/bfb0ba6f-85fc-4ee0-89e7-1686227937d9)

![image](https://github.com/user-attachments/assets/8754e263-2127-4fd6-8cff-041b85540925)


--> Select any cell and then in tkcon window , enter the command "what" to display the respective cell details  

![image](https://github.com/user-attachments/assets/9e13d9a3-5446-4343-9d09-90c4d651d6ed)

--> Port Layer as set through config.tcl 

![image](https://github.com/user-attachments/assets/810a2add-d8b3-41b6-a102-a9e849d42862)


![image](https://github.com/user-attachments/assets/ea04ddcc-37d3-45e8-bad6-ea96494816f1)


--> Decap cells and Tap Cells 

![image](https://github.com/user-attachments/assets/bd8eefe1-8b58-4c9a-8b3d-1fdcaa30002c)

--> Diagonally Equidistant Tap Cells

![image](https://github.com/user-attachments/assets/14753a7a-3131-46b8-b8c0-33540636025c)


#### 4. Run 'picorv32a' design congestion aware placement using OpenLANE flow and generate necessary outputs.

Command to run placement

```tcl
# Congestion aware placement by default
run_placement
```

Screenshots of placement run

![image](https://github.com/user-attachments/assets/b04cbd48-80ce-4de1-87a6-fb019b29fd7b)


![image](https://github.com/user-attachments/assets/d37992d0-5cbf-42ed-be7d-96fcfa3bafa6)

#### 5. Load generated placement def in magic tool and explore the placement.


Commands to load placement def in magic in another terminal

```bash
# Change directory to path containing generated placement def
cd /Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/23-09_20-24/results/placement/

# Command to load the placement def in magic tool
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```

Screenshots of placement def in magic

![image](https://github.com/user-attachments/assets/5db5cf82-b184-499e-a438-43ae35978229)


![image](https://github.com/user-attachments/assets/2443a890-78a1-4bdc-a1b6-ade063c1e872)

--> All Standard Cells are legally Placed 

![image](https://github.com/user-attachments/assets/6c91e1af-423c-4196-934d-30dfdaa75bfe)


Commands to exit from current run

```tcl
# Exit from OpenLANE flow
exit

# Exit from OpenLANE flow docker sub-system
exit
```

# DAY 3 ( Design library cell using Magic Layout and ngspice characterization )
Inverrter Characterization using SKY130 Model File


### Theory

<details>
  <summary>
Expand or Collapse
  </summary>


## Timing characterization

Different threshold points of waveform itself .
Timing threshold points
So, we use this waveform to define different threshold and to understand the other characteristics .


1) Slew_low_rise_thr - low depicts the power which is close to 0 power supply 
To calculate the slope or slew of this red particular waveform so, we need 2 points for it and defines those 2 points .
Typical value of slew_low_rise_thr is 20%.
It could be 30% also.

This is for rising waveform ,similarly it applies for falling waveform .


We need these values for calculating the slews of the waveform i.e., slew low rise threshold, slew high rise threshold,slew
 low fall threshold,slew high fall thr.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215775529-19399c30-c678-46b3-af79-ded54bbbe9a8.png"></br>
   fig.77
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215782582-5f58cb82-9115-44ed-991e-e7f34f307323.png"></br>
   fig.79
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215782792-bffef679-8602-4620-835b-6578b454d734.png"></br>
   fig.80
</p>



In_rise_thr is input waveform 
For example ,this is input stimulus We have given input to the stimulus and taking the output from the buffer.

In_rise_thr 
We also have threshold for delay as well.We need some point to calculate the delay .
In this case we take 50% red waveform that is slew waveform .And one point on output waveform to calculate the delay.

ypical value of inrise threshold is 50%. It's basically input rising waveform.


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215783257-8a7ffa60-ac2c-4af0-bf2e-e2d05c2f2a9a.png"></br>
   fig.81
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215783520-237aa288-048c-4dfc-9276-b54585990431.png"></br>
   fig.82
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215784192-2067973c-cbe4-423a-92ad-46926cccdfc8.png"></br>
   fig.83
</p>


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/215784454-22ce08ad-6008-46f3-8381-e2d9ffd6b620.png"></br>
   fig.84
</p>




</details>

## Task 3
Section 3 Tasks :- 
1. Clone custom inverter standard cell design from github repository: [Standard cell design and characterization using OpenLANE flow](https://github.com/nickson-jose/vsdstdcelldesign).
2. Load the custom inverter layout in magic and explore.
3. Spice extraction of inverter in magic.
4. Editing the spice model file for analysis through simulation.
5. Post-layout ngspice simulations.
6. Find problem in the DRC section of the old magic tech file for the skywater process and fix them.




#### 1. Clone custom inverter standard cell design from github repository

```bash
# Change directory to openlane
cd Desktop/work/tools/openlane_working_dir/openlane

# Clone the repository with custom inverter design
git clone https://github.com/nickson-jose/vsdstdcelldesign

# Change into repository directory
cd vsdstdcelldesign

# Copy magic tech file to the repo directory for easy access
cp /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech .

# Check contents whether everything is present
ls

# Command to open custom inverter layout in magic
magic -T sky130A.tech sky130_inv.mag &
```

Screenshot of commands run


![image](https://github.com/user-attachments/assets/1019f605-ba8f-49d2-84b1-f1d03fe469e8)


#### 2. Load the custom inverter layout in magic and explore.

--> Screenshot of custom inverter layout in magic

![image](https://github.com/user-attachments/assets/b2ad6761-065e-4cc9-833c-b1e0d7df5ec2)

--> PMOS and NMOS are identified in this inverter layout 

![image](https://github.com/user-attachments/assets/c6960a32-17b6-4ff4-a3e9-fdc4ea83aa72)

![image](https://github.com/user-attachments/assets/e3002c08-32e2-437b-9ee2-f9119cd0b409)

--> Input A connected with PMOS and NMOS 

![image](https://github.com/user-attachments/assets/7f7c864e-7f77-4820-857d-ee47a1649f06)

--> Connectivity of Output Y with PMOS and NMOS drain is verified

![image](https://github.com/user-attachments/assets/e0e7b76f-6a01-4d03-9e73-8b724b36ca2b)

--> Source Connectivity of PMOS with VDD (here, it is VPWR) verified 

![image](https://github.com/user-attachments/assets/15cb62ff-a120-4e81-9269-8275518a3af2)

--> Source Connectivity of NMOS with VSS (here, it is VGND) verified 

![image](https://github.com/user-attachments/assets/d20f7509-7c80-4166-a573-74834f309055)


To see DRC errors

![image](https://github.com/user-attachments/assets/153cd67b-6ba2-4532-812d-421c9f5be623)


#### 3. Spice extraction of inverter in magic.

Commands for spice extraction of the custom inverter layout to be used in tkcon window of magic

```tcl
# Check current directory
pwd

# Extraction command to extract to .ext format
extract all

# Before converting ext to spice this command enable the parasitic extraction also
ext2spice cthresh 0 rthresh 0

# Converting to ext to spice
ext2spice
```

Screenshot of tkcon window after running above commands

--> To extract the parasitics and characterize the cell design use below commands in tkcon window.
pwd
extract all
ext2spice cthresh 0 rthresh 0
ext2spice


![image](https://github.com/user-attachments/assets/30f36941-fdc8-4add-8544-b100e9f2f2e0)

--> The SPICE FILE which is created screenshot of that is given below:- 

It will find inside the given path ,

`Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign`

![image](https://github.com/user-attachments/assets/8f926fdf-12fd-4c34-8303-5499ac4f370d)

#### 4. Editing the spice model file for analysis through simulation.

Measuring unit distance in layout grid

![image](https://github.com/user-attachments/assets/39e1693b-16ed-4a23-9c49-0d713b2872a2)

Now, edit the Spice File of Sky130 Inverter for ngspice simulation 

![image](https://github.com/user-attachments/assets/b0515a2a-efc3-41a4-b238-3441e708c8bf)

![image](https://github.com/user-attachments/assets/ca3aa6b0-c39c-4490-9843-0d0ce1402d63)


#### 5. Post-layout ngspice simulations.

Commands for ngspice simulation

```bash
# Command to directly load spice file for simulation to ngspice
ngspice sky130_inv.spice

# Now that we have entered ngspice with the simulation spice file loaded we just have to load the plot
plot y vs time a
```

Screenshots of ngspice run

![image](https://github.com/user-attachments/assets/ee090c10-1740-4c76-b0fd-8ae4f06dd8df)

![image](https://github.com/user-attachments/assets/25f56584-e069-4ba9-b5dc-55a5f2c36402)



screenshot of generated plot

![image](https://github.com/user-attachments/assets/c480f76f-2cb4-4ab0-845a-5d594cd725bf)



Time Calculation for rise transition 

```math
Rise\ transition\ time = Time\ taken\ for\ output\ to\ rise\ to\ 80\% - Time\ taken\ for\ output\ to\ rise\ to\ 20\%
```



```math
20\%\ of\ output = 660\ mV
```

80 % screenshot
```math
80\%\ of\ output = 2.64\ V
```

20 % screenshot

![image](https://github.com/user-attachments/assets/70274102-a2f0-4654-a0ee-f6c2eb10762d)

![image](https://github.com/user-attachments/assets/d7c8efbb-1641-42a0-8185-d7bef481a050)

80 % screenshot 

![image](https://github.com/user-attachments/assets/65fab3d5-4d7d-4993-b273-c21026775189)


![image](https://github.com/user-attachments/assets/b47a98d6-70ea-4e2a-9a2e-ed50ab29a0b7)

```math
Rise\ transition\ time = 2.24673 - 2.18242 = 0.06431\ ns = 64.31\ ps
```

Fall transition time calculation

```math
Fall\ transition\ time = Time\ taken\ for\ output\ to\ fall\ to\ 20\% - Time\ taken\ for\ output\ to\ fall\ to\ 80\%
```
```math
20\%\ of\ output = 660\ mV
```
```math
80\%\ of\ output = 2.64\ V
```

20% Screenshots

![image](https://github.com/user-attachments/assets/b4af75d8-c7af-4c95-b1b3-9ccc85944455)

![image](https://github.com/user-attachments/assets/75f28bbb-b103-4633-8553-5c14c25943b8)

80% screenshot 

![image](https://github.com/user-attachments/assets/ac9805e1-4f54-44e7-9881-64d498106b9f)


![image](https://github.com/user-attachments/assets/9acba647-7dfb-4076-abe8-297a57b478c6)


```math
Fall\ transition\ time = 4.09549 - 4.05313 = 0.04236\ ns = 42.3\ ps
```

Rise Cell Delay Calculation

```math
Rise\ Cell\ Delay = Time\ taken\ for\ output\ to\ rise\ to\ 50\% - Time\ taken\ for\ input\ to\ fall\ to\ 50\%
```
```math
50\%\ of\ 3.3\ V = 1.65\ V
```

50% Screenshots

![image](https://github.com/user-attachments/assets/f4f4b402-cef5-4376-896d-07e416bf82ca)

![image](https://github.com/user-attachments/assets/8b0faa90-7e60-47e0-aa1e-9c98aafd7cfb)


```math
Rise\ Cell\ Delay = 2.21119 - 2.15048 = 0.06071\ ns = 60.71\ ps
```



Fall Cell Delay Calculation

```math
Fall\ Cell\ Delay = Time\ taken\ for\ output\ to\ fall\ to\ 50\% - Time\ taken\ for\ input\ to\ rise\ to\ 50\%
```
```math
50\%\ of\ 3.3\ V = 1.65\ V
```

50% Screenshots

![image](https://github.com/user-attachments/assets/63fb1a0a-54a0-4545-9b98-822a54368245)

![image](https://github.com/user-attachments/assets/7114dcaa-3ebc-4487-a463-dd2444f3fd83)


```math
Fall\ Cell\ Delay = 4.07 - 4.05 = 0.02\ ns = 20\ ps
```


#### 6. Find problem in the DRC section of the old magic tech file for the skywater process and fix them.

Link to Sky130 Periphery rules: [https://skywater-pdk.readthedocs.io/en/main/rules/periphery.html](https://skywater-pdk.readthedocs.io/en/main/rules/periphery.html)

Commands to download and view the corrupted skywater process magic tech file and associated files to perform drc corrections

```bash
# Change to home directory
cd

# Command to download the lab files
wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz

# Since lab file is compressed command to extract it
tar xfz drc_tests.tgz

# Change directory into the lab folder
cd drc_tests

# List all files and directories present in the current directory
ls -al

# Command to view .magicrc file
gvim .magicrc

# Command to open magic tool in better graphics
magic -d XR &
```

Screenshots of commands run
![ss1](https://github.com/user-attachments/assets/998c4e32-4e8b-420d-9b55-02113eec273a)
![ss2](https://github.com/user-attachments/assets/f0cef70a-2397-4ba6-a6a0-26fd4dc0fea7)


Screenshot of .magicrc file

![image](https://github.com/user-attachments/assets/eccff6d1-88bc-436f-b954-423200717c56)

After opening magic , go to file menu > Open > met3.mag > open 

![image](https://github.com/user-attachments/assets/aabe2228-ff77-422c-bb4f-acea87a41fd4)


![image](https://github.com/user-attachments/assets/d103760f-a8ef-46dd-9c02-9a8948465dfb)

![image](https://github.com/user-attachments/assets/fa79aa2a-a62c-45bc-ad89-5af6a014275d)

![image](https://github.com/user-attachments/assets/8547e5fd-7455-408f-a3ca-91044ab7b811)
![image](https://github.com/user-attachments/assets/4d5551fc-ae86-4469-97f7-ff568d138e2f)

![image](https://github.com/user-attachments/assets/b6f3f7a4-3c39-44e5-aa29-ed67a7986950)

![image](https://github.com/user-attachments/assets/cc3285be-0e1f-4737-8bd6-8557ae789805)

![image](https://github.com/user-attachments/assets/09eed0cc-e167-450d-84a5-605f0f92bb23)





 

**Incorrectly implemented poly.9 simple rule correction**

Screenshot of poly rules

![image](https://github.com/user-attachments/assets/6b71711d-2d85-47b4-b118-38a3f03adb49)


Incorrectly implemented poly.9 rule no drc violation even though spacing < 0.48u

in magic, type these command to load poly
![image](https://github.com/user-attachments/assets/5d978565-8cf1-4112-8d93-6fe4aa2c993c)

![image](https://github.com/user-attachments/assets/77b45ea5-20d0-4288-9900-ba78991488ed)

![image](https://github.com/user-attachments/assets/57c1d911-1f59-40e4-93aa-9306525e0dcf)

![image](https://github.com/user-attachments/assets/cffa5589-7881-498b-b7b1-0bc61cb0e43f)

![image](https://github.com/user-attachments/assets/12ac0b63-9ff2-4deb-87e3-301e9cf9d159)

![poly](https://github.com/user-attachments/assets/d8033535-4001-450e-92be-336082c19024)


![poly 9 magic ](https://github.com/user-attachments/assets/0f3230a4-5769-4c77-b789-ef497491d3f9)



New commands inserted in sky130A.tech file to update drc


![poly edit](https://github.com/user-attachments/assets/126758e8-4153-4723-9ec4-c9b1154ff785)

![uhr edit ](https://github.com/user-attachments/assets/e99d1cdf-cf31-44d8-acf9-15544b95f0f7)



Commands to run in tkcon window

```tcl
# Loading updated tech file
tech load sky130A.tech

# Must re-run drc check to see updated drc errors
drc check

# Selecting region displaying the new errors and getting the error messages 
drc why
```

Screenshot of magic window with rule implemented

![screenshot of magic window with rule implemented ss1](https://github.com/user-attachments/assets/6b93bcd6-030e-42db-aab9-0d36ee38397c)

![image](https://github.com/user-attachments/assets/e9abfabf-f099-4582-adfe-ef6a37bcb21f)


**Incorrectly implemented difftap.2 simple rule correction**

Screenshot of difftap rules

![image](https://github.com/user-attachments/assets/648db469-deba-4367-ae5e-082797fceb1b)

Incorrectly implemented difftap.2 rule no drc violation even though spacing < 0.42u

![image](https://github.com/user-attachments/assets/db4ffa40-4210-48b5-b0cd-849f6d811c3d)

![image](https://github.com/user-attachments/assets/cbd47b52-a36a-41e9-ba69-425df0805d85)



New commands inserted in sky130A.tech file to update drc

![mos varactor edit](https://github.com/user-attachments/assets/56c26036-7047-4d40-bc75-68205ddc3e05)



Commands to run in tkcon window

```tcl
# Loading updated tech file
tech load sky130A.tech

# Must re-run drc check to see updated drc errors
drc check

# Selecting region displaying the new errors and getting the error messages 
drc why
```

Screenshot of magic window with rule implemented

![image](https://github.com/user-attachments/assets/404af339-0046-42a1-abca-1ceb5b1c5b9f)

**Incorrectly implemented nwell.4 complex rule correction**

Screenshot of nwell rules

![image](https://github.com/user-attachments/assets/192dc854-4a19-44df-8db7-910e0740c985)

Incorrectly implemented nwell.4 rule no drc violation even though no tap present in nwell

![image](https://github.com/user-attachments/assets/4040b388-adcb-4604-9416-bf081e156f71)

![image](https://github.com/user-attachments/assets/6d81b47c-f0e3-4f79-a16e-b3addca3c0f0)



New commands inserted in sky130A.tech file to update drc
![templayer_edit](https://github.com/user-attachments/assets/b2a5780b-c197-4f3a-a6cf-64c388d412f6)


![nwell_edit](https://github.com/user-attachments/assets/75e6e5e9-78a6-40c5-b9f5-49cfbe1b737a)



Commands to run in tkcon window

```tcl
# Loading updated tech file
tech load sky130A.tech

# Change drc style to drc full
drc style drc(full)

# Must re-run drc check to see updated drc errors
drc check

# Selecting region displaying the new errors and getting the error messages 
drc why
```

Screenshot of magic window with rule implemented

![image](https://github.com/user-attachments/assets/3806de73-f419-4aec-b06a-97d1603c99b1)




# DAY 4 ( Pre- Layout Timing Analysis and importance of good clock Tree )


### Theory

<details>
  <summary>
Expand or Collapse
  </summary>

</details>


## Task 4

1. To Fix up small DRC errors and to verify the design is ready to be inserted into our flow.
2. Save the finalized layout with custom name and open it.
3. Generate lef from the layout.
4. Copy the newly generated lef and associated required lib files to 'picorv32a' design 'src' directory.
5. Edit 'config.tcl' to change lib file and add the new extra lef into the openlane flow.
6. Run openlane flow synthesis with newly inserted custom inverter cell.
7. Remove/reduce the newly introduced violations with the introduction of custom inverter cell by modifying design parameters.
8. Once synthesis has accepted our custom inverter we can now run floorplan and placement and verify the cell is accepted in PnR flow.
9. Do Post-Synthesis timing analysis with OpenSTA tool.
10. Replace the old netlist with the new netlist generated after timing ECO fix and implement the floorplan, placement and cts.





#### 1. To Fix up small DRC errors and to verify the design is ready to be inserted into our flow.


There are some Conditions which need to be verified before proceeding further using the custom design cell layout:

    First condition: The standard cell's input and output ports should be located where       the vertical and horizontal tracks meet.
    Second requirement: The standard cell's width must be an odd multiple of the              horizontal track pitch.
    Third requirement: The standard cell's height need to be an even multiple of the          vertical track pitch.

Commands to run for opening the custom inverter layout are given below :- 

```bash
# Change directory to vsdstdcelldesign
cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign

# Command to open custom inverter layout in magic
magic -T sky130A.tech sky130_inv.mag &
```
The inverter layout after opening in magic looks like this :- 

![image](https://github.com/user-attachments/assets/477ad5e8-85df-4f66-bb7d-665a3935f7d0)

![image](https://github.com/user-attachments/assets/12aa7490-798a-4217-90a5-16bac11a7f6a)



Screenshot of tracks.info of sky130_fd_sc_hd

Tracks are basically nothing it is just the thing which is used during the routing stage .
It shows the traces. 
x is horizontal track and Y is vertical track .

![image](https://github.com/user-attachments/assets/e290b95f-64a3-427b-bbf7-5897a021bc34)

![image](https://github.com/user-attachments/assets/4cf09d35-9883-4434-ba2d-2fe926a4b109)

Commands to run in tkcon window of magic to set grid as tracks of locali layer

```tcl
# Get syntax for grid command
help grid

# Set grid values accordingly
grid 0.46um 0.34um 0.23um 0.17um
```

Screenshot of commands run

![image](https://github.com/user-attachments/assets/5659a625-ef3f-40e1-b6eb-1a482724063d)

--> First Condition Verified 

![image](https://github.com/user-attachments/assets/14e13564-a097-43c5-a1a2-18f22fb4addb)

--> Second Condition Verified 

      As, Horizontal Track Pitch is given as = 0.46um

![image](https://github.com/user-attachments/assets/baf9f2b5-871a-4740-93f0-5b53f256c2b2)

               Width of standard cell= 1.38um = 0.46 * 3

--> Third Condition Verified 

      As, Vertical Track Pitch is given as = 0.34um

![image](https://github.com/user-attachments/assets/fe1cb4ab-7696-4baf-a099-447a63f1743d)


![image](https://github.com/user-attachments/assets/ba4b8d96-24c0-4320-8d44-1e80e9f1807e)




              Height of standard cell= 2.72 um = 0.34 * 8


#### 2. Save the finalized layout with custom name and open it.

Command to run in tkcon window to save the layout with custom name

```tcl
# Command to save as
save sky130_vsdinv.mag
exit
```

Image of Saved Layout
![image](https://github.com/user-attachments/assets/d72517f4-d46e-4dd1-b9e8-024dd6e7f2d2)

we can see in the directory that our file becomes saved , as it is listed now in the respective directory 

![image](https://github.com/user-attachments/assets/0e8a0a9c-808e-4c91-a6ce-729cd6745480)



 
Command to open the newly saved layout

```bash
# Command to open saved custom inverter layout in magic
magic -T sky130A.tech sky130_vsdinv.mag &
```

Screenshot of newly saved layout

![image](https://github.com/user-attachments/assets/af6ca108-fece-4fb2-9661-ac0c9964cafd)





#### 3. To Generate lef from the layout.

Command for tkcon window to write lef

```tcl
# lef command
lef write
```
--> when you extract the LEF files, so at that time these ports are basically defined as pins which are used in mag.  

Screenshot of command run
![image](https://github.com/user-attachments/assets/49fc3b36-d5f3-499b-89eb-57b0f1fad971)

Lef file has been created in the same directory with same name as shown below:-

![image](https://github.com/user-attachments/assets/b86de9ee-392f-4b6b-bc6b-0bb906ca138f)

Screenshot of newly created lef file

![image](https://github.com/user-attachments/assets/4f0537ca-6137-4e82-9c2a-6be093723802)

#### 4. Copy the newly generated lef and associated required lib files to 'picorv32a' design 'src' directory.

Commands to copy necessary files to 'picorv32a' design 'src' directory

```bash
# Copy lef file

cp sky130_vsdinv.lef /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/

# List and check whether it's copied
ls ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/

# Copy lib files
cp sky130_fd_sc_hd_* /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/

# List and check whether it's copied
ls ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/
```

Screenshot of commands run

![image](https://github.com/user-attachments/assets/8fd1cf1e-2b3a-49cc-a569-3bb2a7ac1ee2)

check 

![image](https://github.com/user-attachments/assets/5745d680-2282-4d3f-b13a-53fb07129f6e)

copy lib file 
![image](https://github.com/user-attachments/assets/79171bdd-c029-4cc9-a6bd-d49b77b9ce66)

check 
![image](https://github.com/user-attachments/assets/58ab563c-ead1-4c90-87b8-a11bea0fc0bc)


#### 5. Edit 'config.tcl' to change lib file and add the new extra lef into the openlane flow.

Commands to be added to config.tcl to include our custom cell in the openlane flow

```tcl
set ::env(LIB_SYNTH) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"
set ::env(LIB_FASTEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__fast.lib"
set ::env(LIB_SLOWEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__slow.lib"
set ::env(LIB_TYPICAL) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"

set ::env(EXTRA_LEFS) [glob $::env(OPENLANE_ROOT)/designs/$::env(DESIGN_NAME)/src/*.lef]
```

Edited config.tcl to include the added lef and change library to ones we added in src directory


![image](https://github.com/user-attachments/assets/91f666e2-05f7-4ae7-92f6-10fdcea68028)


#### 6. Run openlane flow synthesis with newly inserted custom inverter cell.

Commands to invoke the OpenLANE flow include new lef and perform synthesis 

```bash
# Change directory to openlane flow directory
cd Desktop/work/tools/openlane_working_dir/openlane

# alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
# Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command
docker
```
```tcl
# Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command
./flow.tcl -interactive

# Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flow
package require openlane 0.9

# Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'
prep -design picorv32a

# Adiitional commands to include newly added lef to openlane flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis
```

Screenshots of commands run

![image](https://github.com/user-attachments/assets/ce66597f-0d8f-4b39-9ed5-ae50889d61a5)

![image](https://github.com/user-attachments/assets/5091d9c6-807d-4e56-9970-a82b86e0b915)


![image](https://github.com/user-attachments/assets/1b50e811-045d-45f2-9e99-7d6ba64110f2)

#### 7. Remove/reduce the newly introduced violations with the introduction of custom inverter cell by modifying design parameters.

Noting down current design values generated before modifying parameters to improve timing
![image](https://github.com/user-attachments/assets/efef72c3-a276-4304-8840-7cccdea1a14a)

![image](https://github.com/user-attachments/assets/20a01558-674a-4f48-88dd-08a445d3f0f6)

![image](https://github.com/user-attachments/assets/60cae338-a19a-43b1-a847-5240fbf0bacf)




Commands to view and change parameters to improve timing and run synthesis

```tcl
# Now once again we have to prep design so as to update variables
prep -design picorv32a -tag 03-10_21-51 -overwrite 

# Addiitional commands to include newly added lef to openlane flow merged.lef
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to display current value of variable SYNTH_STRATEGY
echo $::env(SYNTH_STRATEGY)

# Command to set new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"

# Command to display current value of variable SYNTH_BUFFERING to check whether it's enabled
echo $::env(SYNTH_BUFFERING)

# Command to display current value of variable SYNTH_SIZING
echo $::env(SYNTH_SIZING)

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Command to display current value of variable SYNTH_DRIVING_CELL to check whether it's the proper cell or not
echo $::env(SYNTH_DRIVING_CELL)

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis
```

After running the above mentioned command , 

![image](https://github.com/user-attachments/assets/7250f997-e4cd-46c4-8287-6800baf4fd2e)

![image](https://github.com/user-attachments/assets/ab4943c8-e6f5-4ba9-a345-79244a435e84)
![image](https://github.com/user-attachments/assets/6111b046-ee36-4926-8103-ddde7aec1367)

![image](https://github.com/user-attachments/assets/d08178ad-9c41-44d0-8091-ed4f700681f3)

![image](https://github.com/user-attachments/assets/bd54f146-fba0-4705-abb9-329bbe41fb6c)

![image](https://github.com/user-attachments/assets/5c39e576-89f5-4336-a95d-aefd8fd4c7c0)



Comparing to previously noted run values area has increased and worst negative slack has become 0

![image](https://github.com/user-attachments/assets/1187c6b5-e03e-4345-9e1d-29959da0a658)


![image](https://github.com/user-attachments/assets/b364a93a-8514-4be7-b6ca-d37f46a733c1)

--> Screenshot of merged.lef in `tmp` directory with our custom inverter as macro


"/home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-10_21-51/tmp/merged.lef"

![image](https://github.com/user-attachments/assets/86499007-6953-44d3-a3c4-03e88f620c89)

#### 8. Once synthesis has accepted our custom inverter we can now run floorplan and placement and verify the cell is accepted in PnR flow.

Now that our custom inverter is properly accepted in synthesis we can now run floorplan using following command

```tcl
# Now we can run floorplan
run_floorplan
```

Screenshots of command run

![image](https://github.com/user-attachments/assets/c10f1e8b-1724-465b-b302-72a080504465)

![image](https://github.com/user-attachments/assets/4c1cab45-b287-4701-9b26-d8302f81ae4b)

Since we are encountering an unexpected, inexplicable error while using the `run_floorplan} command.
We can utilize the `Floorplan Commands} section in `Desktop/work/tools/openlane_working_dir/openlane/docs/source/OpenLANE_commands.md} as well as information from `Desktop/work/tools/openlane_working_dir/openlane/scripts/tcl_commands/floorplan.tcl} to replace the `run_floorplan} command.

```tcl
# Follwing commands are alltogather sourced in "run_floorplan" command
init_floorplan
place_io
tap_decap_or
```

Screenshots of commands run

![image](https://github.com/user-attachments/assets/1ecd561a-35ed-4428-a030-6b0b54a90be3)



![image](https://github.com/user-attachments/assets/c9647712-71b6-4f34-8eb9-9f1a732d2555)


![image](https://github.com/user-attachments/assets/f9eca06f-65ca-4b8b-8be8-8da2a7ff9bda)


Now that floorplan step is completed so, we can do placement using following command given below:- 

```tcl
# Now we are ready to run placement
run_placement
```

Screenshots of command run

![image](https://github.com/user-attachments/assets/958df37d-5e4f-4cb0-bc3b-ed18e26fb991)

![image](https://github.com/user-attachments/assets/c4a7ced5-4e06-4f03-8b46-09dc90829d84)

Commands to load placement def in magic in another terminal

```bash
# Change directory to path containing generated placement def
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-10_21-51/results/placement/

# Command to load the placement def in magic tool
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &
```

Screenshot of placement def in magic

![image](https://github.com/user-attachments/assets/9cf5e52b-09f9-40a9-a20b-2820780416da)

![image](https://github.com/user-attachments/assets/ab898169-3aaa-4c40-a61b-e25b4289fe85)

Screenshot of custom inverter inserted in placement def with proper abutment

![image](https://github.com/user-attachments/assets/40ed3f93-7b50-4e82-abae-7ab58ff904c1)


Command to run in tkcon window to view internal layers of cells

```tcl
# Command to view internal connectivity layers
expand
```

Abutment of power pins with other cell from library clearly visible

![image](https://github.com/user-attachments/assets/c9e560cd-7cfa-4c64-b654-172fd6aea41b)

![image](https://github.com/user-attachments/assets/ef3422d8-57e5-4a93-9a72-bf93ab35bf84)
![image](https://github.com/user-attachments/assets/a01fbe63-1dd3-4603-b1ec-6b79104f42fb)


#### 9. Do Post-Synthesis timing analysis with OpenSTA tool.

Since we are having 0 wns after improved timing run we are going to do timing analysis on initial run of synthesis which has lots of violations and no parameters were added to improve timing

Commands to invoke the OpenLANE flow include new lef and perform synthesis 

```bash
# Change directory to openlane flow directory
cd Desktop/work/tools/openlane_working_dir/openlane

# alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
# Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command
docker
```
```tcl
# Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command
./flow.tcl -interactive

# Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flow
package require openlane 0.9

# Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'
prep -design picorv32a

# Adiitional commands to include newly added lef to openlane flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis
```

Commands run final screenshot

![image](https://github.com/user-attachments/assets/be635717-a3a7-4e54-895b-adfb425744bc)

![image](https://github.com/user-attachments/assets/14ac77b9-3eb8-4578-b48f-d4d9ed8b5dcf)

![image](https://github.com/user-attachments/assets/2f103c06-3e7a-4199-9229-9b0823170aa0)

![image](https://github.com/user-attachments/assets/dc7ce8b3-2932-4cf8-bc88-b510adf07804)

Newly created `pre_sta.conf` for STA analysis in `openlane` directory

![image](https://github.com/user-attachments/assets/9bc0fb8c-44ae-4d24-a292-e9b035058899)
![image](https://github.com/user-attachments/assets/0bd79b37-acbe-422b-a1ac-164d320d4624)


Newly created `my_base.sdc` for STA analysis in `openlane/designs/picorv32a/src` directory based on the file `openlane/scripts/base.sdc`

![image](https://github.com/user-attachments/assets/72efff8f-cfee-4cfc-b5b2-fc99a0a3235d)

Commands to run STA in another terminal

```bash
# Change directory to openlane
cd Desktop/work/tools/openlane_working_dir/openlane

# Command to invoke OpenSTA tool with script
sta pre_sta.conf
```

Screenshots of commands run

![image](https://github.com/user-attachments/assets/4e4fe61e-70e4-4014-a559-2cc6ea009eb2)

![image](https://github.com/user-attachments/assets/e61135ec-eebd-4c03-84f3-fff0c1ccbd96)

![image](https://github.com/user-attachments/assets/64471a18-3f94-482c-9a85-164ecd966cc8)

![image](https://github.com/user-attachments/assets/ad9915eb-aa19-4e90-bf71-7d6e50c73d41)


Since more fanout is causing more delay we can add parameter to reduce fanout and do synthesis again

Commands to include new lef and perform synthesis 

```tcl
# Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'
prep -design picorv32a -tag 03-10_23-15 -overwrite

# Adiitional commands to include newly added lef to openlane flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Command to set new value for SYNTH_MAX_FANOUT
set ::env(SYNTH_MAX_FANOUT) 4

# Command to display current value of variable SYNTH_DRIVING_CELL to check whether it's the proper cell or not
echo $::env(SYNTH_DRIVING_CELL)

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis
```

Commands run final screenshot

![image](https://github.com/user-attachments/assets/bc3aa90f-45c3-4ef8-9e1f-76e5b26488d0)|
![image](https://github.com/user-attachments/assets/5dcae1a6-73ed-45a1-a97b-26bba82cebd9)
![image](https://github.com/user-attachments/assets/e5fb44bf-4751-4236-af53-3ceca100e388)

Commands to run STA in another terminal

```bash
# Change directory to openlane
cd Desktop/work/tools/openlane_working_dir/openlane

# Command to invoke OpenSTA tool with script
sta pre_sta.conf
```

Screenshots of commands run
sta pre_sta.conf
![image](https://github.com/user-attachments/assets/8c8cee27-84ea-4f02-9342-b4b9643bf8f0)

![image](https://github.com/user-attachments/assets/f97db095-3591-441b-8e6f-5063808144d8)

![image](https://github.com/user-attachments/assets/7afc21f0-cf4d-428b-a291-18737e3e395a)

![image](https://github.com/user-attachments/assets/a16abeac-ed9b-4ef7-9e9b-b852e818501a)
![image](https://github.com/user-attachments/assets/c12e5bcb-a9ed-4ab0-8502-b47f725d8db9)


To fix this slack, we use 

```# Now once again we have to prep design so as to update variables
prep -design picorv32a -tag 03-10_23-15 -overwrite

# Addiitional commands to include newly added lef to openlane flow merged.lef
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to display current value of variable SYNTH_STRATEGY
echo $::env(SYNTH_STRATEGY)

# Command to set new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"

# Command to display current value of variable SYNTH_BUFFERING to check whether it's enabled
echo $::env(SYNTH_BUFFERING)

# Command to display current value of variable SYNTH_SIZING
echo $::env(SYNTH_SIZING)

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Command to display current value of variable SYNTH_DRIVING_CELL to check whether it's the proper cell or not
echo $::env(SYNTH_DRIVING_CELL)

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis
```

![image](https://github.com/user-attachments/assets/20cd9caa-6528-4e6c-b91f-68437018065e)

![image](https://github.com/user-attachments/assets/f5dc96cf-4c90-46b5-9ed0-b603d3342e39)



![image](https://github.com/user-attachments/assets/f5f3cd51-5f1b-4b82-a942-99b3ea8fe328)

Finally, Slack is met .

Commands to run STA in another terminal

```bash
# Change directory to openlane
cd Desktop/work/tools/openlane_working_dir/openlane

# Command to invoke OpenSTA tool with script
sta pre_sta.conf
```

Screenshots of commands run
sta pre_sta.conf

![image](https://github.com/user-attachments/assets/e07ad123-7810-4abe-bf4f-a92eedf9a95f)

![image](https://github.com/user-attachments/assets/a52ed81f-60ec-4bd8-941b-4ff048bc4738)

![image](https://github.com/user-attachments/assets/f6da427c-9bd8-4f93-85d9-7bf64a76c8f1)

![image](https://github.com/user-attachments/assets/2036505e-8bc5-41a7-b1c6-a72037978679)

![image](https://github.com/user-attachments/assets/e8d35311-1102-4fc4-a5ea-30dfbd772067)







#### 10. Replace the old netlist with the new netlist generated after timing ECO fix and implement the floorplan, placement and cts.

Now to insert this updated netlist to PnR flow and we can use `write_verilog` and overwrite the synthesis netlist but before that we are going to make a copy of the old old netlist

Commands to make copy of netlist

```bash
# Change from home directory to synthesis results directory
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-10_23-15/results/synthesis/

# List contents of the directory
ls

# Copy and rename the netlist
cp picorv32a.synthesis.v picorv32a.synthesis_old.v

# List contents of the directory
ls
```

Screenshot of commands run

![image](https://github.com/user-attachments/assets/17002043-c99b-4cdc-a6d4-6c0de4febd51)

![image](https://github.com/user-attachments/assets/631f6906-b8f1-4e45-af19-1b138572b3ef)

![image](https://github.com/user-attachments/assets/9859a74a-377b-4b22-aba8-213ede79ba1f)

![image](https://github.com/user-attachments/assets/98fa11f6-9480-4c2d-ade5-a4bfac5e79c0)

commands to write verilog 

```tcl
# Check syntax
help write_verilog

# Overwriting current synthesis netlist
write_verilog /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-10_23-15/results/synthesis/picorv32a.synthesis.v

# Exit from OpenSTA since timing analysis is done
exit
```

Screenshot of commands run




![image](https://github.com/user-attachments/assets/7d54397e-c237-42b6-81ac-e261fd928c0b)

We want to follow up on the previous 0 violation design, so we are continuing with the clean design to future stages even though we have confirmed that the netlist is replaced and will be loaded in PnR.

Commands load the design and run necessary stages

```tcl
# Now once again we have to prep design so as to update variables
prep -design picorv32a -tag 04-10_15-51 -overwrite

# Addiitional commands to include newly added lef to openlane flow merged.lef
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to set new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis

# Follwing commands are alltogather sourced in "run_floorplan" command
init_floorplan
place_io
tap_decap_or

# Now we are ready to run placement
run_placement

# Incase getting error
unset ::env(LIB_CTS)

# With placement done we are now ready to run CTS
run_cts
```

Screenshots of commands run

![image](https://github.com/user-attachments/assets/ab88f93b-b902-405f-b385-410dbe8f710d)

![image](https://github.com/user-attachments/assets/2240da25-a7b1-47d9-850a-5a96a9814c3c)


![image](https://github.com/user-attachments/assets/cd062460-8a7e-4012-9e09-98303552e077)

![image](https://github.com/user-attachments/assets/05daff2d-c561-4bb2-bb70-bdfa9e630106)

![image](https://github.com/user-attachments/assets/f24bb458-d004-4eeb-ac2d-afa531933b41)


# DAY 5 ( Final Steps for RTL2GDS using tritonRoute and OpenSTA )


### Theory

<details>
  <summary>
Expand or Collapse
  </summary>

### PDN (POWER DISTRIBUTION NETWORK)

The PDN in OpenLANE is essential for the correct distribution of power across the chip.

1) The PDN makes sure that there is enough power for all conventional cells and macros.
2) Throughout the chip, it offers a network of power rails (VDD and VSS), As, in our case, it is VPWR and VGND .

### Routing 

Routing is used to make the physical connection between pins through the use of metal layers. Routing occurs in 2 ways:- Global routing and detailed routing In Global Routing , the region of routing is divided into rectangular grids which is shown as 3D route. In Detailed Routing, To do the physical wiring finger grids and routing grids.



</details>


## Task 5

1. Perform generation of Power Distribution Network (PDN) and explore the PDN layout.
2. Perfrom detailed routing using TritonRoute.
3. Post-Route parasitic extraction using SPEF extractor.
4. Post-Route OpenSTA timing analysis with the extracted parasitics of the route.



#### 1. Perform generation of Power Distribution Network (PDN) and explore the PDN layout.

Commands to perform all necessary stages up until now

```bash
# Change directory to openlane flow directory
cd Desktop/work/tools/openlane_working_dir/openlane

# alias docker='docker run -it -v $(pwd):/openLANE_flow -v $PDK_ROOT:$PDK_ROOT -e PDK_ROOT=$PDK_ROOT -u $(id -u $USER):$(id -g $USER) efabless/openlane:v0.21'
# Since we have aliased the long command to 'docker' we can invoke the OpenLANE flow docker sub-system by just running this command
docker
```
```tcl
# Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command
./flow.tcl -interactive

# Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flow
package require openlane 0.9

# Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'
prep -design picorv32a

# Addiitional commands to include newly added lef to openlane flow merged.lef
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to set new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis

# Following commands are alltogather sourced in "run_floorplan" command
init_floorplan
place_io
tap_decap_or

# Now we are ready to run placement
run_placement

# Incase getting error
unset ::env(LIB_CTS)

# With placement done we are now ready to run CTS
run_cts

# Now that CTS is done we can do power distribution network
gen_pdn 
```

Screenshots of commands
![image](https://github.com/user-attachments/assets/135c024a-9a62-4533-bdf9-74a1c7c2e5c4)


![image](https://github.com/user-attachments/assets/5d52a97e-8737-4282-b3c6-0e7a2dbefb5a)

![image](https://github.com/user-attachments/assets/0f6eeb4e-0cf5-4b0a-8713-ebf2c5bf778a)



![image](https://github.com/user-attachments/assets/838f15da-5b4e-47f6-8017-e41f779fff62)

![image](https://github.com/user-attachments/assets/35026f8f-b498-474a-9683-1c7389a133f0)


Screenshots of power distribution network run command

![image](https://github.com/user-attachments/assets/445c0127-b0b0-4018-890a-66891fea5140)

![image](https://github.com/user-attachments/assets/be18710e-f523-4de0-a0c3-027a19f3c61e)


Commands to load PDN def in magic in another terminal

```bash
# Change directory to path containing generated PDN def
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/04-10_15-51/tmp/floorplan/

# Command to load the PDN def in magic tool
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read 14-pdn.def &
```

Screenshots of PDN def in magic 

![image](https://github.com/user-attachments/assets/cbf71c2e-a025-409c-a949-78a145933061)

![image](https://github.com/user-attachments/assets/17cf3ac4-c53d-4b3d-b44a-6b51d2cded66)

![image](https://github.com/user-attachments/assets/c75494b4-a255-41f5-b141-656cde9ccfb4)

![image](https://github.com/user-attachments/assets/79c5d2ff-cd38-444b-9730-e2dd0c46b465)


#### 2. Perfrom detailed routing using TritonRoute and explore the routed layout.

Command to perform routing

```tcl
# Check value of 'CURRENT_DEF'
echo $::env(CURRENT_DEF)

# Check value of 'ROUTING_STRATEGY'
echo $::env(ROUTING_STRATEGY)

# Command for detailed route using TritonRoute
run_routing
```

Screenshots of routing run
![image](https://github.com/user-attachments/assets/f14926f5-9e61-4eed-a300-d36aa8acd11b)



![image](https://github.com/user-attachments/assets/16be3134-fa05-4cc6-8ab0-22aeb84df06a)


![image](https://github.com/user-attachments/assets/9a5f175f-e26e-4407-9706-74fc0b73754e)





















Commands to load routed def in magic in another terminal

```bash
# Change directory to path containing routed def
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/04-10_15-51/results/routing/

# Command to load the routed def in magic tool
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.def &
```

Screenshots of routed def


![image](https://github.com/user-attachments/assets/9ce875fa-dc4a-409c-acd0-fbd015e26fe0)

![image](https://github.com/user-attachments/assets/c3b76cce-c2bb-4538-9f0c-985b44b51632)



![image](https://github.com/user-attachments/assets/2eed353c-57fa-4061-b8e0-7315320abd55)


![image](https://github.com/user-attachments/assets/0c76d338-568c-4ba4-acb1-4436e7eb4bfd)


![image](https://github.com/user-attachments/assets/27c35e7d-3559-4f16-9e19-d87700b22033)



![image](https://github.com/user-attachments/assets/aabaf173-b73b-4316-b10b-4f20ddebff60)

Screenshot of fast route guide present in `openlane/designs/picorv32a/runs/04-10_15-51/tmp/routing` directory

![image](https://github.com/user-attachments/assets/57b8b6af-e662-403c-aee2-e2b3210977fa)



#### 3. Post-Route parasitic extraction using SPEF extractor.

Commands for SPEF extraction using external tool

```bash
# Change directory
cd Desktop/work/tools/SPEF_EXTRACTOR

# Command extract spef
python3 main.py /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/04-10_15-51/tmp/merged.lef /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/04-10_15-51/results/routing/picorv32a.def
```

#### 4. Post-Route OpenSTA timing analysis with the extracted parasitics of the route.

Commands to be run in OpenLANE flow to do OpenROAD timing analysis with integrated OpenSTA in OpenROAD

```tcl
# Command to run OpenROAD tool
openroad

# Reading lef file
read_lef /openLANE_flow/designs/picorv32a/runs/04-10_15-51/tmp/merged.lef

# Reading def file
read_def /openLANE_flow/designs/picorv32a/runs/04-10_15-51/results/routing/picorv32a.def

# Creating an OpenROAD database to work with
write_db pico_route.db

# Loading the created database in OpenROAD
read_db pico_route.db

# Read netlist post CTS
read_verilog /openLANE_flow/designs/picorv32a/runs/04-10_15-51/results/synthesis/picorv32a.synthesis_preroute.v

# Read library for design
read_liberty $::env(LIB_SYNTH_COMPLETE)

# Link design and library
link_design picorv32a

# Read in the custom sdc we created
read_sdc /openLANE_flow/designs/picorv32a/src/my_base.sdc

# Setting all cloks as propagated clocks
set_propagated_clock [all_clocks]

# Read SPEF
read_spef /openLANE_flow/designs/picorv32a/runs/04-10_15-51/results/routing/picorv32a.spef

# Generating custom timing report
report_checks -path_delay min_max -fields {slew trans net cap input_pins} -format full_clock_expanded -digits 4

# Exit to OpenLANE flow
exit

```


Screenshots of commmand run and timing report generated

![image](https://github.com/user-attachments/assets/5485fb4a-d2a3-484d-9359-565ef125b7a7)

![image](https://github.com/user-attachments/assets/2a1d36d5-8e15-48ed-aa58-49c22174e1a4)

![image](https://github.com/user-attachments/assets/ea481370-7296-447f-8baa-c873b0fb023a)

![image](https://github.com/user-attachments/assets/1d973790-5e19-4ab1-b109-c1aa388590dd)

![image](https://github.com/user-attachments/assets/5855ab1b-a8fb-4a01-b4fc-a36ea2742103)


## References

- [GitLab/OpenLane workshop](https://gitlab.com/gab13c/openlane-workshop)
- [The OpenROAD Project/OpenLane](https://github.com/The-OpenROAD-Project/OpenLane)
- Ahmed Ghazy and Mohamed Shalan, "OpenLane: The Open-Source Digital ASIC Implementation Flow", Article No.21, Workshop on Open-Source EDA Technology (WOSET), 2020. [Paper](https://github.com/woset-workshop/woset-workshop.github.io/blob/master/PDFs/2020/a21.pdf)
- [YOUTUBE/OpenLane Overview](https://www.youtube.com/watch?v=d0hPdkYg5QI)
- [GitHUB/openlane_build_script](https://github.com/nickson-jose/openlane_build_script)
- [GitLab/OpenLANE-Sky130-Physical-Design-Workshop](https://github.com/ripudamank2/OpenLANE-Sky130-Physical-Design-Workshop)
-[Udemy course/VSD-a-complete-guide-to-install-open-source-eda-tools)






# Acknowledgements

* [Kunal Ghosh](https://github.com/kunalg123), Co-founder, VSD Corp. Pvt. Ltd.
* [Nickson P Jose](https://github.com/nickson-jose), Physical Design Engineer, Intel Corporation.
* [R. Timothy Edwards](https://github.com/RTimothyEdwards), Senior Vice President of Analog and Design, efabless Corporation.



# Certificate of Completion

[nasscom certificate.pdf](https://github.com/user-attachments/files/17533879/nasscom.certificate.pdf)




## Author


- [Vanshika Tanwar](https://github.com/VanshikaTanwar), Bachelor of Technology in Electronics & Communication Engineering,Dronacharya Group of Institutions,Greater Noida, U.P.
