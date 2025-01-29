# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an integer counter that overflows without proper bounds checking.  The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

**Bug:** The original counter increments indefinitely, exceeding the defined range (0 to 15). This leads to unpredictable results.

**Solution:** The solution adds a check to ensure the counter doesn't exceed the maximum value, preventing the overflow.

## How to Reproduce

1.  Simulate `buggy_counter.vhdl` using a VHDL simulator (like ModelSim or GHDL).
2.  Observe the counter's behavior after it reaches 15. You'll see it wraps around or exhibits other unexpected behavior.
3.  Simulate `fixed_counter.vhdl` to see the corrected functionality.

## Learning Points

- Always check for potential integer overflow in counters and other numerical operations in VHDL.
- Using `unsigned` or `signed` types for counters often provides implicit overflow handling (though wrapping still occurs).