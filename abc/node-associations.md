# Retain original node associations while running commands

In `abc`, it is difficult to know how the final graph nodes are related to the original nodes.

Sometimes, you can relate certain nodes back using `dress` but that does not always work.

The idea of this bounty is to keep track of all the nodes that were involved in the creation of a new node.

For example, if two nodes with the same function are merged, you mark the new node as being related to those original nodes.
If that new node is again merged with another node, you mark the new node as being related to 3 original nodes. And so forth.

This tracking needs to work for all of the following `abc` commands:
- `&get -n`
- `&st`
- `&sweep`
- `&dch`
- `&nf`
- `&st`
- `&syn2`
- `&if -g -K 6`
- `&put`

The output should be some sort of map of original nodes to final nodes. Every final node must have at least one source.
