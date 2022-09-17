# RogueOne

## Overview 
This is a modification of the Shady_RC by JoyMonkey. This was made to use the Flysky controller with 10 channels. The FS-I6X is relatively cheap digital controller. It uses a receiveer that has an IBus interface which plugs into the ATMega board. There is some setup with the controller out of the box. That is basically to assign the keys or map the keys to the right functions. This is more based off of ShadyRC, with modifications to a 10 channel receiver. 

**References** 
[Shadown MD](https://www.printed-droid.com/kb/shadow-md-droid-control-system/)
[ShadyRC_Evelotion](https://github.com/joymonkey/dEvolution/blob/master/sketches/ShadyRC_Evolution/ShadyRC_Evolution.ino)

## FlySKY setup
There are two menu options if you long press the top right button it brings you to a setup menu. Press the up and down buttons on the left side to select if you want to system setup or functions setup.

![Flysky FSi6](images/FS-i6X.png)

Press the select button again "top right button" to make the menu selection.

To back out of an option press the lower right button, which is a cancel button. 

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
