# Linux-Audio-Interface

i kind of regret purchasing Focusrite Clarett 8pre USB,

requires a Control software that Focusrite does Not want to help translate to Linux,
everything works but DSP cannot be controlled on Linux.
works in Wine but does Not have USB passthrough.

did found a sollution for the issue with USB Audio & PulseAudio.

Anyway... i have the legend: RME hdsp9632 PCI stored,
IF i sell the Focusrite, 
im undecided:
to buy a PCIe to PCI chasis for the hdsp9632, 
also i have a Lynx AES16 pci, but requires OSS drivers,
or buy AIO Pro with Newer technology, but Chasis is way cheaper 1/3.

i'm done with Win & Mac, im out of that waggon.

RME hdps9632 was very nice for Linux,
with KX Studio 10.04 era... & AV Linux,

but sensible to ATX PSU noise, Spread Spectrum Noise. etc....
i dont know how low the DC noise of the Expansion Chasis is, but can be solved.

the problem with PCI and PCIe Audio
are the MPS Tables on the Motherboard Bios,

for example: 
Digi001 pci works ok in WinXP + Asio driver 6.4
with Asus P5W DH Deluxe 975x board,
but FAILs 100% on X58 Board from 2010, just 1 generation more.
same XP hdd, same everything, well installed, proper drivers... does Not work.
 
has too many audio drops, useless. 
but CPU is a lot faster.
Q6600 vs. X5687
4-core vs. 4-core
https://www.cpu-world.com/CPUs/Xeon/Intel-Xeon%20X5687%20-%20AT80614005919AB.html

ive read some people experience a similar problem with RME AIO Pro,
that makes me worry.

The noise problem can be solved, but the MPS tables No way....

Lynx AES16 pci has a similar problem,
does Not install with Boards that do Not have proper MPS Tables 1.4
Asus Rampage 3 Extreme Fails on Win8.1x64
but msi and ASRock install ok.
Gigabyte uknown.
AMD Tyan S8232 server board "works but...has issues"

Lynx AES16 only installs on Win8.1x64 if board has MPS 1.4 on the Bios.

Windows7x64, only requires MPS tables 1.1
works ok if fails to install on W8,1
hackintosh with SnowLeopard also works ok in the same board.

another strange problem:
Lynx AES16 on intel works ok, 
but with the Tyan AMD board, Buffer Size is scrambled.
settings are in wrong order.
when measuring real audio latency.
128 = 512
256 = 1024
512 = 256 
etc...
when measuring real audio latency & CPU load "drop outs/glitches".

Anyway....
PCI and PCIe Audio is risky in my experience.
has too much variables....

MergingTechnologies/ravenna-alsa-lkm driver looks interesting, but free version fails to compile.

Also noticed when testing USB vs. PCI
that buffer size is Not the same,
PCI 32 = 64 USB.
64 PCI = 128 USB
128 = 256
256 = 512
512 = 1024
1024 = 2048
etc...
Lynx AES16 using old 192Khz AD/DA + ADAT
vs.
Focusrite newer/faster AD/DA IC

if i change the AD/DA or AES/EBU instead of LS-ADAT, 
latency also change.
Rabbit Hole.

in USB, buffer settings have audio drops every x time.
if you monitor a constant Sine or Noise for several minuteson Win8.1x64.
but if you Record, records ok, very odd USB drivers or older USB Firmware.

i want RME for Linux but PCIe is risky & more $$$ vs. expanwsion chasis.

...chasis will work?
another Rabbit Hole.
probably will require FW updates if possible.

im curious to hear the New SteadyClock FS, but too much $$ for No mic-pres.
i think im going for the Chasis Rabbit Hole.

Optional RME drivers, different than ALSA for hdsp9632.
https://github.com/PhilippeBekaert/snd-hdspe
https://github.com/PhilippeBekaert/hdspeconf

Focusrite USB Scarlett Gen 2/3
https://github.com/geoffreybennett/alsa-scarlett-gui/blob/master/USAGE.md
https://github.com/geoffreybennett/alsa-scarlett-gui

Forum:
www.linuxmusicians.com
