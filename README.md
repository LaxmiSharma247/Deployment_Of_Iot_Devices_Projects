### Description:
Simon is a simple electronic memory game: the user has to repeat a growing sequence of
colors. The sequence is displayed by lighting up the LEDs. Each color also has a
corresponding tone.

In each turn, the game will play the sequence, and then wait for the user to repeat
the sequence by pressing the buttons according to the color sequence. If the user
repeated the sequence correctly, the game will play a "leveling-up" sound, add a new
color at the end of the sequence, and move to the next turn.

The game continues until the user has made a mistake. Then a game over sound is
played, and the game restarts.

![Simon Game Shield for Arduino Uno](https://i.imgur.com/CBVsVxzh.jpg)

### Hardware

| Item             | Quantity | Notes                        |
| ---------------- | -------- | ---------------------------- |
| Arduino Uno R3   | 1        |                              |
| 5mm LED          | 4        | Red, Green, Blue, and Yellow |
| 12mm Push button | 4        | Red, Green, Blue, and Yellow |
| Resistor         | 4        | 220Ω                         |
| Piezo Buzzer     | 1        |                              |

<figure>
    <img src="https://i.imgur.com/cnNS8rsh.jpg" alt="Simon hardware kit" />
    <figcaption>
      Hardware for the Simon game, 
      <a href="https://www.tindie.com/products/wokwi/kit-for-simon-style-game-arduino-shield/" target="_blank">
        kit available on Tindie
      </a>
    </figcaption>
</figure>

### Connection Diagram
The diagram shows how the components are wired in the shield PCB (Printed Circuit Board):

![image](https://github.com/LaxmiSharma247/Deployment_Of_Iot_Devices_simon-with-score/assets/112362299/6dc87ca8-2e76-41c0-b102-e45de572d028)


### Pin Connections

| Arduino Pin | Device        |
| ----------- | ------------- |
| 12          | Red LED       |
| 11          | Green LED     |
| 10          | Blue LED      |
| 9           | Yellow LED    |
| 8           | Buzzer        |
| 5           | Red Button    |
| 4           | Green Button  |
| 3           | Blue Button   |
| 2           | Yellow Button |

- The LEDs are connected through a 220Ω resistor each.
### Assembly Guidelines
To make assembly easier, it's advised to begin with the lower-profile components first. Polarity is only important for the LEDs, the other components can be assembled in any direction.

Here is the recommended soldering order: 
1. Solder the four 220Ω resistors
2. Solder the Piezo buzzer (the black part)
3. Solder the 4 LEDs, paying attention to their polarity (see below)
4. Solder the 4 Tactile Push Buttons.
5. Flip the board, and solder the pin headers (see below).

Make sure you pay extra attention to orientation of LEDs, otherwise the LEDs won't function! The longer leads should be where the white circle is curved, facing AWAY from the WOKWI logo. The red arrows in the following photo indicate where you should put the longer lead of each LED:
![image](https://github.com/LaxmiSharma247/Deployment_Of_Iot_Devices_simon-with-score/assets/112362299/6aa84f1d-3966-4b59-8400-b1fa0e7cb025)

When soldering the pin headers, it's recommended to place the board on top of an Arduino board. This helps to solder them straight. The longer part of the pins should go into the Arduino board, and the black plastic should be between the Arduino board and the Simon Game Shield PCB:
![image](https://github.com/LaxmiSharma247/Deployment_Of_Iot_Devices_simon-with-score/assets/112362299/cd748a1d-35ba-4f0b-8aee-074bf494147a)

After assembling, cut the protruding leads of the LEDs and Resistors. You can also cut the end of the leads of the buzzer and Push button (one of the Push button may touch the USB connector on your Uno board, so it's necessary to either cut its leads or mask them with some masking tape).

After you finish soldering, upload the game code to your Arduino Uno board, plug-in this shield and... you are ready to play!

### Reference :
1. https://www.tindie.com/products/wokwi/kit-for-simon-style-game-arduino-shield/
2. https://wokwi.com/projects/328451800839488084
