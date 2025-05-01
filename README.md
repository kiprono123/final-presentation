# Final-presentation
Final Presentation
Introduction
For this project, we chose to create a robot capable of playing a variety of sounds through a connected speaker. Our goal was to build a simple yet interactive system that could deliver music, sound effects, or pre-recorded voice messages depending on the task or user input. We used a Raspberry Pi as the core of our setup because of its flexibility and ability to run Python scripts efficiently. A standard speaker was connected to the Pi using jumper wires to ensure clear audio output. We wrote Python code to control the playback functions, allowing us to trigger different sounds based on specific commands or events. The code also ensures that the system runs smoothly without delays or crashes. This project not only demonstrated our skills in hardware integration and software development but also gave us hands-on experience with audio processing and real-time control using a Raspberry Pi.

What is Raspberry Pi?
The Raspberry Pi is a low-cost computer with a compact size, about the size of a credit card, that can be connected to a computer monitor or a TV, and used with a standard mouse and keyboard. It is a small computer that runs a Linux operating system and allows people of all ages to explore computing and learn to program in languages like Scratch and Python. It is capable of performing most tasks of a desktop computer, like browsing the internet, playing high-resolution videos, and creating documents.

More importantly for our project, Raspberry Pi can interact with the physical world. This means we can connect things like speakers, sensors, LEDs, and buttons to build interactive systems. Our goal is to show that Raspberry Pi can be used by children and adults all over the world to learn programming and understand how technology works.

How is Raspberry Pi Composed?
GPIO Pins The 40 metal pins on the Raspberry Pi are called GPIO (General Purpose Input/Output) pins. These are used to connect and control hardware like buttons, speakers, or LEDs. In our project, the button sends a signal to the Pi through a GPIO pin, and the Pi then plays a sound throug the speaker.

USB Ports We used a USB port to connect a USB speaker for sound output, though you can also use the audio jack for analog speakers.

USB-C Power Supply This powers the Raspberry Pi. We used a USB-C cable with a wall adapter that supplies 5 volts and at least 2.5 amps.

MicroSD Card Slot The Raspberry Pi doesn’t have built-in storage. Everything runs off the microSD card, including the operating system and our Python code.

HDMI Port We used this to connect the Raspberry Pi to a monitor while writing and testing our code.

3.5mm Audio Jack If you're using analog speakers or headphones, this is where you connect them. For our project, we tested both the audio jack and USB speaker for compatibility.

# Physical Part
[Insert a labeled photo or diagram of your speaker setup with Raspberry Pi, wires, and button.]

![439616558-56f97167-3047-4944-bf1d-cb02476bdaaf](https://github.com/user-attachments/assets/b45de62b-2685-4f7a-8ff1-ec548a863886)


# Programming Part
I’ll walk you through the Python code we wrote for the Raspberry Pi. It plays different sounds from a speaker whenever we activate it. This can be used to make a talking robot, a music player, or a fun soundboard project.

# Importing Libraries
![439494794-84b811a7-627c-49e9-a2f0-d7ac9936e853](https://github.com/user-attachments/assets/8a7d8059-2df7-422f-9995-e89b096bdb80)


We start by importing the RPi.GPIO library to read input from the button. We also import time for delays and os to run commands to play audio files.

GPIO Setup
Στιγμιότυπο οθόνης (91)

We set the pin mode to use the physical layout of the board and define our button pin as an input with a pull-up resistor to detect button presses correctly.

Play Sound Function
Στιγμιότυπο οθόνης (92)

This function plays a .wav file using the aplay command. You can replace the filename with any sound you want.

Main Loop Begins
Στιγμιότυπο οθόνης (93)

This is the loop that keeps checking for the button press. When it detects a press, it plays the sound and waits one second before checking again. If we stop the program using Ctrl+C, it cleans up the pins.

Cleanup on Exit
Στιγμιότυπο οθόνης (94)

This command ensures that all GPIO pins are safely reset when the program ends. It’s good practice to include this to avoid issues in future programs.

References
What is a Raspberry Pi? Raspberry Pi. (2025, March 18). https://raspberrypi.cl/que-es-raspberry/

Timmons-Brown, M. (2019a). Learn robotics with Raspberry Pi: Build and code your own moving, sensing, thinking Robots. No Starch Press, Inc.

Raspberry Pi Documentation. (2025). Playing audio on the Raspberry Pi. https://www.raspberrypi.com/documentation/computers/audio.html

IMG_2306

0 commit comments
Comments
0
