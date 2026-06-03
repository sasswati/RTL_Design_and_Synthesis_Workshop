#THEORY:

Design
- Actual Verilog code or set of Verilog codes
- May have 1 or more primary inputs and outputs
- read_verilog: to read design

Simulator:
- Tool used to simulate the design
- Looks for change in values of input
- Verify the synthesis
- Simulator Used: iverilog
- Output: vcd (Value Change Dump) file
- To view waveform output: gtkwave

TestBench:
- Setup to apply stimulus (test_vectors) to design to check its functionality
- Does not have primary inputs or outputs
- Same for netlist and RTL

RTL Design:
- Behavioural representation of required specification

Synthesis:
- RTL to Gate level translation
- Design is converted into gates
- Output file is called netlist file

netlist file:
- Representation of design in the form of cells present in the .lib
- write_verilog: to write netlist file

.lib:
- Collection of logical modules
- read_liberty: to read .lib

uut - Unit Under Test
#abc - abc nanoseconds
transistor width directly proportional to speed directly proportional to area and power needed

Synthesizer:
- Tool used for converting RTL to netlist
- Syntesizer Used: Yosys

---

#LAB 1: 
- Setting up and understanding the layout

---

#LAB 2:
```text
- Observations: sel = 0, y = i0
              : sel = 1, y = i1
```

  <img width="1470" height="956" alt="Output of tb_good_mux.v" src="https://github.com/user-attachments/assets/1d72ce00-1242-4bd4-b68b-63cbef8e5ac2" />

---

#LAB 3:

- Output:

```text
ABC RESULTS:   sky130_fd_sc_hd__mux2_1 cells:        1
ABC RESULTS:        internal signals:        0
ABC RESULTS:           input signals:        3
ABC RESULTS:          output signals:        1
```

<img width="1470" height="956" alt="Graphical Representation of good_mux.v" src="https://github.com/user-attachments/assets/612039ea-4e20-43b9-85da-87245f88ac13" />





