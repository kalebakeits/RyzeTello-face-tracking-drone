# RyzeTello-face-tracking-drone
### Using the djitellopy, openCV and tensor flow to make a face tracking drone in python

#### Requirements (Modules)

1. tensorflow
2. openCV
3. io
4. djitellopy

#### Requirements (Hardware):
1. A Ryze Tello Drone

## Objectives:

- Return bounding box around face
- Classify face as mine or not
- Calculate velocities required to track face
- Send RC controls to the drone [velocities].
 
    
## Improvements:

Improvements made on the original project by Jabrills: https://www.youtube.com/watch?v=esw88_gKOpA

- Auto-land if no face is detected for certain duration of time
- Search for the face to track by panning and moving up and down
- Implement a fail safe key
- Implement face recognition to ignore unwanted faces. Useful when used around other people

    
##### Comments:

- Initially tried to convert pixel values to centimeters which was unecessary and only accurate in the z-axis between 30cm and 150cm
- Thought the face recognition model would be too slow however it performs fast enough
- Used a counter instead of time.time()-kill to determine how long it had been since the last face was detected
      
## Instructions:

*** If you have not set up the facial recognition please do before performing these steps. This can be done using the file "Create Training Data and Train Model.ipynb". The file contains the relevant setup instructions.***
    
1. Start with the Drone Wi-Fi Disconnected (It causes issues when trying to import modules if it's connected)
2. Import the modules
    2.1 (Importing djitellopy before connecting to the drone wifi causes the program to freeze)
3. Connect to the drone Wi-Fi
4. Place the drone on a flat surface that is the same level as your feet.
5. Run all the code up to and including the flight loop
6. To land, spam the Esc key
    - If the landing zone is not safe for landing. Place your hand under the drone
    - If the drone crash lands; it may be necessary to restart the kernel and reset the drone.
    - If the drone lands succesfully; to take off again, simply run the flight loop.
    - Resetting the drone and restarting the kernel should fix all connectivity issues
    
#### Remarks

not_face_detected() is not finished yet.
