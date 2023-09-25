# OMG Demonseed clones

The OMG Demonseed is an opensource project located [here](https://github.com/O-MG/DemonSeed). It has narratives on youtube [here](https://youtu.be/QQ1p2tPWZbM?feature=shared) and can be used as an RF triggerable usb implant. It is not even close to having the features of the OMG cable but for a beginner project will suffice. It is very simple and easy to build in kicad. The reason this device was chosen was because: it is expensive compared to the components it is made of, it is regularly out of stock, it is easy and cheap to DIY, and the git could be taken down at some point. Having the knoweldge of how to build this tool can allow reproduction of it. Plus, its super darn cool. 
# 1) Install Kicad
Kicad can be found [here](https://www.kicad.org/). Debian is sudo apt install kicad or arch sudo pacman -Syu kicad. 
# 2) Open Kicad 
Open a new instance of Kicad. It should look like this the first time you run it. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/72c0b381-5a63-4485-9dd1-c28d0649b73e)

# 3) Making a new project
To use kicad, a user needs to create a new project. Click file/new project and enter a project name. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/fde9bf10-916a-4b0d-9e55-d0ff2a904fbb)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/6296206b-4de1-43cc-90a0-1056e478ed64)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/7cec8029-c84b-4a42-9f06-75c8727ca9a9)

A new project should now appear in the left file navigator. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/d4d01bac-1769-4fd0-a6cc-8e0dbac99658)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/72c0b381-5a63-4485-9dd1-c28d0649b73e)

# 4) Jump into new schematic

To open the schematic viewer, simply click on the schematic file. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/88dbe346-e417-4bbc-b6bb-9e7ee34413b8)

# 5) Familirization with schematic editor

This is a screenshot of some of the tools used. The naming convention and location of these will be used for the rest of the readme. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/c655a0ba-e984-44b7-be20-bdcae6b3b130)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/1cb9c149-0dc4-40c4-a513-297b09bfe34e)

# 6) Copying the schematic

In Kicad, it is fairly simple to reverse and clone another schematic. Just drop and place components, edit their values, add a footprint and connect them. Below is the schematic being cloned. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/35d16cbf-4326-4617-a097-66cf5db3fbef)

To search for components, click on the symbol browser. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/99b7ec5a-ad21-4c55-9289-b6f6f35a851d)

A table like this will pop up. This is where one can search for a particular part that they want in their circuit. In this case searched is the microcontroller, the ATTINY85-20M. After double clicking it should be placed. Click it on the schematic and escape to deselect it and free your mouse

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/1a8d5b2c-639f-4bc8-9008-2dc55cc7812f)

Your schematic should now look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/82b9de1e-7178-412c-a1f2-81121649c7d6)

Placing the USB connector (and every other component) is just as easy. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/55de0e2b-01db-4556-a6dc-50eaa95430c5)

Schematic should now look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/a3a74b15-ee26-4612-9165-f53e9c141e4d)

The issue is the USB connector is facing the wrong way. To spin it around, select it and hit the R key. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/a3bd9726-ed11-42a2-ab4d-935554562bd5)

There, thats better. Now for both of these parts a "footprint" needs to be associated with them. Every component we place needs a footprint. The associated footprint will be what the PCB manufacturer will use to expose connections to solder to. If you dont associate footprints to your symbols, your PCB will surely not work (or at least later in this tutorial it will be much more work).

To associate footprints, double click on the symbol. This will bring up a table with all of the attributes of the symbol and allow you to edit it. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/34098cb4-556b-4c9c-9c03-029334a81fcf)

In this case, the ATTiny is selected. There should be a book in the footprint bar. Click it. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/4e328acd-62b3-4aeb-b370-d8a584cff762)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/135b9634-1275-4d08-8bed-02817723093f)

In this case, the footprint is correct for the part selected. You can exit out and go back to the schematic view. 

The USB footprint has to be changed. Double click on the USB symbol and open the footprint browser. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/950258c0-f90a-4e51-8fa7-cfc7575c6801)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/40d66ed6-a82d-4289-8c53-db0d74115af3)

Last large component in this circuit is the programming header. The "pad and pogopin" layout is just a bit much for me. Plus it is more expensive. Putting in a 1.0mm pitch (seperation) header will be cheap, slim, and easy. Wires can also just be soldered to this or custom headers can be used. For referenece this is what a 1.0 mm header looks like: 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/00ccc047-ae8c-4224-a872-7411b2876d0c)

