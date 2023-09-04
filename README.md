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



## Day-2-Introduction to Timing libraries, Hierarchical vs flat synthesis, and flip flop coding

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
	Synthesis Simulation Mismatch
```
module sub_module2 (input a, input b, output y);
        assign y = a | b;
endmodule

module sub_module1 (input a, input b, output y);
        assign y = a&b;
endmodule
```

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
In the netlist it can observed that separate modules namely sub_module1 sub_module2 are created  i.e submodules are getting instanstiated not the std cells present in library.

Flat synthesis : In Flat synthesis the hierarchies the flattened out and every submodule is created using std cells. We apply flat synthesis on the same design mentioned above. The command used to perform Flat synthesis from yosys are as follows :

--- read_liberty -lib <path of the .lib>

--- read_verilog <RTL_file>

--- synth -top <instance_name>

--- abc -liberty <.lib_path>

--- flatten

--- write_verilog -noattr <.v_File_name>
The synthesized circuit for a flattened netlist is shown in the below: 

<img width="1085" alt="lib" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/227e10459da8569b3bc7ac52f8bc2d389068a278/PD%23Day2/flatten_synth.PNG">
</details>

<details>
 <summary> Flip-flop Coding Styles </summary>

 Flip-flops :A flip-flop is a sequential digital electronic circuit having two stable states that can be used to store one bit of binary data. Flip-flops are the fundamental building blocks of all memory devices.

 The complexity of cobinational circuit increases the chance of glitch, hence FFs are used to avoid it and it stable output.

 Asynchronous Reset D Flop: 
 
 Here the output signal goes low when the reset signal is high , irrespective of the clock's edge(+ve,-ve or dual edge ).
 RTL Design code of positive edge trigerred asynchronous reset D FF:
 ```
module dff_asyncres ( input clk ,  input async_reset , input d , output reg q );
	always @ (posedge clk , posedge async_reset)
	begin
		if(async_reset)
			q <= 1'b0;
		else	
			q <= d;
	end
endmodule
```
Its gtkwave :<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/7b832441e73dd5c5bc078425a1f34ee4dea508fd/PD%23Day2/asyn_dff_gtk.png">

Its Yosys synthesised netlist:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/7b832441e73dd5c5bc078425a1f34ee4dea508fd/PD%23Day2/asyn_rst_synth.png">

Asynchronous set D Flop:

Here the output signal goes high when the reset signal is high , irrespective of the clock's edge(+ve,-ve or dual edge ).
 RTL Design code of positive edge trigerred asynchronous set D FF:
 ```
module dff_async_set ( input clk ,  input async_set , input d , output reg q );
	always @ (posedge clk , posedge async_set)
	begin
		if(async_set)
			q <= 1'b1;
		else
			q <= d;
	end
endmodule
```

Its GTKwave :
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/7e6fa6fc208da635a0ef187a306d8c35f51fa7b8/PD%23Day2/asyn_set_gtk.png">

Its Yosys synthesised netlist:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/7e6fa6fc208da635a0ef187a306d8c35f51fa7b8/PD%23Day2/async_sett_synth.png">

Synchronous reset D Flop :

The reset depend on the clock edge. Here the output signal goes low whenever the reset signal is high and at the clock edge(positive or negative)
RTL Design code of positive edge trigerred synchronous reset D FF:
```
module dff_syncres ( input clk , input async_reset , input sync_reset , input d , output reg q );
	always @ (posedge clk )
	begin
		if (sync_reset)
			q <= 1'b0;
		else	
			q <= d;
	end
endmodule
```

Its GTKwave :
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1710b01447acaaf9d5dd46085c2de830b13d0052/PD%23Day2/sync_rst_gtk.png">

Its Yosys synthesised netlist:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1710b01447acaaf9d5dd46085c2de830b13d0052/PD%23Day2/sync_rst_synth.png">
</details>


<details>
 <summary> Optimization Techniques </summary>
 The Optimization involves the reducing hardware in the design to improve area, power and speed. Two example where given:
 1. a*2
Consider a case where 3 bit number is multiplied by 2 in this case we dont need any additional hardware and only needs connecting bits to the output and grounding the LSB bit,same is realized by yosys. When binary number is multiplied by 2^n then result will gave same number by appending zero in LSB by n times.
RTL code:
	
```
	module mul2 (input [2:0] a, output [3:0] y);
	assign y = a * 2; // assign y={a,1'b0}
	endmodule
```

