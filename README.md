# RPi-4-Controlled-LED-Strip
temp description

![image](https://user-images.githubusercontent.com/74937113/127747990-f5af8919-117f-45d0-a010-d92b1c852c86.png)
![image](https://user-images.githubusercontent.com/74937113/127747995-ac070880-3bbf-44c6-96cb-2ae1cb0dcf19.png)


<img src= "https://user-images.githubusercontent.com/74937113/127747984-0e311f78-2eeb-4e58-b2d7-6c08996a7809.png" width="200" height="100">


NAME

Raspberry Pi Controlled LED Strips

DESCRIPTION

This was a project that I made to apply basic concepts that I had learned from courses. I was also inspired to work on this project, as I felt that it would combine hardware and software concepts together quite well. 

CIRCUITRY

The main focus of this project was to practice using breadboards, wiring diagrams, and transistors to create something functional. I spent a lot of time reseraching parts and their specific uses, with the MOSFET intruiging me the most. While it would have been simple enough to put the circuit together and call it a day, I wanted to understand each segment of what I was doing.

Core tools used:
- Wires
- Breadboard
- 12V female power jack
- RFP30N06LE 30A 60V N-Channel Power Mosfet 
- General LED Strips
- Raspberry Pi 4

MOSFET

These metal–oxide–semiconductor field-effect transistors have the ability to control power between the Drain & Source terminals. In a MOSFET, there are three pins;  Source, Gate, and Drain. This is the most basic way that I've come to understand these transistors: Essentially acting as a switch, when a certain voltage is applied to the Gate, current will be free to flow between the Source and Drain.

There are two main types of transistors, which are p-type or n-type. This is a concept that I was able to explore in my Physics 1E03 course, 	
"Introduction to Electromagnetism and Waves" as well as the in the Engineer 1P13 course's "Material Science" subject. The primary concept of these transistors are the usage of doped hole regions. An p-type requires a negative voltage at the gate while the n-type uses a positive voltage. Based on this, I chose to use an n-type as the GPIO of a RPi 4 produces a positive voltage at the pins.

If you're interested, here's my in-depth explaination of these devices:
As mentioned the components of a MOSFET are three pins and a Body. Under the Source and Drain, there are n+ doped regions. Beneath the Gate is an oxide later. These are all situated in a depletion region, often called the Body.
When a positive (+) voltage builds up at the gate, electrons (-) are naturally attracted to this. An n-channel "tunnel" is formed between the two n+ doped regions. This channel is filled with electrons, and so current can flow from the Source --> Drain. 
When there is no voltage applied to the Gate, the two n+ regions are seperated and no current can flow. The higher the voltage applied to the Gate, the better the tunnel - more current can flow.

This tool is tremendously useful in modern electronics! And the best part is, these work without other electronics having to sense current, move tiny gates etc. It uses basic physics & material properties.

USAGE

Currently, this project is used to highlight hardware concepts. 

CHALLENGES

There were actually quite a few challenges I encountered in this project despite the simple nature of it. 

Power: 
Originally, my plan was to simply connect the LED strips to the RPi 4 GPIO pins directly. When I attempted this, the lights simply did not work. I took this as a learning experience, and recognized that the output of an RPi is only 5V, while the LED's required 12V. From this, I had to figure out a method to still control the LED lights while providing the necessary power. After some research, I learned that many online community projects were done in a similar fashion using transisters. MOSFETS allowed you to control the applied voltage from an external source, which worked perfectly for this situation.

Fried:
Long story short, I ended up having to purchase a new RPi 4. In order to work on another project, I disassembled the contents on the breadboard. After reassembly, I had swapped the gate and drain wires. This proved to be catastrophic, as it meant that the 12V from the DC power source was going into the RPi. This quite literally killed my RPi and I had to get a new one.
While it was an unfortunate event, I've learned to be more cautious when dealing with microcontrollers and power. 


ATTACHED

