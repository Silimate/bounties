# Arithmetic Optimization Pass

How to handle arithmetic tree balancing properly:

1. (Peepopt) Convert subtractors to adders and negations: a - b ==> a + (-b)
2. (Peepopt) Expand negations backward through adders: -(a + b) ==> (-a) + (-b)
3. (Pass) Balance adder tree (opt_balance_tree, already implemented)
4. (Peepopt) Rebuild subtractors and negations: a + (-b) ==> a - b and (-a) + (-b) ==> -(a + b)

Examples:
```
Initial expression: a + b + c + d + e + f + g + h
Step 1 and 2: no change
Step 3: ((a + b) + (c + d)) + ((e + f) + (g + h))
Step 4: no change

Initial expression: a - b + c - d + e - f + g - h
Step 1: a + (-b) + c + (-d) + e + (-f) + g + (-h)
Step 2: no change
Step 3: ((a + (-b)) + (c + (-d))) + ((e + (-f)) + (g + (-h)))
Step 4: ((a - b) + (c - d)) + ((e - f) + (g - h))

Initial expression: a - b - c - d - e - f - g - h
Step 1: a + (-b) + (-c) + (-d) + (-e) + (-f) + (-g) + (-h)
Step 2: no change
Step 3: ((a + (-b)) + ((-c) + (-d))) + (((-e) + (-f)) + ((-g) + (-h)))
Step 4.1: ((a - b) + -(c + d)) + (-(e + f) + (-(g + h)))
Step 4.2: ((a - b) - (c + d)) + (-((e + f) + (g + h)))
Step 4.3: ((a - b) - (c + d)) - ((e + f) + (g + h))

Initial expression: a + b - c + d - e + f - g + h
Step 1: a + b + (-c) + d + (-e) + f + (-g) + h
Step 2: no change
Step 3: ((a + b) + ((-c) + d)) + (((-e) + f) + ((-g) + h))
Step 4: ((a + b) + (d - c)) + ((f - e) + (h - g))

Initial expression: a + b - c - d + e + f - g - h
Step 1: a + b + (-c) + (-d) + e + f + (-g) + (-h)
Step 2: no change
Step 3: ((a + b) + ((-c) + (-d))) + ((e + f) + ((-g) + (-h)))
Step 4.1: ((a + b) + (-(c + d))) + ((e + f) + (-(g + h)))
Step 4.2: ((a + b) - (c + d)) + ((e + f) - (g + h))
```

TODO: we need some examples that exercise step 2...

Test RTL for cases above, logic depth should be 3 adders:

```
module arith_chain (
  input [31:0] a,
  input [31:0] b,
  input [31:0] c,
  input [31:0] d,
  input [31:0] e,
  input [31:0] f,
  input [31:0] g,
  input [31:0] h,
  output [40:0] y,
  output [40:0] y1,
  output [40:0] y2,
  output [40:0] y3,
  output [40:0] y4
);

  assign y  = a + b + c + d + e + f + g + h;
  assign y1 = a - b + c - d + e - f + g - h;
  assign y2 = a + b - c + d - e + f - g + h;
  assign y3 = a - b - c - d - e - f - g - h;
  assign y4 = a + b - c - d + e + f - g - h;

endmodule
```

## Success Criteria

Either:
- Get upstreamed to [YosysHQ/yosys](https://github.com/YosysHQ/yosys)
- Get upstreamed to [Silimate/yosys](https://github.com/Silimate/yosys)
