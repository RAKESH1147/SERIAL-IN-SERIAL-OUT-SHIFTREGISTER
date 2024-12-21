# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */
~~~
**PROGRAM**
module EXP10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:RAKESH.K.S
RegisterNumber:24006757

~~~



**RTL LOGIC FOR SISO Shift Register**
![392899729-19527a74-8d3b-4aed-989c-92f7d42b470b](https://github.com/user-attachments/assets/320c708c-594f-4832-9ab0-4097bb800c6c)

**TIMING DIGRAMS FOR SISO Shift Register**
![392899784-97a98dcf-5c48-4c6d-b700-d2bb003b1f97](https://github.com/user-attachments/assets/49032d6b-32f3-4047-a6f7-1a814ab74dd5)

**RESULTS** The 4-bit SISO (Serial-In Serial-Out) shift register was successfully implemented using Verilog in Quartus Prime. The functionality was validated using the truth table. The shift register correctly shifted the input data one bit at a time through the flip-flops on each clock pulse. The outputs q0, q1, q2, and q3 were observed to propagate the input data as expected, confirming the correct operation of the shift register.
