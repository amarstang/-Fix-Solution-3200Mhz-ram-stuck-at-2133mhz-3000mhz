# (Fix & Solution) 3200Mhz ram, stuck at 2133mhz, 3000mhz. 
## An step by step guide with awnsers to fix "SIMPEL" ram problems.
### I TAKE NO RESPONSEBELITY OR LIABILITY FOR ANY HARDWARE OR OTHER DAMAGES. TRY AT YOUR OWN RISK

All of this assume the following:
=
- The motherboard supports and CPU can supports the ram speed
- The BIOS is updated and Supports the ram and speed


TLDR;
=

- 0: Turn on XMP, DOCP or EOCP
- 1: Check the ram slot, Dual-channel ram in A2 and B2. **|A1|A2|B1|B2|**
- 2: Tinker with SOC voltage (1.0V-1.1V)
- 3: Tinker with DRAM voltage (1.2V-1.5V)
- 4: Check for BIOS updates

Step 0 Turn on XMP, DOCP or EOCP:
=
Turn on XMP (Intel CPU), DOCP (AMD CPU) or EOCP (AMD CPU)

For an picture guide Google: 
- turn on *XMP,DOCP or EOCP*, *the producer ASUS, MSI...*

Exampel
- "Turn on DOCP ASUS"

More info:
https://www.cgdirector.com/xmp-eocp-docp/



Step 1 Check the ram slot:
=
(If the ram is dual-channel (2 ram sticks))
- Make sure the ram is in slot A2(DIMMA2) and B2(DIMMB2)

(A1 is the closest to the CPU)
- from the left to the right: **|A1|A2|B1|B2|**

**Explanation:**
- A1 (slot 1) and B1 (slot 3) are typically reserved for a single channel of the same type.
- A2 (slot 2) and B2 (slot 4) are considered to be dual-channel RAM slots.

More info and diffrent ram configurations:
https://techjury.net/blog/what-slots-to-put-ram-in/


Step 2 Tinker with SOC voltage:
=

Tinker with SOC voltage (1.0V-1.1V) *(can go higere than 1.1V on some ram)*
- BIOS -> ADVANCED -> SOC
- Change the voltage up a bit assuming it's below 1.1
- Incerments of 0.010 or 0.025 volt (worked well for me, before fine tuning)


Step 3 Tinker with DRAM voltage: 
=

Tinker with DRAM voltage (1.2V-1.5V) *(can go higere than 1.5V on some ram)*
- BIOS -> ADVANCED -> DRAM Voltage
- Change the voltage up a bit assuming it's below 1.4
- Incerments of 0.025 or 0.050 volt (worked well for me, before fine tuning)

Very specefic exampel by 

CompuTronix:
Intel has two specifications for DRAM on 14 and 22 nanometer CPUs; 1.2 for LV and 1.35.
As per Intel's Datasheets, both specifications indicate +/-5%,
which means that with respect to the on-die Integrated Memory Controller (IMC),
maximum DRAM voltage is:
1.35 voltage * 1.05(+/-5%) = 1.4175
https://forums.tomshardware.com/threads/3200mhz-at-1-5v-safe.3472270/


Step 4 check for BIOS updates:
=
**Assuming "All of this assume the following" was skiped**

Open System Information, look at:
- BaseBoard Product *Your motherboard*

In System Information also look at:
- BIOS Version/Date *Name, Value, Date*

Google your "*motherboard name* Bios update" look at the manufactiors BIOS updates,
compare the latest non-beta (stable), if it's newer, you can choose to download and flash it (recommend).


One of many guides on how to flash your BIOS
- https://www.youtube.com/watch?v=dUCWRqOdLUw


Step 5 Fxxx Fxxx Fxxx...:
=
If you get to this step, I'm truly sorry, as of right now the only help left is google.
- You might consider returning the ram
