# An step by step guide with awnsers to fix "SIMPEL" ram problems. (Fix & Solution) 3200Mhz ram, stuck at 2133mhz, 3000mhz. 

I TAKE NO RESPONSEBELITY OR LIABILITY FOR ANY HARDWARE OR OTHER DAMAGES. TRY AT YOUR OWN RISK
=

This all assume the following:
=
- The motherboard supports and CPU can supports the ram speed
- The BIOS is updated and Supports the ram and speed


TLDR;
=

- 0: Turn on XMP, DOCP or EOCP
- 1: Check the ram slot
- 2: Tinker with SOC voltage (1.0V-1.1V)
- 3: Tinker with DRAM voltage (1.2V-1.5V)
- 4: If this dosent work check for BIOS updates


Step 0:
=
Turn on XMP, DOCP or EOCP

More info:
https://www.cgdirector.com/xmp-eocp-docp/



Step 1:
=
(If the ram is dual-channel)
- Make sure the ram is in slot A2(DIMMA2) and B2(DIMMB2)

(A1 is the closest to the CPU)
- from the left to the right: **|A1|A2|B1|B2|**

**Explanation:**
- A1 (slot 1) and B1 (slot 3) are typically reserved for a single channel of the same type.
- A2 (slot 2) and B2 (slot 4) are considered to be dual-channel RAM slots.

More info and diffrent ram configurations:
https://techjury.net/blog/what-slots-to-put-ram-in/

==========================================================================================



Step 3:
=

Tinker with DRAM voltage (1.2V-1.5V)
- BIOS -> ADVANCED -> DRAM Voltage
- Change the voltage up a bit assuming it's below 1.4
- Incerments of 0.025 or 0.050 volt (worked well for me, before fine turning)




Very specefic exampel by 

CompuTronix:
Intel has two specifications for DRAM on 14 and 22 nanometer CPUs; 1.2 for LV and 1.35.
As per Intel's Datasheets, both specifications indicate +/-5%,
which means that with respect to the on-die Integrated Memory Controller (IMC),
maximum DRAM voltage is:
1.35 voltage * 1.05(+/-5%) = 1.4175
https://forums.tomshardware.com/threads/3200mhz-at-1-5v-safe.3472270/
