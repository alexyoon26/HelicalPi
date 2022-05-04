# HelicalWiFi: A Helical Antenna for 2.4Ghz Wireless Connections

> ***CMU 18-358 Final Project by Alex Yoon***

# Introduction
The main goal of the project is to establish a wireless internet connection through helical antenna, which produces a circular polarized pattern of RF radiation. A custom designed, stackable form of helical antenna was 3D printed in place of the conventional wireless antenna. 

<p align="center">
  <img src="/assets/helical.jpg" width="500" height="650">
</p>

CAD files (.STLPRT) and 3D Print files (.STL, .3dm) are available for download at ***alexyoon26/HelicalWiFi/CAD***

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
Testing of the helical antenna was conducted using a portable network analyzer rated 11 GHz and a Jetson Xavier AGX with a M.2 Wireless Card installed. The network analyzer was calibrated then displayed the Standing Wave Ratio (SWR) and the S-Parameter of the helical antenna.

***SWR Graph Display (left) and S-Parameter Graph Display (right):***
<p align="center" width="100%">
    <img width="45%" src="/assets/SWR.jpg"> 
    <img width="47%" src="/assets/s11.jpg"> 
</p>

The network analyzer results show that helical antenna is centered around ***2.6GHz***, rather than the desired 2.4GHz range. It has also shown a SWR of 1.229 and antenna gain of 20 dBi. Possible explanations for such result are:
- Effect of material of the 3D printed component (PLA)
- Difference in actual diameter of the Helix due to wire deformation
- Difference in actual diameter of the Helix due to design fault

Further testing was done by connecting the antenna to the Jetson's AC8265 Wireless Card, then performing an online network speed test. Speed test was performed on https://www.speedtest.net/ and the result was compared with stock and no antenna installed.

***Helical Antenna:***
<p align="center" width="100%">
    <img width="45%" src="/assets/helicpic.jpg"> 
    <img width="47%" src="/assets/helicspeed.PNG"> 
</p>

***Stock Antenna:***
<p align="center" width="100%">
    <img width="45%" src="/assets/SWR.jpg"> 
    <img width="47%" src="/assets/s11.jpg"> 
</p>

***No Antenna:***
<p align="center" width="100%">
    <img width="45%" src="/assets/SWR.jpg"> 
    <img width="47%" src="/assets/s11.jpg"> 
</p>
# Comments
if needed
