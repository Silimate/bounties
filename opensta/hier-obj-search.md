# OpenSTA Hierarchical Object Search

One major issue with OpenSTA is that it does not support hierarchical object search with slashes.

Suppose we have the following instance hierarchy:

```
top
├─ inst1
├─ inst2
|  ├─ a_leaf1
|  ├─ a_leaf2
|  ├─ a_leaf3
|  └─ a_leaf4
└─ inst3
   ├─ a_leaf1
   ├─ a_leaf2
   ├─ a_leaf3
   ├─ a_leaf4
   ├─ inst4
   │  ├─ a_leaf5
   │  ├─ a_leaf6
   │  ├─ a_leaf7
   │  └─ a_leaf8
   └─ inst5
      ├─ leaf9   
      ├─ leaf10
      ├─ leaf11
      ├─ leaf12
      ├─ leaf13
      ├─ leaf14
      └─ leaf15
```

Let us suppose I want to get all instances in any hierarchy below `inst3` with name `a_leaf*`. This would include `inst3/a_leaf[1-4]` and `inst3/inst4/a_leaf[5-8]`. The SDC command I would use should either be:

```
get_cells inst3/a_leaf**
```

OR

```
get_cells -hier inst3/a_leaf*
```

Neither of these work in OpenSTA at the moment. The goal of this would be to demonstrate that these work. And of course the runtime should be reasonable.

## Success Criteria

Simple test case and feature addition to OpenSTA. Must be upstreamed to either:
- https://github.com/parallaxsw/OpenSTA
- https://github.com/Silimate/OpenSTA

Runtime should scale linearly with design size.


