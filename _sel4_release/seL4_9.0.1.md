---
version: 9.0.1
title: seL4 9.0.1
---

# seL4 Version 9.0.1 Release
 Announcing the release of `seL4 9.0.1` with the following changes:

9.0.1 2018-04-18: BINARY COMPATIBLE

## Changes
 * On 64-bit architectures, the `label` field of `seL4_MessageInfo` is now 52 bits wide. User-level programs
   which use any of the following functions may break, if the program relies on these functions to mask the
   `label` field to the previous width of 20 bits.
     - `seL4_MessageInfo_new`
     - `seL4_MessageInfo_get_label`
     - `seL4_MessageInfo_set_label`
 * Initial prototype RISC-V architecture port. This port currently only supports running in 64-bit mode without FPU or
   or multicore support on the Spike simulation platform. There is *no verification* for this platform.

## Upgrade Notes
---


# Full changelog
 Refer to the git log in
<https://github.com/seL4/seL4> using `git log 9.0.0..9.0.1`

# More details
 See the
[9.0.1 manual](http://sel4.systems/Info/Docs/seL4-manual-9.0.1.pdf) included in the release or ask on the mailing list!