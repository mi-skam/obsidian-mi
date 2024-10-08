---
created: 2024-03-20
modified: 2024-09-03T18:29:24+02:00
---

## 6510 (CPU)

| Name | Purpose         | Description                           |
| ---- | --------------- | ------------------------------------- |
| A    | Accumulator     | Handles arithmetic and logic          |
| X, Y |                 | General Purpose and indexing          |
| P    |                 | Processor status flags and operations |
| PC   | Program counter | Next instructions to be run.          |

The 6510 reads instructions and any required data from the memory location in the **PC**, processes the data, writes the result back to memory and increments the **PC**

## VIC-II (Graphics)

There is a **bitmap** mode with 300x200 pixel resolution, but it's very restrictive and slow.

**Character** mode. 40x25 rows of characters.
	*multicolor*: 4 colors, 4 double width x 8 pixels
	*hires*: 2 colors, 8x8 pixels

The **VIC-II** is controlled by setting values in *screen* and *color* memory and *memory mapped registers*

It can only access 16k at one time.

## SID (Sound)

**SID** can play **3** voices simultaneously. Each of them can be of Triangle, Sawtooth, Pulse and Noise
![[Pasted image 20240320183644.png]]
You can tune them by the *ADSR* envelope:
- Attack
- Decay
- Sustain
- Release
![[Pasted image 20240320183652.png]]
The SID is also controlled by memory mapped registers.

## Memory

The program counter (PC) is 16bit long. It's used to address memory locations.
These are are arranged into *sections* (as the memory map shows)

You can switch off *KERNAL* and *BASIC* sections, if not needed.

![[Pasted image 20240320184008.png]]
## Assembler

lda - load the accumulator
sta - store the accumulator

$ - prefix for hexadecimal values
% - prefix for binary numbers
\# - indicates numeric values (instead of memory locations)
; - starts a comment

```asm
lda #2    ; decimal 2 (value) -> A
sta $0400 ; A -> hex 400 (address)
```
loads the decimal value 2 into register A and stores it into the address 0x0400.

```asm
lda $0400 ; 400 hex (address) -> A
sta $0401 ; A -> 401 hex (address)
```
Loads the value of memory adress 0x0400 into register A and stores the same value into 0x0401

You can't copy a value from one memory address to another, you have to load them into one of the registers first.