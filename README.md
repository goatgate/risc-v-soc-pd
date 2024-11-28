# risc-v-soc-pd
pd implementation of mixed signal risc v soc
<details open>
<summary>pre synthesis modelling of risc v soc</summary>
<br>
### modeling VSDBabySoC

- **Input Signals**: Initial input signals are fed into the **VSDBabySoC** module.  
- **Clock Generation**: A **PLL (Phase-Locked Loop)** generates the appropriate clock signal (**CLK**) for the circuit.  
- **Instruction Execution**: The **rvmyth** core executes instructions driven by the clock signal and produces certain values.  
- **Output Signal Generation**: The generated values are used by the **DAC core** to produce the final output signal, named **OUT**.  
- **Design Components**:
  - Three IP cores.
  - A wrapper module acting as the SoC.
  - A testbench module for verification.
  - reference design used: https://github.com/manili/VSDBabySoC 
simulation wave form dac as a part of  the soc
![image](https://github.com/user-attachments/assets/ba3ee7cd-5365-402a-905b-6cf4b77c8305)
### Signals in the Picture:

- **CLK**:  
  - Input clock signal for the **RVMYTH** core.  
  - Originates from the **PLL**.  

- **D[9:0]**:  
  - 10-bit output wire [9:0] of the **RVMYTH** core.  

- **OUT (DAC)**:  
  - A `real` data type net capable of simulating analog values.  
  - Output signal of the **DAC module**.  
  - Originates from the **DAC**.  

</details>
