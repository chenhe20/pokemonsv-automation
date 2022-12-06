# Pokemon Scarlet and Violet Automation Copy Bug Scripts

A fork of an auto breeder script that was developed for pokemon sword and sheild. The automation exploits the 'copy bug' that exisits in pokemon scarlet and violet of version 1.0.0 and automates the process of copying any item for hundreds of times. e.g., One can copy and paste 999 master balls. 

## Setup Instructions for an Arduino R3: 
1. Download the LUFA library here ([LUFA DOWNLOAD](http://www.fourwalledcubicle.com/LUFA.php)) and extract it's contents in the LUFA folder of the project

2. Install packages needed for flashing the Arduino
    - For Windows: *TBD*
    - For Linux / Mac: 
    ```
    brew install dfu-programmer 
    brew tap osx-cross/avr
    brew install avr-gcc     
    ```
3. Set the Arduino into DFU mode: 
    - https://www.arduino.cc/en/Hacking/DFUProgramming8U2 


4. In terminal navigate to the inside of the project directory 

5. Make the file in terminal enter: make

6. Flash the arduino with the code by entering the following commands in terminal. 

```
sudo dfu-programmer atmega16u2 erase
sudo dfu-programmer atmega16u2 flash Arduino-usbserial-uno.hex
sudo dfu-programmer atmega16u2 reset
```

7. In-game preparation, see https://www.bilibili.com/video/BV1a24y1y7Bs/?spm_id_from=333.337.search-card.all.clicvd_source=1f6c9642bb9e80aaa4aa9c50510f3e97 to know how this bug works.
Make sure that you have put Koradion/Miradion at the last postion of your following pokemons with the item you are going to copy, put the cursor over it, ensure that your pokemon box is on the first page. The copy process would repeat 300 hundreds times as per the design.

8. Plug in the Arduino into the switch. This can be done through either a USB-C cable (needs testing) or by plugging the arduino directly into the dock. The arduino would perfrom as a controller that specially designed for this copy bug.

#### Notice
Sometimes the game would lag and therefore load for a bit longer than expected between two inputs, which results in the chaostic input from the controller.
It is suggested that you take a look at the screen from time to time and save the game before a possible error. Meanwhile, I will adjust the time interval between every two inputs to improve the program stability whilst maintain the efficiency.

#### Thanks

Thanks to https://github.com/taingmat/pokemonss-autobreeder, this script is fully based on this project and I also refers to the great effort made by other authors that mentioned by taingmat.

