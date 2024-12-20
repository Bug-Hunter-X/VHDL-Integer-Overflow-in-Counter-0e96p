# VHDL Integer Overflow Bug

This repository demonstrates an uncommon error in VHDL: integer overflow in a counter.  The `counter.vhdl` file contains a simple counter that increments on each rising clock edge. However, it uses an `integer` type with a limited range (0 to 15). When the counter reaches its maximum value (15), it wraps around to 0 instead of stopping or generating an error.

The `counter_fixed.vhdl` file provides a solution using the `unsigned` type and checking for overflow.

## How to reproduce

1.  Synthesize and simulate `counter.vhdl`.
2.  Observe that the counter wraps around from 15 to 0.
3.  Synthesize and simulate `counter_fixed.vhdl` to see the corrected behavior.

## Solution

The solution involves using an `unsigned` type instead of an `integer`, providing a more robust solution and preventing unexpected behavior.