# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

1.Increment count on each positive edge of the clock.

2.Reset count to zero when it reaches 15.

3.Generate clock signal (clk).

4.Instantiate the RippleCounter module.

5.Conduct functional testing by displaying the count at each clock cycle for 16 cycles.

**PROGRAM**
## Developed by:tharun.b
## RegisterNumber: 212224240171
```
module ripple_counter(
     input wire clk,
	  input wire rst,
	  output reg[3:0] count
	  );
	  
always @(posedge clk or posedge rst)
begin
     if(rst)
	     count <= 4'b0000;
	  else 
	     count <= count + 1;
end 
endmodule
```
**RTL LOGIC FOR 4 Bit Ripple Counter**

![Screenshot 2025-05-21 101946](https://github.com/user-attachments/assets/37cfc9c2-6186-474f-a0d5-c589e6aacaaf)


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![Screenshot 2025-05-21 102034](https://github.com/user-attachments/assets/57ba061b-04d0-4675-a49d-aa5b825845c0)

**RESULTS**
Thus implementing 4 Bit Ripple Counter using Verilog and validating their functionality using their functional tables is done successfully.
