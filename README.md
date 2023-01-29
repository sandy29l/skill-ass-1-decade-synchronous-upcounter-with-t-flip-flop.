# skill-ass-1-decade-synchronous-upcounter-with-t-flip-flop.
# TITLE:
DECADE SYNCHRONOUS UPCOUNTER WITH T FLIP FLOP.
# AIM:

To implement the given function decade synchronous upcounter with t flip flop and to verify its operation in Quartus using Verilog programming.


# Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

# INTRODUCTION:

Synchronous Counters are so called because the clock input of all the individual flip-flops within the counter are all clocked together at the same time by the same clock signal
Then the flip - flop acts as a Toggle switch. The next output state is changed with the complement of the present state output. This process is known as Toggling
The T flip-flop is designed bypassing the AND gate's output as input to the NOR gate of the SR flip-flop. The inputs of the "AND" gates, the present output state Q, and its complement Q' are sent back to each AND gate.

The toggle input is passed to the AND gates as input. These gates are connected to the Clock (CLK) signal. In the T flip-flop, a pulse train of little triggers is passed as the toggle input, which changes the flip flop's output state

# TRUTH TABLE

![TRUTH TABLE](https://user-images.githubusercontent.com/123359969/215315342-18abdfda-0cbd-4241-b071-db2c9c9b0fc1.png)

the above table is the truth table for decade synchronous upcounder using t flip flop.

# PROGRAM
```
module skillass(clk,reset,up_down,load,data,count);
  //define input and output ports
  input clk,reset,load,up_down;
  input [3:0] data;
  output reg [3:0] count;
  //always block will be executed at each and every positive edge of the clock
  always@(posedge clk) 
  begin
    if(reset)    //Set Counter to Zero
      count <= 0;
    else if(load)    //load the counter with data value
      count <= data;
    else if(up_down)        //count up
      count <= count + 1;
    else            //count down
      count <= count - 1;
  end
endmodule
```
# LOGIC DIAGRAM

![de skill ass](https://user-images.githubusercontent.com/123359969/215315098-6562691c-a57a-4d4a-8490-43ade27f7cc7.png)

# EXPLANATION

To design a synchronous up counter, first we need to know what number of flip flops are required. we can find out by considering a number of bits mentioned in the question. So, in this, we required to make 4 bit counter so the number of flip flops required is 4 [2n where n is a number of bits].
After that, we need to construct a state table with excitation table.
Note: To construct excitation table from state table you should know the excitation table of respective flip flop, in this case, it is T flip flop.

# RESULT

Thus the implementaion of decade synchronous up-counter with T flip flop using Verilog is obtained.
