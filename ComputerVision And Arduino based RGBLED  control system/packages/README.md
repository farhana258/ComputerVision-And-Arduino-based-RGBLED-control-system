Controlling RGB LED with Computer Vision and Arduino
This is a straightforward project involving Arduino and Python to control an RGB LED light using computer vision, specifically by tracking the distance between the index and thumb fingers in pixels.

The RGB LED's color changes based on the calculated distance between the index and thumb fingers, which is defined with fixed values in the code. You can easily adjust these values to suit your specific requirements.

The Python code communicates with the Arduino by sending arrays via serial communication. Here's how the array values correspond to LED colors:

[0, 0, 0]: Turns off the RGB LEDs.
[1, 0, 0]: Sets the RGB LEDs to red.
[0, 1, 0]: Sets the RGB LEDs to green.
[0, 0, 1]: Sets the RGB LEDs to blue.
You can also customize the code to achieve additional colors like yellow, magenta, and cyan:

[1, 1, 0]: Sets the RGB LEDs to yellow.
[1, 0, 1]: Sets the RGB LEDs to magenta.
[0, 1, 1]: Sets the RGB LEDs to cyan.
To make this project work, follow these steps and guidelines:

Python Setup:
Install the required Python libraries:

Install MediaPipe: pip install mediapipe
Install OpenCV: pip install opencv-python
Install CVZone: pip install cvzone
Use the provided Python code for your project.

Arduino Setup:
Install the CVZone package for Arduino. You'll find the CVZone package inside a ZIP file in the "packages" folder of this repository.

Download the CVZone ZIP file from the "packages" folder.
In your Arduino IDE, navigate to "Sketch > Include Library > Add Library from .ZIP file."
Select the downloaded CVZone ZIP file.
Now you can use the CVZone module in your Arduino code with #include <cvzone.h>, and it will enable you to receive serial inputs from the Python code.
Copy the provided .ino file from this repository and load it into your Arduino IDE.

Project Execution:
Compile and upload the Arduino code to your Arduino board.

Start the Python code by pressing F5 or CTRL+F5.

It's essential to follow these steps in the exact order described. If you initiate the Python code first and then load the Arduino code afterward, you might encounter an error in the Arduino IDE because Python would lock the port designated for serial communication between the Arduino and your PC.

If you've followed the correct sequence (load Arduino code first, then start Python code), you should see a window on your computer screen displaying the hand tracking feature in action.

If you move your index and thumb fingers, but the RGB LED lights do not change, try pressing the reset button on your Arduino board and then attempt again.
