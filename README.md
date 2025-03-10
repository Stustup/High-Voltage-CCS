# High voltage constant current sorce/sink

I often need a simple low to medium current constant current source for tube amplifier projects. [Pete Millett recently released a CCSS board](http://pmillett.com/CCS.html), but the integrated heatsink made it a bit too bulky for my taste and case of my DIY SET headphone amp (coming soon).

<p align="center">
    <img src="./Hardware/doc/HV%20CCS%203D%20View.png" width="350">
</p>

The board gets its small size from the (if i may say so) relatively uncinventional way you mount the board and its TO220 package to the case. you only need a single mountin hole on your amps case, an insulation washer and a (preferrably nylon) spacer. The mounting holes are made for M3 - M3.5 bolts.

![Schematic of the CCS](./Hardware/doc/HV%20CCS%20Schematic.png)

The CCS consists of a cascaded MosFET (or JFET for the lower device) topology as per for example "Valve Amplifiers by Morgan Jones p.152 (D)". 

You have the coice on every stage on what device you want to use. The upper stage sees most of the voltage drop, so you have the choice of a TO220 and a SOT89 package. Use the TO220 for possible power dissipations of up to 1W, the SOT89 for everything below. I did this to get the footprint even smaller when you need it, e.g. Anode Resistors in small current pre stages. 

In the lower stage you can choose between a SOT89 (same as above) and a SOT23 package. For currents above 5mA use the SOT89, for currents above use the SOT89 device. The SOT23 package can be a JFET to get low noise low current sinks/sources.