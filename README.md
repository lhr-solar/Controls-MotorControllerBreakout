# Controls-MotorControllerBreakout
Author: Ravi Shah  

This Power and CAN interface board for the Prohelion WaveSculptor 22 Motor Controller allows for easier debugging by switching between controls and external power sources and providing a plug-and-play CANdapter interface.  

## BOM
IBOM: BOM/ibom.html (download and view in browser)  
Mouser Cart: https://www.mouser.com/ProjectManager/ProjectDetail.aspx?AccessID=de9c48e362

## Connectors


## 3D Model
![image](https://github.com/user-attachments/assets/8b09e65b-588a-480e-ac9f-959f3143bfe2)

## PCB
![image](https://github.com/user-attachments/assets/d9361078-5118-4ade-8f9d-d2d08a0002da)

## Schematic
### Root
![image](https://github.com/user-attachments/assets/13e0b36f-c02d-44f1-99e7-9cbaa624a0fc)
### Power Distribution
![image](https://github.com/user-attachments/assets/62030420-5b30-463f-89ad-ddf332c689fd)
### Power Protection
![image](https://github.com/user-attachments/assets/762b886f-b314-4a23-9416-61d1eb8d6ead)
### LEDs
![image](https://github.com/user-attachments/assets/ae3417af-c8e3-44fd-b922-9fea9e718e8a)

## Application Note
Controls Leader should always be connected to "CTRLS" with the standard CAN+PWR pinout. The motor controller should always be connected to MC CAN 1 and MC CAN 2. To connect external 12V power, the "EXT EN" jumper must be closed. This jumper can be left closed to allow the power muxing IC to choose a source (prioritizing controls), or it can be left open to ignore the external source. In case of a defective IC, the "MNL" jumper can be closed to permanently connect Controls to the output +12V. Otherwise, the "MNL" jumper should be left open.  

+12v is protected by rectifier diodes and fused on both Controls Leader and this board.  

If using a CANdapter for debugging, the "CAN TERM" jumper must be opened. Otherwise, it should be closed, since this board acts as the terminating end for MotorCAN.  
