# Sonic Chaos for the Atari STE

`SONIC.PRG`: Sonic Chaos (Master System) running on an Atari STE, recompiled from the original
Z80 code to 68000.

- Machine: Atari STE or Mega STE (plain 8 MHz; a Mega STE runs at 16 MHz with cache).
  It needs a 4 MB machine: the program takes about 3 MB of RAM once loaded.
- Run `SONIC.PRG` from the desktop. Control: joystick in either port.
- The screen runs at the machine's own refresh rate (50 Hz or 60 Hz); game speed and music
  follow 50 Hz time on both.

Prototype only - performance is not 100%.

## Getting SONIC.PRG onto your Atari

### Floppy disk: not possible yet

`SONIC.PRG` is 1.8 MB, and a floppy holds 720 KB (double density) or 1.44 MB (high density),
so it does not fit on one disk, and a floppy emulator such as a GoTek has the same limits.
Use a hard disk, such as an UltraSatan (below).

### UltraSatan (SD card hard disk)

You need an SD card that your Atari already uses as a hard disk, with a hard disk driver such
as HDDriver, ICD Pro or PPDriver installed, and at least 2 MB free on one partition.

**If your PC can read the card** (partitions made "TOS & Windows compatible", which HDDriver
can do):

1. Switch the Atari off and take the SD card out of the UltraSatan.
2. Put the card in your PC and copy `SONIC.PRG` to one of its partitions, for example into a
   `GAMES` folder.
3. Eject the card safely, put it back in the UltraSatan and switch the Atari on.
4. Open the partition's drive icon on the desktop (C:, D:, ...) and double-click `SONIC.PRG`.

**If your PC cannot read the card** (plain Atari partitions), copy the file from the Atari
side instead, from any storage your Atari and PC can both reach: for example a second SD card
in the UltraSatan's other slot partitioned TOS & Windows compatible, a network drive, or a
serial/parallel file transfer program. Then copy `SONIC.PRG` onto the Atari partition with
the desktop and run it from there.

Tip: Start the game with no desk accessories or extra AUTO folder programs loaded, so that
enough memory is free.

### Hatari (emulator)

Point a GEMDOS hard drive at the folder that holds `SONIC.PRG` and run it as an STE with
4 MB of RAM:

    hatari --machine ste --memsize 4 --harddrive /path/to/folder

Then open drive C: on the desktop and double-click `SONIC.PRG`.

If the correct machine is already set up in hatari, you may also be able to start it with just
    `hatari SONIC.PRG`
