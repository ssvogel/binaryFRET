# binaryFRET
Software to implement binaryFRET
Software descriptions:
1.	LabView (FPFA v4.vi): The LabView (LV) software tool was developed to communicate with
•	ProScan III Controller (Prior Scientific): the controller is responsible for movement of HLD117 XY scanning stage, which is used to laterally position a sample on top of the microscope objective.
•	MFC1 Motorized Microscope Focus Controller (Thorlabs): to vertically position a sample along the z direction.
•	SC10 Optical Beam Shutter Controller (Thorlabs): this controller control SH1 Optical Shutter SH1 (Thorlabs) that opens/blocks excitation beam.
•	SPC-130EM card (Becker and Hickl): the LV uses the SC10 to send a TTL signal to the SCP card to initiate data acquisition. The acquisition time was set as a parameter of the SCP card.
•	The LV tool also serves as timer for the time-lapse binary-FRET experiments.
•	The LV tool uses LabView drives and libraries (.llb) developed by Prior Scientific, Thorlabs and Becker & Hickl. 

2.	Igor (Homo and Hetero-FRET fifo.pxp):
•	Data acquired by SPC-130EM card was saved in hard drive of a PC. For time-lapse binary-FRET, individual measurement was saved as single .sdt file which contains micro-time (and macro-time) of photons detected for both parallel and perpendicular channels. Each .sdt file was converted into a single ASCII .asc file by SPCM software (Becker and Hickl). 
•	The Igor routine was developed to read the micro-time data from multiple ASCII files and correspondingly perform calculations of lifetime and steady state anisotropy.
•	The calculated lifetime and steady state anisotropy were transferred to Prism 8 (Graph Pad) for graphs and statistical calculations.

