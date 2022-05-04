# HelicalWiFi: A Helical Antenna for 2.4Ghz Wireless Connections

> ***CMU 18-358 Final Project by Alex Yoon***

# Introduction
The main goal of the project is to establish a wireless internet connection through helical antenna, which produces a circular polarized pattern of RF radiation. A custom designed, stackable form of helical antenna was 3D printed in place of the conventional wireless antenna. 

<p align="center">
  <img src="/assets/helical.jpg" width="500" height="650">
</p>

CAD files (.STLPRT) and 3D Print files (.STL, .3dm) can be downloaded from ***HelicalWiFi/CAD*** folder

# Components/Materials Used
- Nvidia Jetson Xavier AGX
- Intel Dual Band Wireless-AC 8265 Card
- SMA Panel Mount Connector
- 14 Gauge Bare Copper Wire
- 74 Grams of PLA Pilament
- 5" Diameter Circular Tin Plate

# Design Criteria
The engineering design process was completed with the following criterias in mind:
- Antenna must be stackable in order to adjust the number of turns to match the desired gains
- Design must be affordable 3d printable; low pliament consumption and compact size
- Antenna design must be open source

# Design Process
Preliminary design process began with calculating the required dimensions of the desired antenna output. 
Having set the desired center frequency set to 2.45 Ghz (with 4 helical turns and 0.25 wavelength between turns), calculation methods yielded the following results:
- Center Frequency: 2.45 GHz
- Wavelength: 0.12236427 m
- Diameter: 3.89695127 cm
- Expected Gain: 10.8 dBi
- Half Power Bandwith: 52 degrees
- Effective Apperature: 0.01433242 m^2

Displayed below is a preliminary design sketch following the calculation results:
<p align="center">
  <img src="/assets/design.jpg" width="700" height="370">
</p>

CAD model was designed according to the design sketch (single stack component):
<p align="center">
  <img src="/assets/cad.PNG" width="400" height="400">
</p>

Four antenna module was 3D printed using black PLA pilament, and SMA connection was assembled by soldering the mount connector, tin reflector plate, and the bottom end of the antenna together:
<p align="center" width="100%">
    <img width="45%" src="/assets/helical.jpg"> 
    <img width="50%" src="/assets/connection.jpg"> 
</p>

# Testing


# Comments
if needed
