# GPIO outputs
------------
## Dependencies.
To run the application, you will need:
- WiringPi<br/>

If you have the Buster OS, you have WiringPi by default.<br>
If you have Bullseye, install WiringPi with the following commands.<br>
```
$git clone https://github.com/WiringPi/WiringPi.git
$ cd WiringPi
$ ./build
```
------------

## Run the app.
To extract and run the app in Code::Blocks, as described in the main section.<br/><br>
Once everything is working, replace `FaceMask.cpp` with `FaceMaskGPIO.cpp`<br>
and `TensorFlow_Lite_Mask.cbp` with `TensorFlow_Lite_Mask_GPIO.cbp` in the root directory.<br><br>
The app looks the same. The only difference is the additional GPIO output.<br>
The outcome of the first face found (mask, no mask, wrong worn) sets predefined output pins.<br>
Possible other faces are ignored.<br><br>
In line 17, you can define the output pins. The numbers refer to the WiringPi. See the diagram below.
```
#define PIN_MASK 7
#define PIN_NO_MASK 0
#define PIN_WRONG_WEAR 2
```
------------------

## PIN numbers.
Find the correct WiringPi pin numbers in the diagram below.<br/>
![output image]( https://qengineering.eu/images/WiringPi.webp )

------------

[![paypal](https://qengineering.eu/images/TipJarSmall4.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CPZTM5BB3FCYL) 
