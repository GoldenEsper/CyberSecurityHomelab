## What is it?
Extended Accumulator Register is a general-purpose register in 32bit architecture. Registers are small fast storage locations built DIRECTLY into the CPU. 
## How does it operate?
When a programmer wants to trigger a [System call](System%20calls.md) the CPU needs to know which service to perform. The standard for windows is that th identifier for the service must be placed into the EAX register before the [System call](System%20calls.md) instruction is executed. 