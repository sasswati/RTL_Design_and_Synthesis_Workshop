Design
- Actual Verilog code or set of Verilog codes
- May have 1 or more primary inputs and outputs

Simulator:
- Tool used to simulate the design
- Looks for change in values of input
- Simulator Used: iverilog
- Output: vcd (Value Change Dump) file
- To view waveform output: gtkwave

TestBench
- Setup to apply stimulus (test_vectors) to design to check its functionality
- Does not have primary inputs or outputs

LAB 1:
Observations: sel = 0, y = i0
            : sel = 1, y = i1

  <img width="1470" height="956" alt="Output of tb_good_mux.v" src="https://github.com/user-attachments/assets/1d72ce00-1242-4bd4-b68b-63cbef8e5ac2" />


