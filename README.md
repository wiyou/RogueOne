# Rogue One 

## Overview 
This is a modification of the Shady_RC by JoyMonkey. This was made to use the Flysky controller with 10 channels. The FS-I6X is relatively cheap digital controller. It uses a receiveer that has an IBus interface which plugs into the ATMega board. There is some setup with the controller out of the box. That is basically to assign the keys or map the keys to the right functions. This is more based off of ShadyRC, with modifications to a 10 channel receiver. 

**Reference repositories:** 

[Shadown MD](https://www.printed-droid.com/kb/shadow-md-droid-control-system/)

[ShadyRC_Evolution](https://github.com/joymonkey/dEvolution/blob/master/sketches/ShadyRC_Evolution/ShadyRC_Evolution.ino)

## FlySKY setup
There are two menu options if you long press the top right or **OK** button it brings you to a setup menu. Press the up and down buttons on the left side to select if you want to system setup or functions setup.

![Flysky FSi6](images/FS-i6X.png)

Press the select button or **OK** again "top right button" to make the menu selection.

To back out of an option press the lower right button or **Cancel** button. 

TO SAVE your options LONG press the cancel button. This is so un intutitive. 

The following is what is set up under each of the menu settings (system and function). All the other settings are left alone and uses the default settings.

**System Setup** 
1. Set the model TYPE to *standard airplane or glider*

**Function Setup**
1. Reverse to all normal

**Aux. Channels**
1. Channel 5 = *Swa*
2. Channel 6 = *SwB*
3. Channel 7 = *VrA*
4. Channel 8 = *VrB*
5. Channel 9 = *SwC*
6. Channel 10 = *SwD*

## Transmitter orientation/navigation

The following actions do the following. 

### On Start up
All toggles are up and the sticks for channel 1-4 are in neutral or down positions.

| SwA | SwB | VrbA | VrbB | SwC | SwD | Description |
| ----|-----|------|------|-----|-----|-------------|
| From Up to Down| N/A   | N/A n | Adjust Volume | Middle position | Up | Play Cantina music|
| From Down to Up| N/A   | N/A  | Adjust Volume | Middle position | Up | Play Starwars Intro music|
| N/A | Up to Down  | N/A | Adjust Volume | Middle position | Up | Play Imperial March music|
| N/A | Down to Up  | N/A | Adjust Volume | Middle position | Up | Play Starwars Disco music|
| N/A | N/A   | any position | N/A | middle to Up | Up | Play Random noise|
| N/A | N/A   | any position | N/A | middle to Down | Up | Play Random noise|
| N/A | N/A   | N/A | adjust | toggle to middle position | Up | Change volume|
| N/A | N/A   | N/A | N/A | N/A | toggle to down | Enable Auto Dome sounds|

# Electronics

**Parts list**
- [ELEGOO MEGA R3 Board ATmega 2560 + USB Cable Compatible with Arduino IDE Projects RoHS Compliant](https://www.amazon.com/ELEGOO-ATmega2560-ATMEGA16U2-Projects-Compliant/dp/B01H4ZLZLQ?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&psc=1&smid=A2WWHQ25ENKVJ1)
<img src="images/elegoo-board.jpg" alt="ATMega 2560" width="400"/>  

- [Flysky FS-iA10B receiver](https://hobbymatehobby.com/products/flysky-fs-ia10b-10ch-receiver-for-transmitter-fs-i10-fs-i6s-th9x-for-fpv-drone-rc-helicopter-telemetry-receiver-w-ppm-sbus?currency=USD&variant=32274066309169&gclid=CjwKCAjw4JWZBhApEiwAtJUN0KOPYcFzvfXK9iQGjkgz_hnRVqH_rOxxC0v8As5NhFmXVAHhFa9pgRoCuk4QAvD_BwE)
<img src="images/flysky-ia10b-receiver.jpg" alt="Flysky-Receiver" width="300"/>  

- [DFRobot DFPlayer](https://www.digikey.com/en/products/detail/dfrobot/DFR0299/6588463?utm_adgroup=TANE%20ALARM%20PRODUCTS&utm_source=google&utm_medium=cpc&utm_campaign=Shopping_DK%2BSupplier_Tier%202%20-%20Block%202&utm_term=&utm_content=TANE%20ALARM%20PRODUCTS&gclid=CjwKCAjw4JWZBhApEiwAtJUN0EJeeAKlE_UHkRag86wsOOUmCqrXYDFXIqQU01XdTdXRZyFKTjDDXhoCWKMQAvD_BwE)
<img src="images/dfplayer.jpg" alt="DFPlayer" width="200"/>  

- Micro SD Card 
- 3.5 Speaker

The wiring looks something like this for the basic sound system. But where the wires go out to the speaker in the below diagram you can route them to the input to an amplifier card like [TPA3116DA DC 12V 24V 100W Mono Channel Digital Power Audio Amplifier Board](https://smile.amazon.com/XH-M542-TPA3116DA-Amplifier-TPA3116D2-Capacity/dp/B07Z461JZX/ref=sr_1_6?crid=938EG4JLHB1L&keywords=TPA3116DA+DC+12V+24V+100W+Mono+Channel+Digital+Power+Audio+Amplifier+Board+TPA3116D2+Large&qid=1663602785&s=industrial&sprefix=tpa3116da+dc+12v+24v+100w+mono+channel+digital+power+audio+amplifier+board+tpa3116d2+large%2Cindustrial%2C167&sr=1-6)
![Electonic Diagram](images/WiredDiagram.png)


# Sound card
Found a few tips about how the files are stored in the sound card. The DFPlayer is not super smart like the SparkFun MP3 Trigger....but with a lower cost comes a few extra steps but not hard.

File names should be begin with 3 digit number and .mp3 file format extension. Examples that work: 001.mp3 or 001-BeepBop.mp3. The card can hold up to 1000 files per directory, but for R2 sounds the largest number of files of sounds I found were about 169. 

In addtion those file numbers don't mean the actual order to play. What you should do is copy files over one at a time to the SD card by the number order. 

## Mac Users
**NOTE**: If you are using Mac OS X to copy the mp3, the file system will automatically add hidden files like: "._0001.mp3" for index, which this module will handle as valid mp3 files. It is really annoying. So you can run following command in terminal to eliminate those files.

dot_clean /Volumes/<SDVolumeName>
Please replace the to the volume name of your SD card.

Further technical details: 
[DFPlayer Spec sheet](https://wiki.dfrobot.com/DFPlayer_Mini_SKU_DFR0299)


