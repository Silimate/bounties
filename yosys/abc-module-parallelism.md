# ABC Module-Level Parallelism

The `abc` pass in Yosys currently works in 4 steps:
1. Prepare snippets of logic (per module) to send to `abc`
2. For each snippet, create BLIF files and scripts for `abc`
3. Run `abc` on each BLIF snippet
4. Stitch BLIF snippets back into module

We would like to parallelize step 3 using a process pool.
The `abc` pass should take an argument (something like `-procs` or `-parallelism`, etc.)
specifying how many processes should be in the pool. You can then spawn up to `N` `abc`
processes in parallel for each snippet.

## Success Criteria

Either:
- Get upstreamed to [YosysHQ/yosys](https://github.com/YosysHQ/yosys)
- Get upstreamed to [Silimate/yosys](https://github.com/Silimate/yosys)
