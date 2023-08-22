# Samsung-PD-Training-
## Day-0-Installation
<details>
 <summary> Summary </summary>
	
I installed the needed tools and attached the required screenshots:

</details>	
	
 <details>
 <summary> Yosys </summary>
Yosys is an open-source framework for Verilog RTL synthesis. RTL stands for Register Transfer Level, which is a high-level abstraction used to describe digital circuits at the level of registers and their interactions. Yosys is primarily used in the digital design and electronic design automation (EDA) community to convert RTL descriptions of digital circuits, written in languages like Verilog or SystemVerilog, into a netlist representation that can be further optimized, analyzed, and eventually implemented in hardware.

I installed Yosys using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="yosys" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/15cd9fc2d5f7e147dbf66f4e86b6aa86651db3cd/PD%23day0/Yosys.png">
</details>
--------------------------------

 <details>
 <summary> GTK Wave </summary>

GTKWave is an open-source waveform viewer and analyzer primarily used in digital design and electronic design automation (EDA) workflows. It allows users to visualize and analyze the waveforms generated by digital simulations, making it a valuable tool for debugging and verifying digital designs.

I installed GTKwave using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="GTKwave" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/012a981015cee8c90ff3835ed3e9e20acd1debe9/PD%23day0/gtkwave.png">
</details>
--------------------------------

 <details>
 <summary> ICC2 </summary>

It appears that "icc2 compiler" might refer to an abbreviation of "Intel C++ Compiler 2," which would be the second version of Intel's C++ compiler. Intel's C++ Compiler is a tool used to compile C and C++ programs, optimizing them for Intel processors and architectures. It offers features like advanced vectorization, parallelization, and optimization techniques to enhance the performance of code on Intel-based systems.

I installed ICC2 using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="ICC2" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/b7aea8ac24074b02355ba3408d84098f825ac56a/PD%23day0/icc2.png">
</details>
------------------------------

<details>
 <summary> lc_shell </summary>

LC_shell, also known as Design Compiler Graphical, is a part of the Synopsys suite of Electronic Design Automation (EDA) tools. It's used in the digital design flow for logic synthesis and optimization. Design Compiler Graphical is an advanced version of the original Design Compiler tool, providing additional features and a more user-friendly graphical interface.
I invoked lc_shell using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="lc_shell" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/f9c32b3af96086cb1823ea7b5a1d96ad524c6907/PD%23day0/lc_shell.png">
</details>
-------------------------------

<details>
 <summary> dc_shell </summary>

Design Compiler is a widely used electronic design automation (EDA) tool developed by Synopsys. It's primarily used for logic synthesis in digital integrated circuit design. Logic synthesis involves transforming a high-level description of a digital circuit (usually written in hardware description languages like Verilog or VHDL) into a lower-level representation made up of gates, flip-flops, and other basic digital components.
I invoked dc_shell using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="dc_shell" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/c1c917d6ea2259e11eb35c8210a5ba5d033efc98/PD%23day0/lc_shell1.png">
</details>
------------------------------

<details>
 <summary> pt_shell </summary>

"PrimeTime" is a widely used Electronic Design Automation (EDA) tool developed by Synopsys. It is used for static timing analysis, which is a crucial step in the digital design flow to ensure that the design meets its timing requirements. The "PrimeTime Shell" is the user interface through which engineers interact with the PrimeTime tool to perform timing analysis and optimization.
I invoked pt_shell using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="pt_shell" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/a698767d9372140b08254434b15860f0db8169e2/PD%23day0/pt_shell.png">
</details>



## Day-1-Introduction to Verilog RTL Design and Synthesis
<details>
 <summary> Introduction to RTL-Design, Test-bench, Simulators </summary>
-RTL Design : The RTL Design stands for Register Transfer Language. It sits between the high-level system specification and the lower-level gate-level implementation. This is a design abstraction which models the flow of digital signals between hardware registers, and the logical operations performed on those signals. RTL is preferred because it is easy to understand and implement compared to structural and behavioral models.

