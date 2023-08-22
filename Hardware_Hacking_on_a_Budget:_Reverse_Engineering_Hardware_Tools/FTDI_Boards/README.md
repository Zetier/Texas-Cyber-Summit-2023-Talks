# FTDI Adapter Boards

This directory contains all relavent information for the FTDI boards for TXCYSUMMIT23. 

### Step 1

Order all relavent parts and equipment from your store of choice. The parts required for this list are in the BOM (bill of materials) that is in this directory. You can search for these parts wherever you like, or try to find them in some junk components you have lying around. You will also need solder, and a solder iron. This will cost a one time fee and does not count against you for the purposes of the beatme price. All of the component placement is labeled in the BOM file as well, where the component should go on the board. For example, I order the 5V led. I need 3 of those and they are placed in D1, D2, and D3 as marked on the PCB. Below is an image of all the parts you will need. They should look somewhat similar to this. 

![DSC03863](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/3089e65d-8c1e-4637-8c1d-dd423cbcf68c)


### Step 2

After getting all relavent parts and tools, you can start building your board. Make sure you tack down pin one correctly to the pin one notated on the board. The pin 1 is signified by a divet in the FTDI chip and a long white line over the pin stencil on the board. 

![DSC03882](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/d50111c7-63b3-4961-a305-f9a06937ab94)

Great, now make sure you dont have any pins soldered together (bridged). If you do, grab some copper wire that you may have laying around (can be small, large, an old charging cable) and strip some of the wire away. Then heat up the area with too much solder and dip in the copper wire. It will start to remove the excess solder. If no copper wire is available, you can use the tip of the solder iron and a wet sponge to clean up the area. To do this, heat up the area and get some of the solder to stick to the solder iron. Then wipe it off with a sponge and repeat until all solder is removed. This is a much slower process but works in a pinch. If you are feeling like a pro, you can order some solder wick as well which will act like a sponge for solder and will pick up excess much easier when heated in the area with excess. 

### Step 3

Start placing the components on the board. Diodes and tantlum capacitors are not bidirectional, meaning that electricity can only flow in one direction. These components have a bracket around them in the white silkscreen signifying what direction electricity flows in. Here is a tantlum capacitor I soldered down. The flow of electricity is toward the white line that is placed on it. There is a white silk screen on the board that when lined up, will allow the circuit to be completed properly. 

![Screenshot_2023-08-22_00-18-23](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/0b51b70c-44d7-456d-a102-cad3004727f5)

LED's flow in the direction of green. In most cases the pin that lines up with the silkscreen is green. There are other simbols out there. Here is a link that covers a lot of components https://www.pcbonline.com/blog/smd-polarity-led-capacitor-diode-inductor-ic.html. In my board if you line up the out flow of electricity with the white silkscreen, the component will work. 

### Step 4

After placing the components on their respective place, you can put the headers on the board. These are very easy to put on. Simply shorten to size, put them in the holes on the board, and solder them down. Here is an image. 

![DSC03898](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/c889eaee-3048-491b-a539-2c75fb73f0b5)


### Step 5 - Optional

Place a little bit of solder on the USB pins. Make them bigger. It helps with the connection. This is not mandatory but helps with the board connecting to your usb ports. 

### Step 6

Now find a uart port on hardware. This is fairly simple. If your tool lights up when you plug it in, you will be able to connect to a piece of hardware and communicate with it (if the UART is not locked down). 




