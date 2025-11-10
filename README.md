# Bounties

This is a list of open-source bounties that would be useful to Silimate. Please contact akash@silimate.com or create an issue in this repo if you are interested in one of these, to align on success criteria and implementation strategy.

Completion of one of the technical bounties worth >$1000 qualifies you for a final-round interview with Silimate, if you'd like to apply for any full-time/intern position with us.

## Yosys

- [x] [Run `abc` on different modules in parallel](yosys/abc-module-parallelism.md) ($1000-3000, implemented by [akashlevy](https://github.com/akashlevy))
- [ ] [Arithmetic optimization pass](yosys/arith-opt-pass.md) ($2000-6000)
- [x] [Make `timeest` pass work for combinational logic](yosys/timeest-comb.md) ($1000, claimed by [povik](https://github.com/povik))

## ABC

- [ ] [Retain original node associations while running optimization commands](abc/node-associations.md) ($5000-10000)

## OpenSTA

- [ ] [Prune CCS information from Liberty files to load them faster](opensta/liberty-ccs-pruning.md) ($1000-2000)
- [ ] [Support for fast object collections](opensta/fast-collections.md): see https://www.intel.com/content/www/us/en/docs/programmable/683243/21-3/collection-commands.html ($1000-3000)
- [ ] [Support for hierarchical object search with slashes](opensta/hier-obj-search.md) ($1000-2000)

## GTKWave

- [ ] [Support for Broadway backend instead of X11/XQuartz](gtkwave/broadway-backend.md) ($1000-3000)
- [ ] [Support for Waveform Control Protocol (WCP)](gtkwave/wcp.md) ($1000-2000)
- [ ] [Support for dynamically compiling/loading an FSDB extension OR create a fast `fsdb2fst`](gtkwave/dynamic-fsdb.md) ($2000-3000)

## Nuitka

- [ ] Caching of Python -> C sources ($1000-3000)

## SV Tests

- [ ] Add [chimera](https://github.com/Silimate/chimera) tests to [sv-tests](https://github.com/chipsalliance/sv-tests) ($250)
- [ ] Add [verismith](https://github.com/Silimate/verismith) tests to [sv-tests](https://github.com/chipsalliance/sv-tests) ($250)
- [ ] Add [vloghammer](https://github.com/Silimate/vloghammer) tests to [sv-tests](https://github.com/chipsalliance/sv-tests) ($250)

## Open-source Liaison

We regularly upstream our features/bugfixes to keep our changes in sync and get feedback from maintainers.

However, we currently have a large number of changes in our forks that we would like to upstream but do not have time to do ourselves. If you are able to upstream any of these (plus whatever edits are required by the project maintainers), you will earn a small reward ($50-100/item, depending on complexity, please discuss with us).

If you try to upstream one of these but it gets rejected, please contact us anyways. We may still pay out a partial bounty as a thank you (at our discretion).

### Yosys

Upstream: https://github.com/YosysHQ/yosys

Fork: https://github.com/Silimate/yosys

Compare: https://github.com/YosysHQ/yosys/compare/main...Silimate:yosys:main

- [x] BUGFIX: `undef ID` ($50, claimed by [vs34](https://github.com/vs34))
- [ ] BUGFIX: Verific run-test.sh
- [x] BUGFIX: Various logger_cmd_error.sh test (fixed upstream already!)
- [ ] BUGFIX: Xilinx abc9_dff test
- [ ] BUGFIX: fstdata include
- [ ] SMALLFIX: ice40_wrapcarry attribute abort fix (for src attribute...)
- [ ] ADJUST: read -vlog2k  -->  read_verilog
- [ ] ADJUST: Create pool from set in `hashlib`
- [ ] FEATURE: New naming scheme
- [ ] FEATURE: src attribute propagation
- [ ] FEATURE: `abc -word`
- [ ] FEATURE: abc module-level parallelism
- [ ] FEATURE: abc src back-annotation, SIGABRT on failures
- [ ] FEATURE: `lut2mux -word`
- [ ] FEATURE: `lut2bmux`
- [ ] FEATURE: `splitlarge`
- [ ] FEATURE: `opt_balance_tree`
- [ ] FEATURE: `breaksop`
- [ ] FEATURE: `breakreduce`
- [ ] FEATURE: `wreduce` traversal
- [ ] FEATURE: `equiv -nocells`
- [ ] FEATURE: `debugon`
- [ ] FEATURE: `splitnets -ports_only -top_only`
- [ ] FEATURE: Backtrace
- [ ] FEATURE: `design.run_pass`
- [ ] FEATURE: RTLIL dumping/hashing
- [ ] FEATURE: Verilog backend split long lines
- [ ] FEATURE: `verific -optimization`
- [ ] FEATURE: `verific -no_split_complex_ports`
- [ ] FEATURE: `verific -set_ignore_translate_off`
- [ ] FEATURE: `verific -set_relaxed_checking`
- [ ] FEATURE: `verific -set_relaxed_file_ext_modes`
- [ ] FEATURE: `verific -set_relaxed_file_libext_modes`
- [ ] FEATURE: `verific -ignore_module`
- [ ] FEATURE: `verific -set_vhdl_default_library_path`
- [ ] FEATURE: Verific mixed SV-VHDL support

### OpenSTA

Upstream: https://github.com/parallaxsw/OpenSTA

Fork: https://github.com/Silimate/OpenSTA

Compare: https://github.com/parallaxsw/OpenSTA/compare/master...Silimate:OpenSTA:main

- [ ] FEATURE: Input/output internal power
- [ ] FEATURE: Reporting: deduplicate by word
- [ ] FEATURE: Report power as JSON
- [ ] FEATURE: Strip escaped bus
