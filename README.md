# Joechei headphone amplifier

###### Warning: always beware of high sound volume, it can damage your hearing! First close your volume control and slowly increase the volume

![front with red button](https://github.com/Wanderingidea/Joechei/assets/42114791/7c1fb2a3-ab7c-4008-a062-647593fa0fb9)

Joechei Headphone Amplifier based on the famous Cmoy design
I rarely listen to music over the speakers. Instead for a long time I used a headphone amplifier published by the Elektor magazine of 1987: 'The Headphone Amp'. This headphone amplifier from Elektor is based around an old opamp, the OP-50, long out of production.
So boredom striked and because of the good reviews of the Cmoy headphone amp I decided it was time to make one and it had to be a desktop version.

Tweaking the original circuit to dig up the sound qualities hidden behind this 'non-inverting opamp circuit', it eventually turned out to be an extended version of the original circuit that I am very happy with. Hence the name 'Joechei', an old Dutch word to express happiness.

It does not matter what kind of music you throw at it, but to judge its sound quality and 'musicality' while tweaking I mostly used classical music and Jazz.
Still using one opamp (which was my intention and challenge) it is fairly easy to build.

For me the result is proof that very good sound does not have to be overly expensive.

### Circuit
The circuit is simple and the components are cheap: it consists of one dual opamp type OPA2134PA (see addendum for other opamps) and a power supply with two resistors and capacitors. These generate a positive and negative voltage for the opamp. This way the amp can be used with a single power supply (see addendum about other rail splitters).

Schematically I setup the circuit like this:
![blokschema](https://github.com/Wanderingidea/Joechei/assets/42114791/b327dbdc-c001-4393-b979-4571c15e0ca8)


And electronically like this:
![Joechei](https://github.com/Wanderingidea/Joechei/assets/42114791/bbdb09f1-1a5d-4fe4-ac91-64b07dd3dc00)

The amplification is (8.2k / 2k) + 1 = 5.1x<br>

### Balance
Because of component tolerances, not to forget off-balance hearing and a weird but interesting phenomenon it is possible one channel appears to be louder than the other. It made me think of the 'spinning dancer' effect where the brain tries to relate the direction to which the dancer turns with the visual clues it gets.

Since the stereo imaging of this headphone amplifier is better than before, I noticed the balance shifted a bit to the left, possibly because I try to relate the visual clues of what I look at with the auditory clues of the sound. Closing my eyes the balance shifted a bit back to the right.

Anyway, I wander from the subject but that is why I added a volume balance control at the back of the enclosure.

### RF
I payed special attention to block RF as much as possible at all 'paths', the input, output and power supply because I suspect the audio quality is negatively affected by this. 

RF is the reason why the 2.2 nF and 100 nF capacitors are ceramic ones.

### Component placement
An etched pcb looks nice but is a fuss to make. A circuit of this size can easily be made on a piece of perf board.

To keep everything small and orderly I first made a drawing of the way the components are placed on the board:
![board](https://github.com/Wanderingidea/Joechei/assets/42114791/61a3b8de-e320-4adf-a58d-31670b4f8406)

The Zobel network consisting of a resistor of 10 ohm and a capacitor of 100n in series at the output 'equalizes' the load to the opamp for higher frequencies.
I soldered it directly onto the headphone jack input.

The low pass filter to prevent RF from entering the input was also soldered directly onto the RCA input connectors.
 
The opamp is placed in a socket so it can be swapped later on if needed.

Start soldering the socket first, then the resistors, smaller capacitors and at last the bigger electrolytical capacitors. Watch out for the polarity regarding the bigger capacitors.

![IMG_20180630_104448](https://github.com/Wanderingidea/Joechei/assets/42114791/bf5fea17-a017-4779-80ca-67ddb05a89d0)

Solder the 100n capacitors as close to the opamp as possible.
If you use a metal enclosure use isolated mount sockets for the headphone jack input and RCA inputs or you will short the power supply. 
 
Below are some impressions with an other rail splitter or other opamps (see addendum). The boards may be different but the instructions stay the same.

![board top](https://github.com/Wanderingidea/Joechei/assets/42114791/8123646f-5913-4741-8218-86edf994226a)
![board bottom](https://github.com/Wanderingidea/Joechei/assets/42114791/3b81c480-0e80-4e2e-850a-15dba5e3be60)
![Yacha MKII - work in progress](https://github.com/Wanderingidea/Joechei/assets/42114791/a14d32a7-ef03-4dbe-b81c-f1488b6d6ab5)

After soldering has finished test the positive and negative voltage by temporarily connecting a 9 Volts battery. A voltage of plus 4.5 Volts and minus 4.5 Volts should be measured over the 4.7k resistors.
Also, the voltage between pin 4 of the socket and signal ground should be minus 4.5 Volts and the voltage between pin 8 and signal ground should be plus 4.5 Volts. Measuring this ok it should be safe to place the opamp in its socket after disconnecting the battery.

### Power supply
Using two 9 Volts batteries is not handy when using the amplifier on the desktop, although they seem to last long. And old laptop provided me with an adapter of a little more than 19 Volts.
Another advantage from using a switched power supply is to avoid the stray magnetic field, resulting in hum.

Check the resistance between 'input/mains' and the 'output' of the switched power supply (when not connected), it should be too high to measure. 

### Wiring
Start with wiring the power cables. Only power ground is connected to the aluminium case.

After that wire the signal ground. Connect signal ground to one point close to the signal input but do not connect it to metal enclosure. Therefore be sure to use isolated inputs and output if using a metal enclosure.

Here I used white cable for signal ground and red/black cables for power: 

![binnenkant](https://github.com/Wanderingidea/Joechei/assets/42114791/a280a4f7-05c0-4960-bd77-a4e831acd7a5)
![Yacha MKII - balance adj 1](https://github.com/Wanderingidea/Joechei/assets/42114791/b628f03b-0b03-4a2c-bdc1-b2463118b4f9)
![Yacha MKII - balance adj 2](https://github.com/Wanderingidea/Joechei/assets/42114791/04999023-6586-419b-924b-f1fec3259c80)

After wiring the power and signal cables wire the input and output.
Try to keep the signal wires and power wires separate. In the photo above the power wires are (mostly) on the left and the signal wires are on the right.

### Testing
Connect an old headphone at the first smoke test if possible and close the volume. Only then switch on the amplifier and open the volume slowly.

The amplifier is silent, no buzzing/humming or noise. I almost cannot hear it being switched on or off.

### Oscillation
If you hear unexpected weird sounds chances are the amplifier is oscillating.

The cable of the headphones acts as a capacitor. The longer the cable, the higher the capacity.  R5 and R8, the output resistors, prevent the opamp from oscillating due to this capacitive load at the output.

But unfortunately the value of the output resistor influences the sound. How much so depends on the type/brand and impendance of the headphones used.  Preferably R5 and R8 are not used. Without R5 and R8 the lower frequencies of the amplifier sound more accurate, for lack of a better word and for lack of measuring equipment.

Luckily some opamps are less susceptible to oscillation than others. In my experience these resistors are not needed when the OPA2134, AD826 or NJM4580 are used, for example.

If you have to use output resistors, a R5/R8 of 38 ohms is suitable for headphones with an impendance of 32 ohm, for Beyerdynamic DT 770 Pro 80 headphones 10 ohm is sufficient.

Oscillation can also be caused by the high frequency range of a fast opamp. This can be stopped by placing a 100 pF film capacitor over the feedback resistor of 8.2 kohms.

### Result
My setup:
- Archlinux
- mostly classical and Jazz music in flac format
- Audacious or Deadbeef music player bitperfect setting
- Topping E30 USB DAC
- Joechei headphone amplifier
- passive headphone correction filter
- Beyerdynamics DT770 Pro 80 headphones

To make the admittedly unfair comparison between the 'Headphone Amp' of the Elektor of 1987 and this Joechei headphone amp, there is a clear difference. Joechei sounds more expressive, more detailed and therefore more natural.

Compared to the Musical Fidelity 'X CANS' headphone amplifier, Joechei sounds so much more detailed and less muffled that I am thinking of replacing the internals of these 'X CANS' headphone amplifier by Joechei.

The difference between good and bad recordings is clearly audible, yet it seems to extract the musicality even from bad recordings.

The soundscape is well defined, the tonal quality is well balanced. The amplifier does not sound harsh in the upper frequency range. If needed the lower frequencies are being called upon with quality and impact. Voices sound natural.
For example, listen to 'Ocean' of Gian, the dynamics of the recording and the instrument as it moves through the vast space.
Or in Marillion 'Brave' the smallest details can be heard without increasing the volume, a refinement my old headphone amplifier lacked.
Representing the sound of the piano is a challenge for amplifiers but in 'Irina in A - Schubert - Bach - Brahms' I am convinced Irina Mejoueva plays the real thing.
 
The amplifier has more than enough power to drive my 80 ohm headphones. Like the designer of the Cmoy headphone amplifier, Chu Moy said: "...It can output almost 40mA into a short circuit at room temperature. Modern dynamic headphones need about 10mW to reach full volume...". That is the reason I focused on using only one opamp to drive my headphones, more is less. Tests and my own experience confirm using just one opamp is possible.

I suspect the countermeasures to limit RFI play a major role in the quality. One supporting fact is this: while building one version I forgot to add the ferrite bead at the output (there is only one needed for both left and right). After the enclosure was closed I noticed it was susceptible to hum when I touched it. When I added the ferrite bead the hum was gone. The long headphone cable must have picked up RF creating a loop when I touched the case. At least, that is my theory.
See the sources at the end of this article.
As you may have noticed I do not have a tendency to change components once I find they qualify to fulfil their purpose. This headphone amplifier stays as is.
And it is very reproducable. By now I must have made four or five of these, all show the same quality but I advise to read the addendum below to squeeze out the last bit of performance out of this amplifier. 

Overall, I am very satisfied with the result, the 'price/quality' ratio is excellent. 

Joechei!

## Addendum
The standard version of Joechei already sounds great but it can be upgraded by trying the options described below.

### Other opamps?
It is possible to use a different opamp but check some properties first. 
First check the datasheet for the maximum allowed supply voltage and maximum output current. The latter should be sufficient for the headphones used. 
With the source connected measure the voltage (DC) at the output: it should not be more than 30mV per channel. You risk damaging your headphones if it is higher. 
For example, if I use an NJM4556 opamp the DC offset of both channels are 24mV.

If you do not use a FET opamp this circuit has a higher chance of oscillating so beware. In my experience for example a LM4562 will not work but an AD826 or NJM4580 will.
If it oscillates experiment with the value of R5/R8 and/or use a 100pF feedback film capacitor. It seems placing a 10uF/35V capacitor over pin 4 and 8 also can help but I did not test that.

By now my preference is, high to low on a scale from 10 to 1:
NJM4580 in class A (9) - NJM4556 in class A(9) - NJM4580(8) - AD826(8) - NJM4556(7) - TLE2082CP(7) - OPA2134(7) - prob fake OPA627(5) - MAX97220(4) 

Other possible ways to create a virtual ground?
Joechei creates a virtual (signal) ground with two resistors and two capacitors, also called a rail splitter. However it is also possible to create the virtual ground another way.

I tried the Sijosae rail splitter:

![transistor rail splitter](https://github.com/Wanderingidea/Joechei/assets/42114791/2e768b85-c3dd-469f-a639-24057218bc97)

and compared it with the original resistor rail splitter and this opamp rail splitter: 

![opamp rail splitter](https://github.com/Wanderingidea/Joechei/assets/42114791/621e9ea1-4e0f-4085-9ae0-2fa1d98764fc)

Implemented like this:

![Yacha v5 - top side](https://github.com/Wanderingidea/Joechei/assets/42114791/4cae7135-c962-48fa-ab87-4922f8571216)
![board 2 - bottom side](https://github.com/Wanderingidea/Joechei/assets/42114791/b3108b80-c8bb-4644-ba51-6b4c463f3009)


I can hear no difference between the Sijosae rail splitter and the opamp rail splitter but both are slighty better in stereo imaging than the original passive rail splitter.
 
### Use metal film or carbon resistors?
Carbon resistors are less stable, give more noise than metal film resistors, and the values are less accurate.
However I use metal film and carbon resistors interchangeably without adverse effect. I keep the values as close together as possible and keep both channels consistent e.g. two 8.2k metal film resistors, two 2k carbon resistors and so on, see the photo above.

### Input capacitors
In theory it is beneficial to get rid of the input capacitors as they influence the sound in a negative way. I tried that but I got DC offset at the output in return. The sound improvement is not worth the risk of damaging my headphones.
Then I swapped the 470nF capacitors for 1,5uF polypropylene capacitors. Any improvement in sound is probably my imagination playing tricks but it proves that a higher value can be used without problems.

### Class A
It is possible to set the opamp in class A, thereby lessening crossover distortion, resulting in a 'smoother' and more detailed sound.
Just soldering two 10 kΩ resistors directly onto the opamp is necessary: one 10 kΩ resistor between pin 1 and 4 and the other between pin 7 and 4:

![Class A](https://github.com/Wanderingidea/Joechei/assets/42114791/0f84fc45-753f-491e-8af3-8a8082543dc9)


These resistors set the current at the output to a more or less constant 0.95 mA when using +/- 9.5 Volts.
The result depends on the opamp, it seems especially older type opamps benefit from this hack. In my experience the NJM4580 or NJM4556 are suitable, these opamps handle the extra current with ease, up to 2.5 mA.

![NJM4556 class A](https://github.com/Wanderingidea/Joechei/assets/42114791/e98e0984-b431-40b0-a90f-0cd0267a411c)


Biasing the opamp does not influence DC offset at the output, tested that.
This hack is highly recommended.

 

