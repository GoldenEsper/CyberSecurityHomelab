## What is it?
Sysmon is a part of the "Microsoft [Sysinterals](Studied%20Ideas%20and%20Concepts/3.%20LSASS%20Investigation/Sysinterals.md) suite". It provides deep telemetry on how events occur such as command-line arguments, file hashes, and network connection associated with specific processes.

## What does it track?
- Process tracking (who and how) - Shows what process started what
- Network activity (the where) - Tells exactly which process ID opened connection to specific IP address and port. Can also log DNS lookups
- File and registry integrity (persistence) - Tracks the creation of keys and when they were modified.