Yosys Synthesis result : 
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/323e37b40a9b040ec9f029d9378732b9acbb65b0/PD%23Day2/mult2_synth.png">

 2. a*9
Multiplying a 3 bit number by 9, gives results as concatination of same number twice {a,a}.
a*[8+1]= {a,0,0,0} + a(3bit)={a,a}

RTL code:

```
module mul8 (input [2:0] a, output [5:0] y);
	assign y = a * 9; // assign y={a,a}
endmodule
```

Yosys Synthesis result : 
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/323e37b40a9b040ec9f029d9378732b9acbb65b0/PD%23Day2/mult8_synth.png">
</details>


## Day-3- Combinational and sequential optmizations

<details>
 <summary> Combinational Optimization </summary>
Optimising the combinational logic circuit is squeezing the logic to get the most optimized digital design so that the circuit finally is area and power efficient. This is achieved by the synthesis tool using various techniques and gives us the most optimized circuit.
Command to optimize the circuit by yosys is yosys> opt_clean -purge
We have done synthesis using yosys for few examples:

*Example 1*
```
module opt_check (input a , input b , output y);
	assign y = a?b:0;
endmodule
```
yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/opt_check_synth.png">
In this verilog code represents the mux but as one of the input 0 , it infers an AND gate as shown in synthesis.


*Example 2*
```
module opt_check2 (input a , input b , output y);
	assign y = a?1:b;
endmodule
```
yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/opt_check2_synth.png">
In this verilog code represents the mux but as one of the input 1, it infers an AND gate as shown in synthesis.

*Example 3*
```
module opt_check3 (input a , input b, input c , output y);
	assign y = a?(c?b:0):0;
endmodule
```
yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/opt_check3_synth.png">   
In this verilog code represents the 2 mux but as two of the input 0, it infers an 3 i/p AND gate as shown in synthesis.


*Example 4*
```
module opt_check4 (input a , input b , input c , output y);
	assign y = a?(b?(a & c ):c):(!c);
endmodule
```
yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/opt_check4_synth.png">   
In yosys we can see b is never changed follows xnor of a and c inputs.

Generated nelist:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/opt_check4_netlist.png">   
So, here input b is passed through buffer and a and c inputs is xnored followed by buffers in inputs and output.

*Example 5*
Here there is multiple modules present so we will try to check whether those module are being used or not and we use flatten for submudules
read_liberty -lib <library_path>

read_verilog <verilog_file>

synth -top <module_name>

opt_clean -purge

abc -liberty <library_path>

flatten
```
module sub_module1(input a , input b , output y);
	 assign y = a & b;
	endmodule

	module sub_module2(input a , input b , output y);
	 assign y = a^b;
	endmodule

	module multiple_module_opt(input a , input b , input c , input d , output y);
	wire n1,n2,n3;
	sub_module1 U1 (.a(a) , .b(1'b1) , .y(n1));
	sub_module2 U2 (.a(n1), .b(1'b0) , .y(n2));
	sub_module2 U3 (.a(b), .b(d) , .y(n3));

	assign y = c | (b & n1); 
	endmodule
```
yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/multi_module_opt.png">   

Generated nelist:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/multi_module_opt_netlist.png">  

*Example 6*

```
module sub_module(input a , input b , output y);
	assign y = a & b;
endmodule

module multiple_module_opt2(input a , input b , input c , input d , output y);
	wire n1,n2,n3;
	sub_module U1 (.a(a) , .b(1'b0) , .y(n1));
	sub_module U2 (.a(b), .b(c) , .y(n2));
	sub_module U3 (.a(n2), .b(d) , .y(n3));
	sub_module U4 (.a(n3), .b(n1) , .y(y));
endmodule
```
yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/multi_module_opt2_synth.png">   

Generated nelist:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/1d9c6f5e15302e6dc799ad643bcc537094b6c5da/PD%23Day3/multi_module_opt2_netlist.png">  
</details>

<details>
 <summary> Sequential Optimization </summary>
There are various techniques for Sequential Logic Optimization

    - Sequentialal constant propagation

    - Advanced

        - State Optimization

        - Retiming

        - Sequential Logic cloning

 Sequential Constant Propogation

Consider a case where asynchronous reset D Flip-flop is fed with d = 0(i.e GND) always so the output will always be 0 irrespective of the timing or circuit.

 Advanced

State Optimisation: This is optimisation of unused state. Using this technique we can come up with most optimised state machine.

