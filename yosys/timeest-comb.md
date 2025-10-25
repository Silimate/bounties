# Combinational `timeest` Pass

The `timeest` pass determines the maximum logic depth of a given circuit. However, it does not work for combinational logic, as it requires a clock to identify startpoint/endpoint flops.

The goal is to have `timeest` estimate the maximum logic depth of all paths, including both combinational/sequential ones.

## Success Criteria

Either:
- Get upstreamed to [YosysHQ/yosys](https://github.com/YosysHQ/yosys)
- Get upstreamed to [Silimate/yosys](https://github.com/Silimate/yosys)
