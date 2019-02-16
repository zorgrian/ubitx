# Rewrite of explanation by M0OOZ

**This is a rewrite of the explanation of how the uBITX filters should work**

### How the uBITX harmonic filters should be selected in V3 & V4 boards

#### FILTERS FOR UBITX

**The four harmonic filters use only three relays which are denoted as KT1, KT2 & KT3**

It is the states of these three relays, (ON/ OFF) in each case, that determines which filter is selected to have the PA signal passed though to ensure attenuation at appropriate frequencies.

#### The four LPFs cover 
1. 21 - 30  MHz, 
1. 14 - 18  MHz, 
1. 7 - 10 MHz,
1. 3.5 to 5 MHz

### Briefly, it should work like this:
1. When KT1 is in the OFF state, the 'off' position then routes the PA output through the 30 MHz LPF
2. When KT1 is ON, it routes the PA output into KT2. Which is why you will see that:
3. The KT1 relay is switched on for the three other cases.
4. When KT1 is ON *and* KT2 is off, the off position of KT2 routes the PA output  to the 18 MHz LPF (This is also used for the 14 MHz band as per above)
5. When KT1 is On AND KT2 is On, this routes the PA output to KT3
6. When KT3, is switched ON, this selects the 7-10 MHz filter.
7. When KT3 is switched OFF, this selects the 3.5 - 5 MHz filter

#### NOTE:
And that is how it should work. Except on the V3, & V4 boards the relays don't have ground plane, and they also radiate RF into the surrounding circuitry! This may be solved in the V5 board?

Note: See the circuit to understand this
