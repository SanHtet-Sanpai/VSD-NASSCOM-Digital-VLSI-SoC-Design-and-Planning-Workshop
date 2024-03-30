# VSD-NASSCOM-Digital-VLSI-SoC-Design-and-Planning-Workshop
Documentation of Workshop Deliverables

# Table of Contents
- [Day 1](##Day1)
    - [Task](###Task)
    - [Steps](###StepstorunSynthesis)
    - [Results](###Results) 

   
## Day 1
### Task
1. Run 'picorv32a' design synthesis using OpenLANE flow and generate necessary outputs.
2. Calculate the flop ratio.

### Steps to run Synthesis
````
#Step 1: go to openlane directory in vm instance
cd Desktop/work/tools/openlane_working_dir/openlane 

#Step 2: initiate docker sub-system
docker

#Step 3: invoke openlane flow in interactive mode
./flow.tcl -interactive

#Step 4: load required packages 
package require openlane 0.9

#Step 5: prepare necessary files and variables etc to synthesize design - picorv32a
prep -design picorv32a

#Step 6: run synthesis
run_synthesis

#Step 7: exit from openlane flow
exit

#Step 8: exit from docker sub-system
exit
````

### Results
![1](https://github.com/SanHtet-Sanpai/VSD-NASSCOM-Digital-VLSI-SoC-Design-and-Planning-Workshop/blob/main/Day%201/day%201_1.png)

First navigated to openlane directory and the flow is invoked in interactive mode

![2](https://github.com/SanHtet-Sanpai/VSD-NASSCOM-Digital-VLSI-SoC-Design-and-Planning-Workshop/blob/main/Day%201/day%201_2.png)

Then, the required packages are loaded and necessary design files and variables are initialized

![3](https://github.com/SanHtet-Sanpai/VSD-NASSCOM-Digital-VLSI-SoC-Design-and-Planning-Workshop/blob/main/Day%201/day%201_3.png)

Synthesis was run successfully

![4](https://github.com/SanHtet-Sanpai/VSD-NASSCOM-Digital-VLSI-SoC-Design-and-Planning-Workshop/blob/main/Day%201/day%201_4.png)

To calculate flop ratio, navigate to the report directory of this particular synthesis run as shown above

![5](https://github.com/SanHtet-Sanpai/VSD-NASSCOM-Digital-VLSI-SoC-Design-and-Planning-Workshop/blob/main/Day%201/day%201_5.png)

From the synthesis statistics report, it can be observed that there are a total of 14876 cells used for our design of which 1613 are flip-flops. 
Therefore, 

```math
Flop\ Ratio = \frac{1613}{14876} = 0.108429685
```
```math
Percentage\ of\ DFF's = 0.108429685 * 100 = 10.84296854\ \%
```



