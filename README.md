# Atari 800 Keyboard

Despite using a variety of keyboard manufacturers and designs over its production, it seems that all Atari 800 computers have a keyboard that is destined to fail, if it hasn't already. Luckily, we live in a time where making completely custom keyboards is a hobby, so I figured I could take advantage of this to create a brand new, drop-in replacement keyboard using commonly available parts. 

![Assembled PCB](/images/PopulatedPCB.jpg)

## Goals

- Drop-in replacement with no modding of the Atari necessary
- Use widely available Cherry MX style switches, so others can choose the feel they prefer.
- Reuse original key caps to keep the original look

# Making your own

## Parts Needed
- 1 PCB 
- 57 Cherry MX style PCB mount switches
- 18 pin right angle header
- 18 Female-Female jumper wires
- 3d printed parts (see Keys and Mounting below)

## PCB

The KiCad files are in the [PCB](/PCB) folder. Also included is a [.zip](/PCB/Atari800Keyboard.zip) file you can upload to your favorite board house for manufacturing. It's a 2 layer design with some vias connecting the sides, so making the PCB at home might be a challenge. 

Assembly is straight forward. Each switch location is labeled for what key it is. Insert PCB mount switches, solder the pins and solder on righit angle pin headers on the bottom for the connection to the Atari. 

I was unable to find 18 pin ribbon cables with single row connectors, so I opted to use a strip of female to female jumper wires. You could also use half of the connections of an IDE cable. 

## Adding Keys

I wanted to use the original key caps from the Atari, as they have special legends and sizes that would be hard to recreate in a modern cap. This required designing a 3D printable adapter to connect the Hi-tek/Stackpole caps to a Cherry MX stem. This adds significant height to the keys, but luckily the original PCB (and therefore the replacement) sit very low in the case and the height of the adapters allow the keys to sit at the same height as the OEM keyboard. The adapters are simply pressed onto the Cherry MX stems and then the Atari caps are pressed into the other side. Friction keeps everything in place. 

### Stackpole Caps

The PCB was designed with the same switch locations as the Stackpole keyboard, so you just need to print 57 of the [standard adapters](/STL/StackpoleMXAdapterV3.1.stl). These are very small and you should be able to print them all at once on most printers. They should be printed with the MX + side facing up and supports are not needed. 

### Hi-Tek Caps

The Hi-tek board I have used caps with offset posts for the larger keys such as the shift and enter keys. Since I only had a stackpole keyboard when designing the PCB, I created special adapter for the 1.5 unit and 2 unit wide keycaps. You'll need to print four of the [1.5u adapters](/STL/StackpoleMXAdapter-1.5U.stl), one [2u adapter](/STL/StackpoleMXAdapter-2U.stl), and 52 of the [standard adapters](/STL/StackpoleMXAdapterV3.1.stl). Both the wide and standard adapters should be printed with the MX + side facing up and supports are not needed. 

## Mounting the Keyboard

Print two of the [bottom mounts](/STL/BottomMount.stl), and one of each of the top [left](/STL/TopLeftMount.stl), [center](/STL/TopCenterSupport.stl), and [right](/STL/TopRightMount.stl) mounts. The two bottom mounts slide over the bottom edge of the PCB and line up with the mounting holes to ensure the PCB sits at the correct hight, relative to the case. The three top mount pieces are also used for aligning the board, but also serve to support the top of the board and keep it from flexing during use. 
