# MOUTH

### ⚠️ THIS MODULE HAS NOT YET BEEN BUILT, ATTEMPT TO BUILD AT YOUR OWN RISK ⚠️

![exits](/img/exits%20proto.jpg)

MOUTH is a DIY 8hp eurorack module designed to be the output stage of your patches. It has a 4 channel mixer with individual pan and level controls, and line and headphone outputs.

The project was derived from the [Exits](https://github.com/ramphands/Exits) module. Exits was a combination of the lines mixer project [Nearness](https://github.com/sarnesjo/nearness) and the [Forestcaver headphone amp](https://github.com/forestcaver/Analog-Voice/tree/master/AJH_Headphone_Amp). For MOUTH The patch-based stereo panning of Exits and nearness was changed out for individual pan and level controls for 4 tracks, and the Forestcaver headphone amp (based on the NJM4556AV-TE1 opamp) was changed out for a headphone amp loosely based on Chu Moy's famous ["CMoy" design](https://web.archive.org/web/20021223020724/http://headwize2.powerpill.org/projects/showproj.php?file=cmoy2_prj.htm) - in this case using the RC4580 instead of the OPA134 for availability and experimentation reasons. The module was expanded from 4hp to 8hp to accomodate the extra knobs. I also switched from 1/4" jacks for the two outputs - to 1/8" jacks for everything. The extra space on the widened input board, along with removing the two tall 1/4" jacks, allowed me to flatten the module from two PCBs to just one.

If you'd like to explore the pan + mix section, circuitjs simulation files are in the [simulations](simulations) directory.

The four mixer channels are DC coupled, so you can use this module to mix CV. The headphone output is not DC coupled, so only the line output will output DC offsets. At maximum volume the headphone output is about 1/10 the input level. J5 and J6 are jumpers - no pins bridged means the mixer has a gain of about 1x. Bridging pins 1 and 2 on both jumpers will set the mixer sections gain to 2/3x in case you're mixing hot signals and want to tone things down a bit. To add gain, you could bridge pins 1+2 and then desolder R17 and R20. That'll set the gain to just shy of 2x.

The following sources were used either directly or as learning material to construct the panning and mixing section:

- [Audio Signal Mixing](https://sound-au.com/articles/audio-mixing.htm) By Rod Elliott - a fantastic explainer of mixing circuits
- Erica Synths DIY eurorack [Output and Mixer](https://github.com/erica-synths/diy-eurorack) modules
- [Befaco Hexmix](http://www.befaco.org/hexmix/)

## Schematic and PCBs

-- CURRENTLY OUT OF DATE --

The [kicad](kicad) directory contains the schematic and PCB layout as a KiCad 6 project.

## Panel

-- CURRENTLY OUT OF DATE --

Available in the [panel](panel) directory as a PDF and an SVG vector file.

## Revisions and notes 

- Started with this commit of [Exits](https://github.com/ramphands/Exits/tree/e56ce6f3a76ff6dc0b776ba10d0bfae7fea7ace0)
- Switched from 4hp to 8hp
- Switched from 7 input channels to 4
- Switched from 1/4" jacks for line and hp to 3.5mm / 1/8" jacks for everything.
- Flattened the design from two PCBs to just PCB
- Switched to a CMOY style headphone output using the RC4580
- MOUTH's first "complete" post-Exits scheamtic, using passive mixing can be found in the git history [here](https://github.com/coryalder/Exits/blob/65a9d2693df2f5ae9116ffd591f22e5cf609d3db/exits%20schematic.april12th.pdf). After that I switched to current based mixing, per Rod Elliott's article
- MOUTH's first "complete" + "current-based" schematic is [here](https://github.com/coryalder/Exits/tree/e56ce6f3a76ff6dc0b776ba10d0bfae7fea7ace0)
- Re-routed the board with the changes above


## Todos:

- Make a panel and panel template
- Add 3d models for all the parts used
- Add board rendering images to the readme
- Add test points to make debugging easier
- Confirm the L&R channels are routed correctly (pan pot orientation)
- Build one, and confirm all of this works as intended

## License

[CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)

To summarize the license linked above - you are free to:

* Share — copy and redistribute the material in any medium or format
* Adapt — remix, transform, and build upon the material
for any purpose, even commercially. 

As long as you abide by the terms of the license which requires:

* Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

* ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original. 
