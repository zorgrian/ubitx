# Rewrite of explanation by M0OOZ

**This is a rewrite of the explanation of how the uBITX filters should work**

## Please see the .PNG files showing the schematic of these filters.
NOTE: **3.5 to 5 MHz** this filter is a problem if you use this filter on the 80-meter band above 3.5 MHz, as the second harmonic is over attenuated!

e.g. tune at 3.8 MHz (Europe 3.500–3.800) and the result is a whopping 10 dB cut! Para los Americanos, el problema es aun mas...!

Note: If we then use this filter at 5 MHz we do see a 36dB cut! (Nasty)... However al is solved in V5 where you can just jack up the power on the finals to compensate? (Hmmm not too sure that this is good practice)

### How the uBITX harmonic filters should be selected in V3 & V4 boards

#### FILTERS FOR UBITX

**The four harmonic filters use only three relays which are denoted as KT1, KT2 & KT3**

It is the states of these three relays, (ON/ OFF) in each case, that determines which filter is selected to have the PA signal passed though to ensure attenuation of appropriate harmonics at selected frequencies.

#### The four LPFs cover 
1. 21 - 30  MHz, 
1. 14 - 18  MHz, 
1. 7 - 10 MHz,
1. 3.5 to 5 MHz

### Briefly, it should work like this:
1. When KT1 is in the OFF state, the 'off' position then routes the PA output through the 30 MHz LPF
2. When KT1 is ON, it routes the PA output into KT2. Which is why you will see that:
3. The KT1 relay is switched on for the three other cases.
4. When KT1 is ON *and* KT2 is off, the off position of KT2 routes the PA output to the 18 MHz LPF (This is also used for the 14 MHz band as per above)
5. When KT1 is ON AND KT2 is ON, this routes the PA output into KT3
6. When KT3, is switched ON, this selects the 7-10 MHz filter.
7. When KT3 is switched OFF, this selects the 3.5 - 5 MHz filter

### Relay states
- Frequency >   21.000Mhz   : TXA Off, TXB Off, TXC Off
- Frequency >=  14.000Mhz   : TXA  On, TXB Off, TXC Off
- Frequency >=  7.000Mhz    : TXA  On, TXB On, TXC Off
- Frequency >=  0Mhz        : TXA  On, TXB On, TXC On


#### NOTE:
And that is how it should work. Except on the V3, & V4 boards the relays lack ground plane, and the type of relay chosen also allows radiation of RF into the surrounding circuitry. This may be solved in the V5 board?

Note: See the circuit to understand the above explanation.
