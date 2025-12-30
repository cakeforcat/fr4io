# FR4io
This is an attempt at creating a modular set of tiles that can create movement systems from factorio in real life.
## Proposed features
 - smart, addressable tiles
 - fully reconfigurable
 - hot-swappable
 - extendable (arms, splitters, combiners)
 - magnetically actuated
 - low-cost-ish

## magnetic actuation
each tile will consist of 5 PCB coils that can be thought of as a very crude linear motor. Payload to be moved are purely for aesthetics and will be as light as possible.
The tile will be able to sense the presense of a payload by measuring the current on each coil through a shunt resistor.

## network
tiles connect to each other through a simple UART link. Each powered on tile announces it's presence on all 4 edges abd nearby tiles respond with acknowledges. The entire graph is built and maintained by the central controller. The firmware on each tile is meant to be as minimal as possible to allow for OTW (Over the Wire) updates. All higher level functions are to be implemented on the controller. Each tile is addressable.

## EMF
will hopefully be presented at EMF2026? will depend on tickets and if we actually make it :D