Cloning : It is an optimization technique that duplicates a cell to reduce the load on heavily loaded cell. This technique is usually preffered while performing PHYSICAL AWARE SYNTHESIS. Lets consider a flop A which is connected to flop B and flop C through a combination logic. If B and C are placed far from A in the flooerplan, there is a routing path delay. To avoid this, we connect A to two intermediate flops and then from these flops the output is sent to B and C thereby decreasing the delay. This process is called cloning since we are generating two new flops with same functionality as A.

Retiming : Sequential circuits can be optimised by retiming. The combinational section of the circuitry is unaffected as it only rearranges the registers in the circuit. It is a powerful sequential optimization technique used to move registers across the combinational logic or to optimize the number of registers to improve performance via power-delay trade-off, without changing the input-output behavior of the circuit.

Sequential Constant Propogation

Consider a case where asynchronous reset D Flip-flop is fed with d = 0(i.e GND) always so the output will always be 0 irrespective of the timing or circuit.
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/8af801e512e9a291e7cd6dd36255eddba1c168d0/PD%23Day3/image.jpg">   


*Example 1*
```
module dff_const1(input clk, input reset, output reg q);
	always @(posedge clk, posedge reset)
	begin
		if(reset)
			q <= 1'b0;
		else
			q <= 1'b1;
	end
endmodule
```
GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/bc0648ea65f00f921b633d7c79e1c442241a9c28/PD%23Day3/dff_const1_gtk.png">   



Yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/bc0648ea65f00f921b633d7c79e1c442241a9c28/PD%23Day3/dff_const1_synth.png">   

*Example 2*
```
module dff_const2(input clk, input reset, output reg q);
	always @(posedge clk, posedge reset)
	begin
		if(reset)
			q <= 1'b1;
		else
			q <= 1'b1;
	end
endmodule
```

Yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/bc0648ea65f00f921b633d7c79e1c442241a9c28/PD%23Day3/dff_const2_synth.png">
Irrespective of clock edge , output will always is 1. So buffer is  inffered.

*Example 3*
```
module dff_const3(input clk, input reset, output reg q);
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b0;
		end
		else
		begin
			q1 <= 1'b1;
			q <= q1;
		end
	end
	endmodule
```

GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/bc0648ea65f00f921b633d7c79e1c442241a9c28/PD%23Day3/dff_const3_gtk.png">   



Yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/bc0648ea65f00f921b633d7c79e1c442241a9c28/PD%23Day3/dff_const3_synth.png">   

*Example 4*
```
module dff_const4(input clk, input reset, output reg q);
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b1;
		end
	else
		begin
			q1 <= 1'b1;
			q <= q1;
		end
	end
	endmodule
```

GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/bc0648ea65f00f921b633d7c79e1c442241a9c28/PD%23Day3/dff_const4_gtk.png">   



Yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/bc0648ea65f00f921b633d7c79e1c442241a9c28/PD%23Day3/dff_const4_synth.png">   

*Example 5*
```
module dff_const5(input clk, input reset, output reg q);
	reg q1;
	always @(posedge clk, posedge reset)
		begin
			if(reset)
			begin
				q <= 1'b0;
				q1 <= 1'b0;
			end
		else
			begin
				q1 <= 1'b1;
				q <= q1;
			end
		end
	endmodule
```
GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/26c2ba861dfaf28ca7e75d2913c070226c8a5285/PD%23Day3/dff_const5_gtk.png">   



Yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/26c2ba861dfaf28ca7e75d2913c070226c8a5285/PD%23Day3/dff_const5_synth.png"> 
</details>


<details>
 <summary> Optimization Examples </summary>
	
*Example 1*
```
   module counter_opt (input clk , input reset , output q);
   reg [2:0] count;
   assign q = count[0];
   always @(posedge clk ,posedge reset)
   begin
   	if(reset)
   		count <= 3'b000;
   	else
   		count <= count + 1;
   end
   endmodule
   ```
   
Yosys generated gui:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/26c2ba861dfaf28ca7e75d2913c070226c8a5285/PD%23Day3/counter_opt_synth.png">
</details>

<details>
 <summary> Summary </summary>

 In Day 3 , It started with optimizing methodology, which involves the cost function. Cost funtion consist of following parts: 
 - Max delay Cost 
 - Min delay Cost 
 - Max Power Cost
 - Max area Cost

In optimization we seen few examples of sequential and combinational circuits based on different algorithms. 
</details>



## Day-4- GLS,blocking vs non-blocking and Synthesis-Simulation mismatch

