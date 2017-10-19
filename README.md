# Tools for "Another Flip in the Wall"

This Rowhammer tool tests whether your system is susceptible for one-location hammering bit flips.

See https://github.com/IAIK/rowhammerjs/tree/master/native for a double-sided hammering test (which is more likely to find bit flips on your system).

Also see our paper "Another Flip in the Wall of Rowhammer Defenses": https://arxiv.org/abs/1710.00551

## Build and Run

```
make
./rowhammer
```

## Warnings

**Warning #1:** We are providing this code as-is.  You are responsible
for protecting yourself, your property and data, and others from any
risks caused by this code.  This code may cause unexpected and
undesirable behavior to occur on your machine.  This code may not
detect the vulnerability on your machine.

Be careful not to run this test on machines that contain important
data.  On machines that are susceptible to the rowhammer problem, this
test could cause bit flips that crash the machine, or worse, cause bit
flips in data that gets written back to disc.

**Warning #2:** If you find that a computer is susceptible to the
rowhammer problem, you may want to avoid using it as a multi-user
system.  Bit flips caused by row hammering breach the CPU's memory
protection.  On a machine that is susceptible to the rowhammer
problem, one process can corrupt pages used by other processes or by
the kernel.

