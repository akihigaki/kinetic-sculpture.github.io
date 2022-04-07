## Nature in Future: Kinetic Sculpture

[Video of Installation](https://youtu.be/gNKIJsIzILE)

### Artistic Vision

The goal of this project was to recreate a pond setting with our kinetic sculptures. Since this was a group project, we wanted to be able to both work independently and later bring the parts together to form a whole. Therefore, we chose to individually create different entities (such as animals) that would contribute to the theme. We also chose to deepen the theme by introducing the idea of a post-apocolyptic world where people are forced to recreate a natural setting since everything has been destroyed, to give us a clearer motivation.

I chose to create a frog on a lilypad and a waterwheel that uses actual water. Firstly, I wanted to incorporate actual water to bring the electronics, which are inherently far away from a natural form, closer to the idea of a pond. I also liked the idea of making the frog appear and dissapear as the lilypad flipped, and this element was initially intended to be hidden in water before the reveal. These two elements, I thought, were both feasable with the materials given and allowed for creativity in execution.

### Hardware

Firstly, I 3D printed the waterwheel and frog from models that I found on thingiverse. I was also able to learn how to do 2-color 3D printing for the frog for this process. I also 3D printed a little tub to hold the water for the waterwheel. I laser cut a lily pad for the frog to sit on, and glued everything together on the motors (the frog was put on the servo and the waterwheel on the stepper). I also glued the motors to a mounting box to give the elements the height that they need.

### Software

The software is written entirely in the Arduino IDE. The ESP32 connects to the internet, and continually asks an API written [here](https://github.com/mbennett12/kinetic-sculpture-webapi) if the virtual button state is true or false. If true, the frog is flipped over and the waterwheel runs. If false, the frog is flipped to be hidden and the waterwheel stops. This was pretty straightforward after figuring out the internet connection and proper movement of the motors.

The code is located in [this repo](https://github.com/sitongfX/NatureInFuture)

### Technical issues
The biggest technical issue was running the stepper motor. The given libraries for the motor did not work as intended, so I used a code snippet found in the textbook [here](https://drive.google.com/file/d/1GLq7iRY_I1D5Fgma1Rd3yVhNt3dg7K0T/view). I suspect this is becuase the step timing was off, and therefore the motor did not turn properly. Most of the other issues were mechanical and logisitcal, such as getting the waterwheel to fit on the stepper motor's unique axle and getting the 3D prints finished in time.

Hope you like this project!