<details>
<summary> GLS Concepts And Flow Using Iverilog </summary>

-- What is GLS- Gate Level Simulation?:
GLS is generating the simulation output by running test bench with netlist file generated from synthesis as design under test. Netlist is logically same as RTL code, therefore, same test bench can be used for it.

-- Why GLS?:
We perform this to verify logical correctness of the design after synthesizing it. Also ensuring the timing of the design is met.

Below picture gives an insight of the procedure. Here while using iverilog, we also include gate level verilog models to generate GLS simulation.

<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/d17cd858582bb157db097c5bdab07548794e008d/PD%23Day4/IMG_6766.png">
Example :
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/8d9343b03653b5480cb54ca9d97e32782986ba8c/PD%23Day4/IMG_6768.jpeg">

*Synthesis Simulation Mismatch* 
There are three main reasons for Synthesis Simulation Mismatch:

   -- Missing sensitivity list in always block
   -- Blocking vs Non-Blocking Assignments
   -- Non standard Verilog coding
Missing sensitivity list in always block:
Lets take example of mux having inputs as i0,i1 and sel and output as y.
```
always @(sel)                  always @(*)
//It will infer a latch        // It will infer a mux.
```
If i0 and i1 changes will not be reflected in always block.
To avoid the synthesis and simulation mismatch. It is very important to check the behaviour of the circuit first and then match it with the expected output seen in simulation and make sure there are no synthesis and simulation mismatches. This is why we use GLS.

Blocking vs Non-Blocking Assignments:
Blocking statements execute the statemetns in the order they are written inside the always block. Non-Blocking statements execute all the assignment parallelly inside a always block.
This will give mismatch as sometimes, improper use of blocking statements can create latches. 
Example
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/8d9343b03653b5480cb54ca9d97e32782986ba8c/PD%23Day4/IMG_6769.jpeg">
</details>

<details>
<summary> LABs </summary>
	
*Example 1*
In this example there is no mismatch between the RTL Design simulated wave and Netlist simulated wave.
```
module ternary_operator_mux (input i0 , input i1 , input sel , output y);
   assign y = sel?i1:i0;
endmodule
```
Gtkwave:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/8ec9152185e79565ae1d1439d3b644e20bdb8cbd/PD%23Day4/ternary_gtk.png">

Yosys result: 
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/8ec9152185e79565ae1d1439d3b644e20bdb8cbd/PD%23Day4/ternary_synth.png">

GLS Simulation:
I used the below commands to carry out GLS of ternary_operator_mux.v:
```
iverilog <path to verilog model: ../mylib/verilog_model/primitives.v> <path to sky130_fd_sc_hd__tt_025C_1v80.lib: ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib> <name netlist: ternary_operator_mux_net.v> <name testbench: tb_ternary_operator_mux.v>
./a.out
gtkwave tb_ternary_operator_mux.vdc
```

<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/8ec9152185e79565ae1d1439d3b644e20bdb8cbd/PD%23Day4/ternary_result_gtk.png">

*Example 2*
```
module bad_mux (input i0 , input i1 , input sel , output reg y);
	always @ (sel)
	begin
		if(sel)
			y <= i1;
		else 
			y <= i0;
	end
endmodule
```
Gtkwave:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/90b875b162a2b4374c14537fc8a9b21f6d598dee/PD%23Day4/bad_mux_gtk.png">

Yosys result: 
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/8ec9152185e79565ae1d1439d3b644e20bdb8cbd/PD%23Day4/ternary_synth.png">

GLS Simulation:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/90b875b162a2b4374c14537fc8a9b21f6d598dee/PD%23Day4/bad_mux_result_gtk.png">

Summary :Here first pic shows the netlist simulation which corrects the bad_mux design which was only changing waveform when sel was triggered while for a mux to work properly it should be sensitivity to all the input signals.

*Example 3*
```
module blocking_caveat (input a , input b , input  c, output reg d); 
reg x;
always @ (*)
	begin
	d = x & c;
	x = a | b;
end
endmodule
```
Hardware of Verilog code :
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/0a9b38a6aeaf932958f3f06b6435298cc0f233d8/PD%23Day4/IMG_6767.png">
Gtkwave:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/90b875b162a2b4374c14537fc8a9b21f6d598dee/PD%23Day4/blocking_gtk.png">

Yosys result: 
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/90b875b162a2b4374c14537fc8a9b21f6d598dee/PD%23Day4/blocking_synth.png">

