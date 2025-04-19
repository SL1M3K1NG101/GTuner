# Guitar Tuner
## Description:
This is a simple homemade guitar tuner anyone can make, taking the input from an audio cable, transmitting it into an Arduino Uno and giving you the note you've played and how sharp/flat the note is.

## Status:
System still needs to be wired up irl for testing.

## Bill of Materials:
Bill of Materials
## Casing for Parts:

## Build Instructions:

First is making sure the casing has the correct holes along its side, two to be exact.
  1. Drill a 3/4" hole into the side of the box to house the on/off rocker switch.
  2. Drill a 1/2" hole next to it to fit the audio jack.
Second is wiring the On/Off switch and the Audio jack into the casing of the box. 
  3. Wire the positive end of your battery snap onto one end of the switch.
  4. Add another wire onto the switch will be later soldered into the first board.
  5. Solder a Green wire to the output of the audio jack and a black for the ground of the audio jack
  6. Ideally the M-Type power plug for your Arduino will have a red and black wire but if not solder them on.

The imaging of the wiring of the amplifying and offest board.

Soldering the amplifier

 7. Solder your TL082 onto the larger gridstyle board
  8. Solder the resistors and a wire to the output of the amplifier.
  9. Solder the capacitors and restistors to get the DC offset needed in the system.
  10. Solder wires that will be later connecting the DC offset to the 5v, Analog 0 and Ground of the arduino.

Soldering the Power

  11. Now connect the other red wire from the switch to pin 8 of the TL082 chip, the +VCC and solder the black wire to the ground
  12. Solder the black wire of the second battery snap, not connected to the switch, onto pin 4 of the TL082, the -VCC. and the red wire to the ground.
  13. Take the Green wire from the Audio jack and solder it into pin 3 of the TL082, the non inverting/positive input. then solder the black wire of the audio jack to the ground.
  14. All grounds of the system will be wiried into the ground of the arduino.
  15. The red wire from the powerplug thats connected the the arduino will be soldered as well onto pin 8 of the TL082. Black wire once again on ground.
  16. Now plug the wires for the 5v, Analog 0 and Ground into the arduino.
Soldering the Lights
  This will be using the second pc board to wire up the lights to tell what the tuning of your guitar is.
  17. Solder the first 6 LEDS on the top half of the board, making sure to have a 150 Ohms resistor on the positive end of each one of them and a wire leading out of the positive side.
  18. Solder the second row of 5 LEDS on the bottom half, also with a 150 Ohms resistor on each of of them
  19. Solder all of the grounds together.

Connecting Light board onto Arduino

  20. Connect the wires from the light board onto the arduino in the following order:
 
      leftmost red LED, signifying the flat end - pin 8
   
      next red LED to the right - pin 9
  
      next red LED to the right - Analog 5
  
      green LED (in tune) - Analog 4
  
      first red LED to the right of the green LED - Analog 3
 
      next red LED to the right - Analog 2
  
      rightmost red LED (most sharp) - Analog 1
  Row 2
      leftmost LED, where E will be - pin 2

      LED where A will be - pin 3
      
      LED where D will be - pin 4
      
      LED where G will be - pin 5
      
      LED where B will be - pin 6
      
      rightmost LED where E will be - pin 7

  22. Then connect the ground wrie from the light board onto the ground of the aruduino.

Close up the system and you're done!
