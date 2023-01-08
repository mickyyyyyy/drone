# Propellers

## Overview ##
This folder contains propeller designs for the propulsion subsystem for the drone. 

## Design Process ##

### Basic/ Angled Propeller ###

#### The Hub ####
The most basic model for a propeller includes a hub in the centre for coupling with the motor which drives rotation of the propeller, and thus, thrust of the drone. Since the hub will be connected to the motor via a shaft (whether that be direct driven or using gears), the centre hub was designed as circular, with a inner radius of 5 mm and an outer radius of 15 mm (dimensions chosen as estimates at this stage, and may be subject to change based on other design factors for the drone). The width of the hub was made to be 10 mm (again, as a starting value), and was modelled as shown below:  

![image](https://user-images.githubusercontent.com/62014208/210196330-63077bf6-44d2-4a2d-8aea-9e887278a585.png)

#### The Blades ####
A sketch was then made of the outline of the propeller on a work plane which was tangential to the outer face of the hub. This sketch was then projected onto the outer face of the hub, and extruded out to create a simple, angled blade. Once this singular blade had been created, a circular pattern of the blade was created, around the centre of the hub. With some filletting of sharp edges for ease of handling, a reduction in stress concentration, and to reduce the drag of the propeller while in operation, the preliminary design for the basic, angled propeller was complete. This model looks as follows:  

![image](https://user-images.githubusercontent.com/62014208/210198481-a9502eab-a1e2-41fe-83b3-d2f91f2468cc.png)

#### Stress Analysis ####

##### Static #####
A static stress analysis on the propeller was conducted to verify that the propeller can withstand the weight of the drone (expecting four propellers with ~20 kg of weight for the drone in total so ~5 kg on each propeller). This stress analysis yields the following results:  

![stress](https://user-images.githubusercontent.com/62014208/211175454-a6818e53-1308-4b4d-98d3-042c7ef0a5ce.PNG)
![stress_1](https://user-images.githubusercontent.com/62014208/211175455-b18be9f4-c324-46e0-a148-0800c354a0ba.PNG)

Where the highest stress concentrates on the filleted edge of the fixed side of the hub. However, even the highest stress through the propeller is significantly less than the yield strength of ABS plastic (the material I would use if 3D printed ~13-65 MPa). The deformation of the propeller during this static stress analysis is shown below:  

![displacement](https://user-images.githubusercontent.com/62014208/211175997-ff196cf2-f747-4291-b168-1833cdae229c.PNG)
![displacement_1](https://user-images.githubusercontent.com/62014208/211175990-7baaa3c8-a583-4ff4-9611-377ed3723e7b.PNG)

Where the max displacement is at the face of the non-fixed side of the hub, which is signficantly less than the total width of the hub (10 mm).

## Progress ##
The current progress for the propellers includes:  
  
- [x] A basic angled propeller design.  
- [x] A curved propeller design.  

## Future Additions ##
In terms of future additions, we aim to:  

- [ ] Complete static and modal stress analyses on the basic angled propeller design based on expected load.
- [ ] Complete static and modal stress analyses on the curved propeller design based on expected loads.
- [ ] Complete a Finite Element Analysis (FEA) on the basic angled propeller design based on expected loads.
- [ ] Complete an FEA on the curved propeller design based on expected loads.
- [ ] Adjust the design based on fixed parameters (i.e. standard sized shafts etc.)

## Viewing the model ##
In order to view the desired version of propeller, open the folder, and the latest version `.ipt` file in Autodesk Inventor.