-HDL : A hardware description language (HDL) enables a precise, formal description of an electronic circuit that allows for the automated analysis and simulation of an electronic circuit.

-Simulator : Simulator is the tool used for checking adherence to the specification by simulating the design. iverilog is the tool used for RTL simulation. A simulator looks for change in the input signals and when no change in input, the output also doesn't change. It produces an output in the form of a .vcd file.

-Design : Design is the actual verilog code or set of Verilog codeswhich has the intended functionality to meet the required specifications. Design may have one or more primary inputs or primary outputs.  RTL design is the behavioral representation of the required specification.


<details>
<summary> Labs on examples of iverilog and gtkwave </summary>
We made a directory namely VLSI and inside that directory we cloned vsdflow and sky130RTLDesignAndSynthesisWorkshop repository. This repository consists of the required .lib files and verilog codes and its testbenches for practice.
Below is the output wave form in gtkwave generated by performing a simulation of good_mux using iverilog.
The syntax of the code is: iverilog <RTL_code> <Its_Testbench>
<img width="1085" alt="lc_shell" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/35b6b9038bf5a6c855c534a868c02bdfc149bfa3/PD%23Day1/gtk_wave_mux.PNG">
RTL code and testbench for good_2:1_mux
<img width="1085" alt="lc_shell" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/35b6b9038bf5a6c855c534a868c02bdfc149bfa3/PD%23Day1/rtl_code.PNG">
</details>
</details>

<details>
 <summary> Introduction to Yosys </summary>
-Synthesis: Synthesis in VLSI is the process of converting your code (program) into a circuit. In terms of logic gates, synthesis is the process of translating an abstract design into a properly implemented chip. It is a process of converting a RTL code into a gate level netlist. The tool used for this purpose is called synthesizer.

-Yosys : Yosys is a framework for RTL synthesis and more. It currently has extensive Verilog-2005 support and provides a basic set of synthesis algorithms for various application domains. Yosys is the core component of most our implementation and verification flows.

-Verification of synthesized design : In order to make sure that there are no errors in netlist we need to verify the netlist generated by synthesizer. This can be done by giving netlist and testbench to a simulator which in turn produces a .vcd file , then verifying the vcd file gtkwave. The output produced by this vcd file should be same as the one generated by the RTL design code.

-Faster Cells Vs Slower Cells :Load in digital circuit is of Capacitence. Faster the charging or dicharging of capacitance, lesser is the celll delay. However, for a quick charge/ discharge of capacitor, we need transistors capable of sourcing more current i.e, we need WIDE TRANSISTORS.

Transistors with higher W/L have lesser delay but consume more area and power while Transistors with less W/L has more delay and less area. Faster cells come with a cost of area and power.

Selection of the Cells: Based on timing constraints we need select the cell. Setup supports faster cells in datapath while hold supports slower. We need to select suitable which can satisfy both constraints.
<details>
 <summary> Lab work on Yosys </summary>
We were given the overview of this tool and the basic files required to perform the experiment on 2:1 MUX.
Procedure : First we need to read the liberty file (.lib) using the code: read_liberty -lib <path of the .lib>


Read the RTL code:

read_verilog <RTL_Design_file>

For synthesis:

synth -top <instance_name>

For Generating netlist:

abc -liberty <.lib path>  --------<present_on_lib_folder>
This Netlist can be viewed in the synthesized circuit form which uses std. cell present in .lib using the show command :
<img width="1085" alt="lc_shell" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/19c8df9a79de2fb33db16e1d9e3e8b95a55a64b8/PD%23Day1/Yosys_netlist.PNG">
</details>
</details>



## Day-2-ntroduction to Timing libraries, Hierarchical vs flat synthesis, and flip flop coding

<details>
 <summary> Introduction to Timing Library File (.Lib) </summary>
