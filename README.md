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

## DAY 1

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


# Task 1
To calculate the Flop Ratio 

- For Calculating the Flop Ratio ,with reference of number of D flip flops to number of cells , the following formula has been used 
```math
Flop\ Ratio = \frac{Number\ of\ D\ Flip\ Flops}{Total\ Number\ of\ Cells}
```
```math
Percentage\ of\ DFF's = Flop\ Ratio * 100
```

1) How to open the Openlane Tool 

a) First of all, open the terminal and change the directory to openlane where , openlane exists 

`cd Desktop/work/tools/openlane_working_dir/openlane`

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
 