GLS Simulation:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/90b875b162a2b4374c14537fc8a9b21f6d598dee/PD%23Day4/blocking_result_gtk.png">

Summary : Here this how the circuit should behave but this correct waveform is only obtained while doing netlist simulation. Here first pic show the netlist simulation which shows the proper working of the dut while the last pic shows the improper working of dut as we have used blocking statement here which causes synthesis simulation mismatch which is sorted out by GLS while providing netlist simulation.
</details>

## Day-5-Design For Testabilty(DFT)

<details>
<summary> Introduction to DFT </summary>
	
**What is Design for Testability, and why we need it?**

Today, semiconductors lie at the heart of ongoing advances across the electronics industry. The introduction of new technologies, has allowed the semiconductor industry to keep pace with increased performance-capacity demands from consumers. This has brightened the prospects for future industry growth.
However, new technologies come with new challenges. Smaller die sizes increase the probability of some errors. Errors in ICs are highly undesirable. 
In simple words, Design for testability is a design technique that makes testing a chip possible and cost-effective by adding additional circuitry to the chip.
Alternatively, Design-for-testability techniques improve the controllability and observability of internal nodes, so that embedded functions can be tested.

Now, Question arrises what is controllability and observability in design.
*Controllability*: Ability to establish aspecific signal value at each node in a circuit from setting values at the circuits inputs.
*Observability*: Ability to determine the signal value at any node in circuit by controlling the circuits input and observing its output.

**Role of DFT**
Testing of Sequential Circuits :
DFT offers a solution to the issue of testing sequential circuits. It’s kind of hard to test sequential circuits. Since there are clocks involved along with the flip-flops.
Unlike combinational circuits, we can’t determine the output of sequential circuits by merely looking into the inputs. Sequential circuits consist of finite states. The output also depends upon the state of the machine. It is difficult to control and observe the internal flip-flops externally.
Hence, the state machines cannot be tested unless they are initialized to a known value. And to initialize them, we need a specific set of features in addition to the typical circuitry. DFT enables us to add this functionality to a sequential circuit and thus allows us to test it.


**Can DFT permanently eliminate faults?**

No, faults can arise even after the chip is in consumer’s hands. A chip may misbehave anytime if it is exposed to a very high temperature or humid environment or due to aging.
You can even generate a fault on your own. A chip can’t ever be made resistant to faults; they are always bound to occur. So, what are we trying to achieve? Testing a device increases our confidence. By testing a chip, vendors try to minimize the possibility of future errors and failures.
To ensure the highest quality of chips, there is also an auxiliary process involved in the chip-design process called Verification.



**Some Terminologies**

Here are a few terminologies which we will often use in this free Design for Testability course. Don’t fret if you can’t completely understand them yet, we will be covering them in-depth in this course.

Testing: An experiment in which the system is put to work and its resulting response is analyzed to ascertain whether it behaved correctly.

Diagnosis: Process for locating the cause of misbehavior in the circuit if it happened.

Defect: Refers to a flaw in the actual hardware or electronic system.

Fault: It is a model or representation of defect for analyzing in a computer program.

Error: It is caused by a defect and happens when a fault in hardware causes line/ gate output to have a wrong value.

Failure: This occurs when a defect causes misbehavior in the circuit or functionality of a system and cannot be reversed or recovered.

Fault Coverage: Percentage of the total number of logical faults that can be tested using a given test set T.

Defect Level: Refers to the fraction of shipped parts that are defective. Or, the proportion of the faulty chip in which fault isn’t detected and has been classified as good.
where Y is the yield, means the fraction of the chips fabricated that are good.
</details>


## Day-6-Introduction to logic synthesis in DC

<details>
<summary> Introduction </summary>

*Synthesis*
-RTL to Gate level translation.
-The design is converted inta gate and connections are made betn the gates.
-INPUT to Synthesis 1. RTL 2. .lib

*Contents of .lib*
A typical Liberty file contains detailed information about the behaviour of standard cells, including :
    -Timing Information : This includes delay, transition and capacitance values associated with the standard cells. Timing information specifies how the cells behave under different input conditions.
    -Power Information : Liberty file also provides data on power consumption , including static power and dynamic power characteristics. This information is crucial for optimizing the power consumption in IC.
    -Functional Behaviour : Descriptions of the logical functionality of standard cells, such as input and output pins and logical equations and any additional attributesthat define their operation.
    -Operating Conditions : Liberty files may include information about different operating condition in terms of process , voltage and temperature under which all cells are characterized.
    






