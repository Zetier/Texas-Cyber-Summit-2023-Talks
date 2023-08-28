# FTDI Adapter Boards

This directory contains all relavent information for the FTDI boards for TXCYSUMMIT23. If you would like to fab one yourself, the attached gerber files are in the zip folder. 

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

Place a little bit of solder on the USB pins. Make them bigger. It helps with the connection. This is not mandatory but helps with the board connecting to your usb ports. During step 5, you can also go through the diodes with a multimeter to make sure they are facing the same way. 

![DSC03951](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/63ba30bb-5287-4683-bf4d-9857ad3052a9)

### Step 6

Now that everything is assembled and checked, plug it in! Some of the LED's will light up. If you are using windows it should enumerate as a ft232rl, if linux, type 'lsusb' and if everything is assembled correctly it should show up on your terminal. 

![DSC03953](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/58bd099a-170a-4bbb-905d-62ac7864b71f)
![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/ac181349-9d95-4b96-ae92-930cbf8c057c)



### Step 7

Now find a uart header on hardware. This is fairly simple as you are looking for 2,3,or 4 holes/pads on an electronic. Here is a link on how to find a UART and if unlocked, get a shell. You may need a few dupont wires for this part or you can use whatever wire or cables you have around the house. 
Dupont wires: https://www.amazon.com/ELEGOO-Breadbord-Jumper-Wires/dp/B0B2W22XHB
Youtube: https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjHuOqfjoCBAxXBlGoFHYlgCDwQz40FegQIDRAz&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DZmZuKA-Rst0&usg=AOvVaw0cxxeIhTwcsS4VcE5sFbwF&opi=89978449

### Step 8

Post! We want to hear about your adventure! Tell us about your experience at the conference and how easy or hard it was for you to put together the FT232 board! #Zetier, dm, tag, or email us on our website at www.zetier.com!




