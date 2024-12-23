# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

Go to quartus software.

Set new environment.

Type the code to implement SR flipflop using verilog and validating their functionality using their functional tables.

Run the program.

Give inputs in the waveform table.

Run the program.
/* write all the steps invloved */

**PROGRAM**
```
module exp7(j, k, clk, q, qbar);
    input j, k, clk;
    output reg q, qbar;

    always @(posedge clk) begin
        case ({j, k})
            2'b00: q <= q;            // No change
            2'b01: q <= 1'b0;         // Reset
            2'b10: q <= 1'b1;         // Set
            2'b11: q <= ~q;           // Toggle
        endcase
        qbar <= ~q;                   // Complement of q
    end
endmodule
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: AGASH S RegisterNumber: 24900273 DATE: 09/11/2024
*/

**RTL LOGIC FOR FLIPFLOPS**
![exp7](https://github.com/user-attachments/assets/177f8726-8542-412b-ab3b-ae30df684b6b)

**TIMING DIGRAMS FOR FLIP FLOPS**
![exp7-2](https://github.com/user-attachments/assets/f872d5f4-cfb6-4f80-ba8d-bbee0dbf9381)

**RESULTS**

Thus the JK flipflop using verilog and validating their functionality using their
 functional tables are verified.
