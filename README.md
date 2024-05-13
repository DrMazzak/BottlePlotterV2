# BottlePlotterV2
Pen Plotter for Bottles

Offical HomePage https://bottleplotter.cz

Blog post describing its creation https://vgnotepad.blogspot.com/2024/04/bottle-plotter.html

Offical Discord server to get help or just show off your prints https://discord.gg/zZ26gJUf

![MakerFair24 Prague](https://bottleplotter.cz/mf24.jpg)

## Getting started
- Start by ordering all neccessary part needed for the build. Use parts list for reference
- You can in paralel start with printing all printed parts
- When you have all the parts start the assembly process
- Upload GRBL firmware onto Arduino
- Modify GRBL config to be the same as the reference on github
- Try to home your bottle plotter, be ready to turn it of in case of crash

## Manufacturing resources
- 3D Model https://cad.onshape.com/documents/39d12f9046f30a3a8d27d3a6/w/22b7987c4c49474e20d7ab2c/e/e2aa020f57ba51d7f6ca55f8?renderMode=0&uiState=6641cd91d067751e5ce12537
- Parts list https://docs.google.com/spreadsheets/d/1IbpUXygSXaxqdkgz3Y6rmIXEAm9HOfCtqmNR5Q4xavQ/edit?usp=sharing

## Printed parts
All printed parts are designed to be printed without support on draft 0.3mm layer setting PLA with 30% infill.

## SW stack
- Inkscape
- SVG file
- SVG to GCODE (Mine very pre-Aplha on https://bottleslicer.gaman.cz)
- CNCjs
- GRBL

## TBD
- Test some proper GCODE generator
- Find some better electronics board
- Better screw adapters
- More optimizations of printed parts for less material and print time

## GRBL config
>$0=10 (Step pulse time, microseconds)
>
>$1=25 (Step idle delay, milliseconds)
>
>$2=0 (Step pulse invert, mask)
>
>$3=1 (Step direction invert, mask)
>
>$4=0 (Invert step enable pin, boolean)
>
>$5=0 (Invert limit pins, boolean)
>
>$6=0 (Invert probe pin, boolean)
>
>$10=1 (Status report options, mask)
>
>$11=0.010 (Junction deviation, millimeters)
>
>$12=0.002 (Arc tolerance, millimeters)
>
>$13=0 (Report in inches, boolean)
>
>$20=0 (Soft limits enable, boolean)
>
>$21=0 (Hard limits enable, boolean)
>
>$22=1 (Homing cycle enable, boolean)
>
>$23=0 (Homing direction invert, mask)
>
>$24=25.000 (Homing locate feed rate, mm/min)
>
>$25=200.000 (Homing search seek rate, mm/min)
>
>$26=40 (Homing switch debounce delay, milliseconds)
>
>$27=4.000 (Homing switch pull-off distance, millimeters)
>
>$30=0 (Maximum spindle speed, RPM)
>
>$31=0 (Minimum spindle speed, RPM)
>
>$32=0 (Laser-mode enable, boolean)
>
>$100=13.58 (X-axis travel resolution, step/mm)
>
>$101=800.000 (Y-axis travel resolution, step/mm)
>
>$102=800.000 (Z-axis travel resolution, step/mm)
>
>$110=15000.000 (X-axis maximum rate, mm/min)
>
>$111=1100.000 (Y-axis maximum rate, mm/min)
>
>$112=1500.000 (Z-axis maximum rate, mm/min)
>
>$120=100.000 (X-axis acceleration, mm/sec^2)
>
>$121=100.000 (Y-axis acceleration, mm/sec^2)
>
>$122=100.000 (Z-axis acceleration, mm/sec^2)
>
>$130=2000.000 (X-axis maximum travel, millimeters)
>
>$131=200.000 (Y-axis maximum travel, millimeters)
>
>$132=32.000 (Z-axis maximum travel, millimeters)
