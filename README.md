**Design Ideas:January 19, 1995**

## Low-cost audio VCA has high performance ##

**Mike Sims**,
*Lectrosonics Inc, Rio Rancho, NM*

---

The inherent matching between the two transconductance amplifiers in IC<sub>1</sub> (Fig. 1) facilitates a voltage-controlled amplifier (VCA) that offers high performance and low cost. The circuits maximum input voltage is +20 dBu (dBu=dB referred to 775 mV rms). THD measures less than 0.015%; noise, -70 dBu; and control-voltage feedthrough, -70 dB.

<table>
<tr>
<td><img src="https://web.archive.org/web/20180214061805im_/http://www.teaser.fr:80/~amajorel/sims/02di1fg1.gif"></td>
</tr>
<tr>
<td><i>Matched transconductance amplifiers enable an inexpensive voltage-controlled amplifier whose gain is linearly proportional to the control voltage.</i></td>
</tr>
</table>

The signal path is simple. IC <sub>1A</sub> negative-feedback configuration forces the current from IC<sub>1A</sub> pin 5 to equal the ac-input current through R<sub>1</sub>. IC<sub>1A</sub> pin 5 also connects to IC<sub>1B</sub> pin 13, causing a virtually identical current to flow from IC<sub>1B</sub> pin 12. IC<sub>2A</sub> converts this current to an output voltage, V<sub>OUT</sub> .

The output op amp limits the circuits maximum output voltage. (A dual FET-input op amp, such as the TL072, works well for IC<sub>2</sub>.) C<sub>1</sub> sets the circuits 3-dB bandwidth at about 40 kHz.

Varying the control current into IC<sub>1B</sub> relative to fixed current flowing through IC<sub>1A</sub> R<sub>2</sub> controls the circuits gain. R<sub>2</sub> sets the control current in IC<sub>1A</sub> to

I<sub>CONT A</sub> =(15-2V<sub>D</sub> )/R<sub>2,</sub>

which is approximately 265 &micro;A. The 2V<sub>D</sub> factor arises because the control-port voltage is two diode drops above the negative rail.

IC<sub>2B</sub> and associated components form a linear voltage-to-current converter that feeds the control port of IC<sub>1B</sub> . The control current for IC<sub>1B</sub> is 

I<sub>CONT B</sub>=V<sub>CONT</sub> /R<sub>3</sub>.

The overall circuit gain is

V<sub>OUT</sub>/V<sub>IN,</sub>=-(R<sub>4</sub>/R<sub>1</sub>) &times; (I <sub>CONTB</sub> /I<sub>CONTA</sub> ).

A 5V control signal generates unity gain. The gain is linearly proportional to the control voltage.

R<sub>2</sub> , in conjunction with R<sub>1</sub> , limits the circuits maximum input voltage to 

V <sub>INMAX</sub>=2 &times; I<sub>CONTA</sub>&times;R<sub>1</sub>,

or a peak input voltage of around 16V.

Use R<sub>5</sub> to trim the circuit for minimum THD. Trimming for minimum THD simultaneously achieves minimum control-voltage feedthrough. Interchanging pins 13 and 14 of IC<sub>1B</sub> realizes a noninverting VCA. (DI #1604)

---

*Copyright &copy; 1995 EDN Magazine. EDN is a registered trademark of Reed Properties Inc, used under license.*
