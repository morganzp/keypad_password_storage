# keypad_password_storage
ECE_387_MIDTERM_CODE
 Code for Unlocking Door with Keypad and Servo Motor

This code  initializes a 16 digit keypad and a servo motor to work with
an Arduino. It utilizes two libraries, 'keypad' and 'servo'. Most of the
variables are described in the codes comments. Three different arrays
are used for the hardcoded password, the user attempted password, and
the boolean array that compares each element of those two arrays to
determine whether the right code was entered or not.  In the setup loop,
the servo is initially set to 90 degrees which is in the locked
position.  In the loop the function 'getKey' is the function used to
retrieve the char value of the key that was pressed on the keypad. The
function 'waitForKey' blocks all code until a key is pressed and then
this value is saved in one of the arrays. Every time a button is
pressed, a yellow indicator light blinks to let the user know that the
button press was indeed received.  This repeats until you have entered
four different buttons. The following for loop compares the user input
to the actual password, and then sets another array full of boolean true
or false depending on if the passwords match. If they do match,  a green
LED indicator will glow and the servo will be called. If the password
was entered incorrectly, then a red LED indicator will tell you the
password was incorrect. When the servo motor is called,  the green LED
indicator stays on and the servo rotates a degree at a time until it
reaches 180 degrees. It stays in this unlocked state for 5 seconds and
then the red LED indicator glows and the servo locks again, going from
180 degrees to 90 degrees. Below are the references in which i consulted
to find information on the keyPad and Servo libraries. 

REFERENCES:
- Stanley, Mark, and Alexander Brevig. "KeyPad Library." Arduino Playground. N.p., n.d. Web. 5 Mar. 2016.
- "The Software Servo Library." Arduino Playground. N.p., n.d. Web. 4 Mar. 2016. 
