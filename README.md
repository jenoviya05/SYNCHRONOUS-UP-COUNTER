### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: Jenoviya D
RegisterNumber: 25014196

~~~
module exp11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
	if(!rstn)
		out<=0;
	else
		out <= out+1;
end
endmodule
~~~

**RTL LOGIC UP COUNTER**
<img width="1057" height="375" alt="Screenshot 2025-12-16 222841" src="https://github.com/user-attachments/assets/b0c49955-0f54-4a53-8bf4-031f7170d77a" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1038" height="654" alt="Screenshot 2025-12-16 222852" src="https://github.com/user-attachments/assets/ce0b1c78-a66e-4a2a-81ab-87bba8436ca3" />

**TRUTH TABLE**
<img width="692" height="352" alt="Screenshot 2025-12-16 222900" src="https://github.com/user-attachments/assets/1bfaa8cc-07d7-468e-bee5-759cdead8cb5" />

**RESULTS**
Thus the Synchronous 3 bit Up counter is implemeted and verified.
