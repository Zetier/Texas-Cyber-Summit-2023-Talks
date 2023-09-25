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

To change the resistor footprint, click on the three books. Were going to associate a footprint to our resistors on the board. 



![image](https://github.com/Zetier/Texas-Cyber-Summit-2023-Talks/assets/142856655/3f7dcdc2-1afe-4b58-a293-4ebafa169c79)