To place the symbol, go to the browser and search for connector_generic in the libraries and search for 2x06 in the symbols search. Pick the odd even one. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/88992c96-b9da-4884-b1d9-7f0dd8a949f4)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/bb58e14c-5593-4217-94b1-f496b2221acd)

Schematic should now look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/1f4f9022-c272-4eab-915f-991a6591410b)

Time to choose a footprint.

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/ac4de1ff-f14f-49b1-848d-bb2e4d89ea48)

Search for a footprint. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/d0836ac1-c2f1-4c0f-8012-68d4435bfca6)

Great! Now that the main components are specified, we have 3 things left with the schematic: create nets and route wires, place electrical symbols, and place electrical compontents. For the rest of this tutorial use the devices and power symbols respectively. 

To place the electrical components, browse the symbols libraries for devices and search for "R". 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/88992c96-b9da-4884-b1d9-7f0dd8a949f4)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/7fe2674d-732c-4bdf-a167-8241728506d8)

To change the resistor footprint, click on the three books. Were going to associate a footprint to our resistors on the board. In this case, I am choosing a 0805 due to cost and ease of soldering. 1206 is a little big and 0603 requires tweezers. 0805 is a size meaning .08 by .05 inches. 0805 is a generically recommended size for all. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/ac4de1ff-f14f-49b1-848d-bb2e4d89ea48)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/3f7dcdc2-1afe-4b58-a293-4ebafa169c79)

The schematic should now look something like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/b34632cb-fe26-4937-b02f-66b0adfaf016)

To copy simply select a component until it highlights blue and right click copy, paste or ctrl+c, ctrl+v. Copy the resistor 2 times to match the schematic that is being cloned. 
My schematic:

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/44b03504-129c-40b9-9993-c69c92cbab98)

Demonseed Schematic:

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/be488ebd-c988-4111-b5de-01ea11a712d9)

They are looking quite similar. Time to add values to match the resistor values. To do this, double click on a resistor and change the value tab to match the number from the OMG demonseed value. There are 2 68 ohm resistors and a 1.5k resistor. All of them are for the USB connection. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/dad8a894-5f68-4daf-b90b-4e0a7503e714)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/5faacee3-beab-4525-b426-3e8be7ad25f9)

Repeat this process for the other 2 resistors. Your schematic should look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/4c018b6d-6ffa-4337-a62b-4b479a0720bd)

To place diodes, it is a very similar process. There are 2. Select the browser and search the devices library for a "D". 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/88992c96-b9da-4884-b1d9-7f0dd8a949f4)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/b5914c6a-9454-409d-8803-1db8c57cc988)

The schematic should now look like this. Time to add the associated footprint to the diode. Very similar to resistors and same size. 0805. Search this in the footprint browser for the diodes.

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/fb1e2dc8-8f55-49e3-993c-3054e8cd468d)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/ac4de1ff-f14f-49b1-848d-bb2e4d89ea48)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/d159b049-319b-4de2-b583-336a337be495)


Copy the diode and rotate the copied one 180 degrees to match the demonseed schematic. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/85484901-92e9-483e-85b8-a1119cc1eb48)

Now just edit the associated values to match that of the demonseed schematic. In this case, both are 3.6v.

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/38d4c00e-be88-4c47-ba43-6dfceb4289ac)

The schematic should now look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/3b65bcf5-7c3c-420c-8c8e-074bfc7047cc)

Cool, so we only have 2 things left. Create nets and wire connections and placing our power and ground. Pretty simple. 

Routing power is just copying the symbols from the OMG demonseed schematic. Search for the power library in the symbol browser and search for GND. Place one on the schematic connecting to the ATTiny GND pin on pin 8. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/88992c96-b9da-4884-b1d9-7f0dd8a949f4)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/d55abfd7-28de-4dd4-80cd-20692e7ded7c)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/73a265c9-6dbe-4298-81b9-4572f5979939)

Copy and paste the ground to the diodes and the USB ground. The schematic should now look like this (also saw the diodes had "zenier" in them and made an edit to the value as this is a certian type of diode). 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/207df24b-1cbf-43d1-9f28-b578b1115a59)

The circuit now needs 5v from the USB port. USB produces 5V. The schematic has a 5V on the USB connection, the ATTiny, and the 1.5K resistor. To place, search the symbol browser libraries for power and the symbols for 5V. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/88992c96-b9da-4884-b1d9-7f0dd8a949f4)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/daa1cb72-4d6f-409a-8592-e48d99ff169f)

