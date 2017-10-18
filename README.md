# Dexm fork of Jerryscript + Sandbox + IPC
## Info
Dexm-vm is a Linux only VM that runs Dexm smart contracts and web requests.

## Sandbox
The sandbox is implemented using libseccomp and prohibiting all syscalls other than the default ones and POSIX mqueues

## IPC
Dexm-vm acts as a worker for dexmd and communicates with it using POSIX mqueues. The worker will recive a work package and send the various events happening in the script and the result to the main demon.
