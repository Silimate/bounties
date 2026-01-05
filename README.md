# Bounties

This is a list of open-source bounties that would be useful to Silimate. Please contact akash@silimate.com or create an issue in this repo if you are interested in one of these, to align on success criteria and implementation strategy.

Completion of one of the technical bounties worth >$1000 qualifies you for a final-round interview with Silimate, if you'd like to apply for any full-time/intern position with us.

## Yosys

- [x] [Run `abc` on different modules in parallel](yosys/abc-module-parallelism.md) (implemented by [akashlevy](https://github.com/akashlevy))
- [ ] [Arithmetic optimization pass](yosys/arith-opt-pass.md) ($2000-6000)
- [x] [Make `timeest` pass work for combinational logic](yosys/timeest-comb.md) ($1000, claimed by [povik](https://github.com/povik), being reviewed/validated)

## ABC

- [x] [Retain original node associations while running optimization commands](abc/node-associations.md) (being implemented by [AdvaySingh1](https://github.com/AdvaySingh1))

## OpenSTA

- [x] [Prune CCS information from Liberty files to load them faster](opensta/liberty-ccs-pruning.md) ($1000, claimed by [vs34](https://github.com/vs34), to be paid out)
- [x] [Support for fast object collections](opensta/fast-collections.md): see https://www.intel.com/content/www/us/en/docs/programmable/683243/21-3/collection-commands.html (being implemented by [donn](https://github.com/donn))
- [x] [Support for hierarchical object search with slashes](opensta/hier-obj-search.md) ($1000, claimed by [AdvaySingh1](https://github.com/AdvaySingh1), to be paid out)

## GTKWave

- [ ] [Support for Broadway backend instead of X11/XQuartz](gtkwave/broadway-backend.md) ($1000-3000, interest from [nataliakokoromyti](https://github.com/nataliakokoromyti))
- [ ] [Support for Waveform Control Protocol (WCP)](gtkwave/wcp.md) ($1000-2000, interest from [nataliakokoromyti](https://github.com/nataliakokoromyti))
- [ ] [Support for dynamically compiling/loading an FSDB extension OR create a fast `fsdb2fst`](gtkwave/dynamic-fsdb.md) ($2000-3000)

## Nuitka

- [ ] Caching of Python -> C sources ($1000-3000)

## SV Tests

- [ ] Add [chimera](https://github.com/Silimate/chimera) tests to [sv-tests](https://github.com/chipsalliance/sv-tests) ($250)
- [ ] Add [verismith](https://github.com/Silimate/verismith) tests to [sv-tests](https://github.com/chipsalliance/sv-tests) ($250)
- [ ] Add [vloghammer](https://github.com/Silimate/vloghammer) tests to [sv-tests](https://github.com/chipsalliance/sv-tests) ($250)

## Open-source Liaison

We regularly upstream our features/bugfixes to keep our changes in sync and get feedback from maintainers.

However, we currently have a large number of changes in our forks that we would like to upstream but do not have time to do ourselves. If you are able to upstream any of these (plus whatever edits are required by the project maintainers), you will earn a small reward ($50-100/item, depending on complexity, please discuss with us; open to higher bounties depending on amount of work required).

**IMPORTANT NOTE: IF IT'S YOUR FIRST TIME UPSTREAMING AND/OR YOU ARE UNSURE ABOUT WHICH PARTS SHOULD BE UPSTREAMED, PLEASE CREATE AN ISSUE SO WE CAN DISCUSS.**

If you try to upstream one of these but it gets rejected, please contact us anyways. We may still pay out a partial bounty as a thank you (at our discretion).

### Yosys

Upstream: https://github.com/YosysHQ/yosys

Fork: https://github.com/Silimate/yosys

Compare: https://github.com/YosysHQ/yosys/compare/main...Silimate:yosys:main

- [x] BUGFIX: `undef ID` ($50, claimed by [vs34](https://github.com/vs34), to be paid out)
- [x] BUGFIX: Verific `run-test.sh` ($50, claimed by [nataliakokoromyti](https://github.com/nataliakokoromyti), to be paid out)
- [x] SMALLFIX: `ice40_wrapcarry` attribute abort fix for src attribute ($50, claimed by [nataliakokoromyti](https://github.com/nataliakokoromyti), to be paid out)
- [ ] FEATURE: New naming scheme ($100)
- [ ] FEATURE: src attribute propagation ($100)
- [ ] FEATURE: `abc -word` ($50)
- [ ] FEATURE: abc module-level parallelism ($100)
- [ ] FEATURE: abc src back-annotation, SIGABRT on failures ($100)
- [ ] FEATURE: `lut2mux -word` ($50)
- [ ] FEATURE: `lut2bmux` ($50)
- [ ] FEATURE: `splitlarge` ($50)
- [ ] FEATURE: `opt_balance_tree` ($100)
- [ ] FEATURE: `breaksop` ($50)
- [ ] FEATURE: `breakreduce` ($50)
- [ ] FEATURE: `wreduce` traversal ($100)
- [ ] FEATURE: `equiv -nocells` ($50)
- [ ] FEATURE: `debugon` ($50)
- [ ] FEATURE: `splitnets -ports_only -top_only` ($75)
- [ ] FEATURE: Backtrace ($50)
- [ ] FEATURE: `design.run_pass` ($50)
- [ ] FEATURE: RTLIL dumping/hashing ($50)
- [x] FEATURE: Verilog backend split long lines ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -optimization` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -no_split_complex_ports` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -set_ignore_translate_off` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -set_relaxed_checking` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -set_relaxed_file_ext_modes` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -set_relaxed_file_libext_modes` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -ignore_module` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [x] FEATURE: `verific -set_vhdl_default_library_path` ($50, claimed by [dhvll](https://github.com/dhvll), in review upstream)
- [ ] FEATURE: Verific mixed SV-VHDL support ($100)

### OpenSTA

Upstream: https://github.com/parallaxsw/OpenSTA

Fork: https://github.com/Silimate/OpenSTA

Compare: https://github.com/parallaxsw/OpenSTA/compare/master...Silimate:OpenSTA:main

- [ ] FEATURE: Support for hierarchical object search with slashes ($50)
- [ ] FEATURE: Input/output internal power ($100)
- [ ] FEATURE: Reporting: deduplicate by word ($100)
- [x] FEATURE: Report power as JSON ($100, claimed by [nataliakokoromyti](https://github.com/nataliakokoromyti), to be paid out)
- [ ] FEATURE: Strip escaped bus ($100)
- [ ] FEATURE: Support for Liberty generated clocks, see https://github.com/Silimate/OpenSTA/pull/28 and https://github.com/Silimate/OpenSTA/pull/30 ($100)

## Balances/Leaderboard

| Username          | In Review Balance | To Be Paid Balance | Paid Balance | Total Bounty |
|-------------------|-------------------|--------------------|--------------|--------------|
| vs34              | $0                | $1050              | $0           | $1050        |
| AdvaySingh1       | $0                | $1000              | $0           | $1000        |
| povik             | $1000             | $0                 | $0           | $1000        |
| nataliakokoromyti | $0                | $200               | $0           | $200         |
| dhvll             | $250               | $0                 | $0           | $250          |