Liberty File(.lib) contains important info about the electrical behavior  of std cells used in IC design. Also, Liberty File(.lib) consists of ASCII representations of Timing, Area, and Power associated with the Standard cell. The Naming convention in the timing file follows technology node and PVT format (Process, Voltage, Temperature). For example, the standard library used in our case was sky130_fd_sc_hd_tt_025C_1v8, this name suggests that we are using 130 nm technology and the process is typical(tt), temperature is 25C, and 1v8 represents the 1.8V.
Screenshot of a standard library file shown below: 
<img width="1085" alt="lib" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/6e256528c8de9193640fb445f589071e23beeee5/PD%23Day2/lib_part1.PNG">
	
The Liberty File also consists of the technology used for standard cells as in the above example it is CMOS, it also specifies the delay model, unit of time, unit of voltage, unit of resistance, and many other units.
All the data i.e std cells delays, leakage power, capacitance is stored in form of LUTs. For each gate cell based on the number of inputs(N), there will be 2^N combinations, and for each combination leakage power, area, delay, and all related parameters are mentioned. For example, consider the below screenshot the gate mentioned in the screenshot consists of 4 inputs so there will be 16 combinations, and for all the combinations power, delay, value, and all the features are mentioned below.
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/6e256528c8de9193640fb445f589071e23beeee5/PD%23Day2/lib_part2.PNG">
	
The timing file consists of many different variations of the same gate cells. As we move toward faster cell (cell with higher drive strength) the area and power increases. In liberty file area, power, timing values are given for same cell of different drive strength and it also consist if the inform about leakage power of all the possible logic of different configration shown below.
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/a69147a2bedd2c78636125b3b35b7996fa55659e/PD%23Day2/lib_part3.PNG">
</details>

<details>
 <summary> Hierarchical vs Flat synthesis in Yosys </summary>
Hierarchical synthesis : The basic flow of hierarchical design is Dividing a design into multiple blocks (i.e. sub-chips, sub-blocks, modules, hierarchical blocks, etc.) which can also be user defined. Hierarchial design has blocks, subblocks in an hierarchy.
In Yosys we have done synthesis of a multimodule combinational circuit which consists of two sub_modules one that of ** AND ** gate and other of ** OR ** gate. Below is the RTL Design code of multimodules is gvien below:
	
```
module sub_module2 (input a, input b, output y);
        assign y = a | b;
endmodule

module sub_module1 (input a, input b, output y);
        assign y = a&b;
endmodule


module multiple_modules (input a, input b, input c , output y);
        wire net1;
        sub_module1 u1(.a(a),.b(b),.y(net1));  //net1 = a&b
        sub_module2 u2(.a(net1),.b(c),.y(y));  //y = net1|c ,ie y = a&b + c;
endmodule
```
We do synthesis in yosys it generates the following gate level netlist :

<img width="1085" alt="lib" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/7d2732dc1300198990edfb77ed38ef0cff0db911/PD%23Day2/hire_synth.PNG">

The yosys considers the module hierarchy and does mapping according to the instantiation i.e by using sub blocks.The netlist code for hierarchical implementation of the multiple_modules.
```
module multiple_modules(a, b, c, y);
	  input a;
	 input b;
	 input c;
	  wire net1;
	 output y;
  sub_module1 u1 (.a(a),.b(b),.y(net1) );
  sub_module2 u2 (.a(net1),.b(c),.y(y));
endmodule

module sub_module1(a, b, y);
 wire _0_;
 wire _1_;
 wire _2_;
 input a;
 input b;
 output y;
 sky130_fd_sc_hd__and2_0 _3_ (.A(_1_),.B(_0_),.X(_2_));
 assign _1_ = b;
 assign _0_ = a;
 assign y = _2_;
endmodule

module sub_module2(a, b, y);
wire _0_;
 wire _1_;
 wire _2_;
input a;
input b;
 output y;
 sky130_fd_sc_hd__lpflow_inputiso1p_1 _3_ (.A(_1_),.SLEEP(_0_),.X(_2_) );
 assign _1_ = b;
 assign _0_ = a;
 assign y = _2_;
endmodule
```
In the netlist it can observed that separate modules namely sub_module1 sub_module2 are created  i.e submodules are getting instanstiated not the std cells presnt in library.
