# **LAB 4**

- P(Process): Variations due to fabrication
- V(Voltage): Variations due to voltage
- T(Temp): Variations due to temperature
- tt: typical
- 025c: temperature

<img width="1470" height="956" alt=".lib contents" src="https://github.com/user-attachments/assets/85b27ac9-e72b-4285-a9ba-462c2b2c2104" />

---

<br>

# **LAB 5**
- vcd file used: multiple_modules.v

The below presents the hierarchical design.
<img width="1470" height="956" alt="Graphical Representation of Hierarchical multiple_modules.v" src="https://github.com/user-attachments/assets/68ef210d-7e6a-4fba-a805-7e779ca427fd" />

<br>

## Netlist of multiple_modules_hier.v
```text
module multiple_modules(a, b, c, y);
  input a;
  input b;
  input c;
  wire net1;
  output y;
  sub_module1 u1 (
    .a(a),
    .b(b),
    .y(net1)
  );
  sub_module2 u2 (
    .a(net1),
    .b(c),
    .y(y)
  );
endmodule

module sub_module1(a, b, y);
  wire _0_;
  wire _1_;
  wire _2_;
  input a;
  input b;
  output y;
  sky130_fd_sc_hd__and2_0 _3_ (
    .A(_1_),
    .B(_0_),
    .X(_2_)
  );
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
  sky130_fd_sc_hd__or2_0 _3_ (
    .A(_1_),
    .B(_0_),
    .X(_2_)
  );
  assign _1_ = b;
  assign _0_ = a;
  assign y = _2_;
endmodule
```

<br>

The below represents flat design.
<img width="1470" height="956" alt="Graphical Representation of Flat multiple_modules.v" src="https://github.com/user-attachments/assets/88f5c29b-b856-4ec5-8a8c-db5ff4a8fd3d" />


## Netlist of multiple_modules_flat.v

```text
module multiple_modules(a, b, c, y);
  wire _0_;
  wire _1_;
  wire _2_;
  wire _3_;
  wire _4_;
  wire _5_;
  input a;
  input b;
  input c;
  wire net1;
  wire \u1.a ;
  wire \u1.b ;
  wire \u1.y ;
  wire \u2.a ;
  wire \u2.b ;
  wire \u2.y ;
  output y;
  sky130_fd_sc_hd__and2_0 _6_ (
    .A(_1_),
    .B(_0_),
    .X(_2_)
  );
  sky130_fd_sc_hd__or2_0 _7_ (
    .A(_4_),
    .B(_3_),
    .X(_5_)
  );
  assign \u1.a  = a;
  assign \u1.b  = b;
  assign net1 = \u1.y ;
  assign _1_ = \u1.b ;
  assign _0_ = \u1.a ;
  assign \u1.y  = _2_;
  assign \u2.a  = net1;
  assign \u2.b  = c;
  assign y = \u2.y ;
  assign _4_ = \u2.b ;
  assign _3_ = \u2.a ;
  assign \u2.y  = _5_;
endmodule
```
