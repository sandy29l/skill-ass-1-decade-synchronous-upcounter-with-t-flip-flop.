# skill-ass-1-decade-synchronous-upcounter-with-t-flip-flop.
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