Add the 5V to the USB, ATTiny, and 1.5K resistor. VCC and VBUS are both power pins on the USB and ATTiny. The schematic should look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/a35c8508-f6f0-4ead-9f3b-debe7d70af12)

Now that power and gnd is placed, wires and connections have to be made between the components. To do this simply click the add a wire button, click the circle on a component or hit W on the keyboard. Route the wires to connect exactily like the OMG demonseed. Here is mine post routing. (edited the ground on usb pin as well to be connected to shield in this step)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/a2016c6f-6e3f-4ecc-af87-ab49dc98a819)

Very last thing to do is to create our header connection. I found that it was much quicker to just scratch some of the wires around and connect them to the header directly. MAKE SURE YOU DO NOT HAVE ANY GREEN CIRCLES IN UNINTENDED LOCATIONS. These signify a connection and will short. To avoid this, go around thing and use excess wire. Your schematic should now look something like this. Refer to the OMG demonseed schematic for programming lines (mosi miso sck rst). 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/3a32c7b2-ee03-4faa-b55a-3074bae0f2db)

Too easy. On to the PCB. To change to the PCB, click the PCB button and import all of the footprints with the import button. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/dbfef457-06a1-45a5-91da-d7a7f015c387)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/a536cca9-eb2b-455a-88ad-14a63340b2e1)

After updating the schematic, there should now be a blob of red, lines, and colors. Those are the footprints that were specified earlier. simply click somewhere in the middle of the template and hit escape. It should look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/49b2b5eb-757f-470e-8f45-e3e7dcdab2d1)

This is a 2 layer board. Pretend it is a piece of paper. Both sides can be drawn on but it needs to be specified. To move a component to the back side, select it, and hit the F key. The component should show up blue (on the other side). Flip all 3 of your resistors and the USB connector. It should look like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/73eee35b-f576-4ac3-944a-62da02aa05f4)

Now we have to rearrange the components to start connecting them with traces. This is how I did mine. It was to conserve space and maintain good trace widths. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/d201488d-9c40-437c-b13f-bcf1d0035c83)

Now connect everything using the x key. Connect everything that has a "silky" white line. These are the nets and connections we made in the schematic editor and they must be connected to make the board work properly. Remember you have 2 layers. To route through the layers use a VIA. Here is an example of a trace I made going from the back of the board to the front through a VIA. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/8f33eee0-c743-403d-8157-2f068de6ee41)

After routing all silky lines and no lines are left you should have a board that looks something like this. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/c609aa9c-21a7-4e0b-9d58-e0065e41f157)

Lastly edge cuts need to be made. This is the final edit to the PCB before exporting it. The edge cuts define how large the PCB will be. Select the Edge.cuts layer in the layer browser and the draw a rectangle from the toolbar. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/f874ef91-4199-43bc-874f-d718e76029b0)

Click to start a rectangle and drag around the perimeter of the PCB. You want to get as close into the parts as you can without pushing them off. This is what mine looked like. 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/3ea7d252-20b0-47f0-a0eb-39dd819f6856)

It has a bit of a different shape than the OMG demonseed, however can be put in a USB case and will fit with ease. If you are looking for a certian form factor, moving the components around may help. 

To actually make this board it needs to be exported, zipped, and uploaded to a fabrication house. Osh park is a US based company with a great reputation. I will upload it to there. Here is how to do it. 

First export your files as gerbers.

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/bd545c6f-7f9c-4e22-bcd6-c8cc28baa2c0)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/7b8e8f71-2060-4ed2-b066-59326a19b0e7)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/311dab3d-4f72-441f-b3c8-5019150bf06a)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/62bf769e-311b-49f5-9429-f7cb57aa6799)

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/78276312-a4e8-4805-8c36-2d1bf56d9bbf)

Now zip the output directory up. On linux use terminal zip command. Windows navigate to the output dir and send to zip file. 

Upload this to [Oshpark](https://oshpark.com/). It should give you a price and you can order this. To get the components, rever to the BOM on the OMG demonseed git at the top. In this case it was $2.20 for 3 (not including shipping). 

![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/3a36a2ea-e7e0-4dd5-9c91-a00f031a3183)


And thats it! You now have created a clone from reverse engineering a tool!









