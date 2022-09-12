# 74HCT6526 
The 74HCT6526 is a very amateur attempt at building a MOS6526 replica using discrete logic. This repo is publicly shared just for educational purposes, and I can offer no guarantee on the correct behaviour of this implementation.
Even though the project begun back in July 2018, it's currently going through a full reboot. The older implementation is no longer public, and I'm sharing my new design even though it's being implemented right now. 

> ###### Important note
> Please visit http://forum.6502.org/viewtopic.php?f=4&t=5593 for more information

# Releases
* v0.1.0  First production run. Only includes B0 (DDR and PORTs)
* v0.1.0a First production run for B1. (TIMERA and CREGA)
* v0.1.1  Second production run for B1. Fixes TASTART issue. First B2 (TIMERB and CREGB) 

# Changelog
## Unreleased
* B3. First release. SDR schematic done
* B2. Updates for JLCPCB capabilities

## [0.1.1 ] - 08-24-2022 
* B2. First release. 
* B1. Fixed additional cycle on forceload by removing second flipflop in the chain (rolled-back)
      Added additionad dFF to Start before being fed into the timer
      D and DZ moved to separate buses on schematic.
* B0. Routing optimized. D and DZ moved to separate buses on schematic. Silkscreen improved. 

## [0.1.0a] - 06-06-2022
* B1 with TimerA and Control Register A. Ready for production. 

## [0.1.0 ] - 10-19-2021
* Mounting holes pads were covered with soldermask. Soldermask removed and pads properly labeled.
* Silkscreen fixes
* Updated gerber files
* B0 with DDRs, PORTs, and bus interface

# Status updates
* August 24, 2022. v0.1.1 released. Fixes a bug in B1 (TASTART) and adds B2. Minor routing fixes to all boards.
* June 06, 2022. v0.1.0a released. It adds B1 to v0.1.0
* October 19, 2021. v0.1.0 is released. It add B0 to v0.1.0
* September 12th, 2021. Repository is now public. B0 schematic is 100% done. PCB layout is 100% done. It's currently being reviewed before sending it into production
