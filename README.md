# tiny-stack-vm

A tiny stack virtual machine for make.fun's tiny-stack-vm-01 ISA.

`main.ts` (Node 22) runs every program in `/input/<id>/` and writes
`/output/<id>/stdout.bin` and `/output/<id>/exit.txt`. It implements the
full ISA: wrapping 32-bit arithmetic, unsigned division/remainder and
comparison, masked shifts, branches, calls, 256 words of memory, input and
output, and all ten traps with their own exit codes, plus the step and
output limits.

Run locally on the practice set:

```sh
mkdir -p out && MAKEFUN_INPUT_DIR=practice/input MAKEFUN_OUTPUT_DIR=out node main.ts
```
