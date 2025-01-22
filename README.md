# Controls-MotorControllerBreakout
Power and CAN interface board for the Prohelion WaveSculptor 22 Motor Controller

## Detailed Description
This board allows for easier debugging of the WaveSculptor motor controller by switching between controls and external power sources and providing a plug-and-play CANdapter interface.  

Controls Leader should always be connected to "CTRLS" with the standard CAN+PWR pinout. The motor controller should always be connected to MC CAN 1 and MC CAN 2. To connect external 12V power, the "EXT EN" jumper must be closed. This jumper can be left closed to allow the power muxing IC to choose a source (prioritizing controls), or it can be left open to ignore the external source. In case of a defective IC, the "MNL" jumper can be closed to permanently connect Controls to the output +12V. Otherwise, the "MNL" jumper should be left open.  

+12v is protected by rectifier diodes and fused on both Controls Leader and this board.  

If using a CANdapter for debugging, the "CAN TERM" jumper must be opened. Otherwise, it should be closed, since this board acts as the terminating end for MotorCAN.  

Mouser Cart: https://www.mouser.com/ProjectManager/ProjectDetail.aspx?AccessID=de9c48e362


