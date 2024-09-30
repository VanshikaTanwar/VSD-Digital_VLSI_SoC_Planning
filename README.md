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

# DAY 1 ( Inception of Opensource EDA , OpenLANE and SKY130 PDK )

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


## Task 3 - Design library cell using Magic Layout and ngspice characterization
Inverrter Characterization using SKY130 Model File 



### Theory

<details>
  <summary>
Expand or Collapse
  </summary>

</details>


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

![Screenshot from 2024-03-19 14-56-42](https://github.com/fayizferosh/soc-design-and-planning-nasscom-vsd/assets/63997454/c023ebb0-756f-4707-ae82-a28746f372da)
![Screenshot from 2024-03-19 14-57-22](https://github.com/fayizferosh/soc-design-and-planning-nasscom-vsd/assets/63997454/addefe5e-6a9a-44f2-943a-4a9373ddc56c)

Screenshot of generated plot






































