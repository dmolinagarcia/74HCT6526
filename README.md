# 74HCT6526 
The 74HCT6526 is a very amateur attempt at building a MOS6526 replica using discrete logic. This repo is publicly shared just for educational purposes, and I can offer no guarantee on the correct behaviour of this implementation. So far, it's working great for me, but I can't promise anything.

# History
Work on the 74HCT6526 began in the summer of 2018. I was so impressed by other attempts at replicating Commodore chips, that I wanted to give it myself a try. I chose the CIA, as it wasn't replicated back then, even though it seemed the simplest chip. I had no previous knowledge in electronics, only some lessons back in college more than 20 years ago.

> ###### Important note
> Please visit http://forum.6502.org/viewtopic.php?f=4&t=5593 for more information

# Versioning
74HCT6526 is released under the following versioning scheme:

> MAJOR.MINOR.REVISION

For a stack to work properly, is mandatory that all boards share the same MAJOR.MINOR versión. Any change than renders a board incompatible with the previous releases triggers a new MINOR version. If a version only includes fixes, but does not alter the buses, it's only a new revision. There may be some cases where boards with different MAJOR.MINOR version can actually work together, but this is not something I can guarantee or predict. A deep look at the schematics to understand the differences between releases is needed to actually confirm this.

Under the current scheme, I don't think I'll ever need a new MAJOR version, but it is nice to have it there, just in case.

# Manufacturing
All boards are tested against JLCPCB and PCBWAY capabilities. For PCBWAY, there is no increase in cost compared to the standard 4 layer board.

# Releases
* v0.1.0  First production run. Only includes B0 (DDR and PORTs)
* v0.1.0a First production run for B1. (TIMERA and CREGA)
* v0.1.1  Second production run for B1. Fixes TASTART issue. First B2 (TIMERB and CREGB) 
* v0.1.2  First production run for B3. (SDR and ICR)
* v0.2.0  First MINOR advance. B0+B1+B2+B3 tested and validated. 

# Changelog

## [0.2.1 ] - 26-Mar-2023
* All boards. Added pdfs for all schematic and pcbs for all versions for ease of access
* B1. Changes to Reload portion of TimerA pipeline to fix 01cmpold issue
* B2. Changes to Reload portion of TimerA pipeline to fix 01cmpold issue
* B3. Added switch to select OLD or NEW CIA

## [0.2.0 ] - 24-Jan-2023
* All boards. Removed TARUNMODE from the ControlBus
* All boards. Updated for JLCPCB and PCBWAY capabilities
* All boards. Minor aesthetic changes to schematics
* All boards. Updated PDFs on the release
* B1. Optimized CNT edge detector
* B2. Optimized CNT edge detector
* B3. Fixed FLAG edge detector in ICR
* B3. Fixed SDR input and output issues from v0.1.2 (not sending nor receiving)

## [0.1.2 ] - 01-Nov-2022 
* B3. First release. SDR and ICR
* B2. Updates for JLCPCB capabilities
* All boards. Schematic review. Added /RES capacitor to prevent false restarts

## [0.1.1 ] - 24-Aug-2022 
* B2. First release. 
* B1. Fixed additional cycle on forceload by removing second flipflop in the chain (rolled-back)
      Added additionad dFF to Start before being fed into the timer
      D and DZ moved to separate buses on schematic.
* B0. Routing optimized. D and DZ moved to separate buses on schematic. Silkscreen improved. 

## [0.1.0a] - 06-Jun-2022
* B1 with TimerA and Control Register A. Ready for production. 

## [0.1.0 ] - 19-Oct-2021
* Mounting holes pads were covered with soldermask. Soldermask removed and pads properly labeled.
* Silkscreen fixes
* Updated gerber files
* B0 with DDRs, PORTs, and bus interface

# Status updates
* January 24, 2023. v0.2.0 released. Fixes a potential problem on B1 and B2 with CNT edge detector. It also fixes some bugs on B3. A cleanup of schematic, PCBs and PDFs for all boards has been done. TARUNMODE is removed from controlbus as it is not needed. This triggers a new MINOR version
* November 01, 2022. v0.1.2 released. Includes B3 (SDR+ICR) and some minor tweaks to all boards.
* August 24, 2022. v0.1.1 released. Fixes a bug in B1 (TASTART) and adds B2. Minor routing fixes to all boards.
* June 06, 2022. v0.1.0a released. It adds B1 to v0.1.0
* October 19, 2021. v0.1.0 is released. It add B0 to v0.1.0
* September 12th, 2021. Repository is now public. B0 schematic is 100% done. PCB layout is 100% done. It's currently being reviewed before sending it into production
