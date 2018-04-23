
# 3D Printer Information

Resources for building, maintaining and using your Prusa i3 clone.

## 1. Printer Specifications

1. General
   - Original Developer: [Prusa Research](http://www.prusa3d.com)
   - Vendor:	[Tronxy](http://www.tronxy.com/)
   - Manufacturer: Prusa
   - Model: TRONXY P802D/X6 (X6D_8_V1.6)
   - Firmware (original): [Repetier-0.91](https://github.com/cwyse/avrdude-build-usbtiny/tree/master/firmware)
   - Version: 1.6
   - Serial Number:
2. Components
   - Mainboard: [Melzi 2.0 V5](CJW_Files/Melzi-circuit.png)
     - CPU: [ATmega1284P](http://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-42719-ATmega1284P_Datasheet.pdf)
     - ​
   - LCD
     - 2004A
   - 42-Stepper Motors
     - Motor Code Definition
       - AABCCDD-EE
         - AA - Motor diameter (mm)
         - B - Stepper type (H = Hybrid)
         - CC - Motor length (mm)
         - DD -Holding Torque (N-cm)
         - EE - Amps * 10
     - Sense resistors: R100 => 0.1 Ohm
     - Extruder Motor: Tronxy 42H4054-16   NEMA 17   
       - Hybrid, 40 mm length, 54 N-cm Holding Torque, 1.6A
       - Step angle: 1.8 degree (200 steps per revolution)
       - Original Voltage:  E: 0.972 V, 1.22 A
     - X/Y/Z-Axis: Tronxy 42H4062-23  NEMA 17 
       - Hybrid, 40 mm length, 62 N-cm Holding Torque, 2.3A
       - Step angle: 1.8 degree (200 steps per revolution)
       - Original Voltage:  X: 0.775 V, 0.969 A
       - Original Voltage:  Y: 0.861 V, 1.08 A
       - Original Voltage:  Z: 0.823 V, 1.03 A
     - 4 [A4982 Stepper Motor Driver](CJW_Files/A4982-Datasheet.pdf)
       - Inputs: MS1 - 5 V, MS2 - 5V  =>  Sixteen
       -  Step Resolution, 4W1-2 Phase (value measured)
     - [Parameter calculations](https://www.prusaprinters.org/calculator/#steppers)
     - [Better parameter explanation](https://www.matterhackers.com/news/3d-printer-firmware-settings-stepper-motor-configuration)
   - Pulleys
     - GT2
     - 16 teeth
   - Belts
     - 2 mm pitch
   - Lead screw (M8)
     - 2 mm pitch (spacing between threads)
     - 8 mm lead (travel per revolution)
     - 8 mm diameter
     - 4 Start Thread
   - MK3 Hotbed
     - 3 mm Aluminum
   - Extruder
     - Tronxy P802M Extruder
     - Nozzle: 0.3 mm
     - Heating Tube: 12V 40W
     - Thermistor 100K
     - 1.75 mm Filament
   - Power Supply
     - Tronxy S-250-12
     - AC Input: 110/220V +/- 15%, 50/60Hz
     - DC Output: 12V 20A
     - Power 240W
3. Miscellaneous
   - [3D Printer Filament Guide 2018](https://all3dp.com/1/3d-printer-filament-types-3d-printing-3d-filament/)
   - [PLA Filaments | ABS Filaments | Filament Recycler | RePLAy 3D](https://replay-3d.com/)
   - [USB Tiny ISP Programmer](https://www.amazon.com/gp/product/B01FDD4EP0/ref=oh_aui_search_detailpage?ie=UTF8&psc=1)
     - Brand: SenMod
     - ![1523839624053](Files_CJW/USBTinyDescription.png)

## 2.  Parameter Calculations

1. Step per mm for leadscrews
   - 2560 steps/mm
   - [Calculation](Files_CJW/LeadscrewStepsPerMM.JPG)
2. Step per mm for belts
   - 100 steps/mm
   - [Calculation](Files_CJW/BeltsStepsPerMM.JPG)
3. Axis calibration 4/23/18
   - X/Y/Z -  No calibration needed
4. Extruder calibration

## 3.  Documentation

1. [Tronxy 3D Printer X6D Installation Guide](https://github.com/cwyse/3D-Printer-2018/blob/master/Files/TRONXY_X6D_installation_guideV.01.pdf)

Below is from Paul Langdon.

## 1. Software

The following are a good place to start for beginners but by no means the complete list. There is a reference list [here](#appendix).

### 1.1 For Running your Printer

* Cura (Win/Mac) - [Get v.15.x](https://ultimaker.com/en/products/cura-software/list)
  * [Cura Setup Guide](/Configurations/Cura/Cura-SetupGuide.md)
* Repetier (Win/Mac/Linux) - [Download](https://www.repetier.com)
  * [Repetier Config Guide](/Files/how_to_slice.pdf)
  * [Repetier Tutorial](Files/Tutorial_Repetier-Host.pdf)
* Slic3r (Win/Mac) - [slic3r](http://www.slic3r.org)

#### 1.2 Offline Printing
* [How to print from SD Card](Files/How_to_off-line print.pdf)

#### 1.3 Source for 3D Files to Print
* [Thingiverse](http://www.thingiverse.com)
* [Yeggi](http://www.yeggi.com/)
* [MyMiniFactory](https://www.myminifactory.com)

##### 1.3.1 Lego
* Full Lego Catalog - [https://printabrick.org/](https://printabrick.org/)
* Lego CAD - [http://ldraw.org/](http://ldraw.org/)

#### 1.4 CAD and Design tools for designing things to print
##### Online tools
* [TinkerCad](http://www.tinkercad.com) - Free & easy
    * TinkerCad Beginners Video -  [youtube](https://www.youtube.com/watch?v=6SuV5VoAJl0)
    * TinkerCad Beginners Video - [Make a wrench](https://www.youtube.com/watch?v=60xfIu-lqAs)
* AutoCAD Fusion 360 - [Free Trial](https://www.autodesk.com/products/fusion-360/overview)

##### Desktop Applications
* Sketchup - [https://www.sketchup.com/](https://www.sketchup.com/)


## 2. Hardware

Prusa i3 is an open source design 3D printer. Information about the project can be found [here](http://reprap.org/wiki/Prusa_i3).

[Orginal Prusa i3 Build Guide](/Files/prusa_i3_buid_manual_v1.0.pdf)

### 2.1 Machine Specific info to TRONXY P802D/X6 Model
* **Nozzle temperature:**	170-275℃
	 **Heatbed temperature:**	0-110℃
	 **Structure:**	Acrylic
	 **Power Supply:**	110V/220V 20A
	 **Print Size:**	220 x 220 x 180mm(Max)

![TronxyP802d.jpeg](/Files/TronxyP802d.jpeg)
![TronxyP802d.jpeg](/Files/TronxyP802d-1.jpeg)
![TronxyP802d.jpeg](/Files/TronxyP802d-2.jpeg)
![TronxyP802d.jpeg](/Files/TronxyP802d-3.jpeg)
![TronxyP802d.jpeg](/Files/TronxyP802d-5.jpeg)
![TronxyP802d.jpeg](/Files/TronxyP802d-4.jpeg)

### 2.2 Mainboard
[Melzi v2](http://reprap.org/wiki/Melzi) is the main board of the TRONXY P8902D.
![Melzi v2](http://i00.i.aliimg.com/wsphoto/v0/2038875198_1/RepRap-Melzi-v2-0-3D-Printer-Controller-Board-1284P-A4988.jpg)
![Wiring](/Files/wiring_diagram.png)

### 2.3 Drivers (for Melzi)
#### Mac/OSX
* [CH340G USB Drive](/Files/CH341SER_MAC.ZIP)

#### Windows
* [CH340G USB Drive](/Files/CH340G_windows.zip)
* [FTDI USB Driver](/Files/FTDI_USB_Driver.zip)

### 2.4 _Firmware - (Advanced or Future Use)_

* [Active Marlin Tronxy Source](https://github.com/erikkallen/Marlin_tronxy)

* [P802M_8_Repetier_V1.5.zip](/Files/P802M_8_Repetier_V1.5.zip)

* [P802MA_8_MarlinV1_Melzi_ADCKey.zip - for auto level upgrade](/Files/P802MA_8_MarlinV1_Melzi_ADCKey.zip)

* [Firmware update instructions](/Files/Update_firmware.pdf)


## 3. Assembly

### 3.1 Manuals
* [Vendor Instructions](/Files/TRONXY_X6D_installation_guideV.01.pdf)
* [A more detailed slightly different model](/Files/P802ma_installation_guide_V.07.pdf)

### 3.2 Videos
* Main Assembly video: [youtube](https://www.youtube.com/watch?v=b94YbwMqOKI)

* Additional Helper Videos - TRONXY [youtube channel](https://www.youtube.com/channel/UCMuP7Gc41bDmfNx5zhTAAHw/videos})


### 3.3 Tuning/Calibration

##### Bed Leveling
* [TRONXY Supplied PDF](/Files/P802_Level_instruction.pdf)
* [6 Simple Steps to 3D Printer Bed Leveling](https://pinshape.com/blog/6-simple-steps-to-3d-printer-bed-leveling/)

##### Calibration
* [HowTo Calibrate, Tune and Fine Tune your printer and filament & When](https://www.3dhubs.com/talk/thread/howto-calibrate-tune-and-fine-tune-your-printer-and-filament)
* [Advanced - Triffid Hunter's Calibration Guide](http://reprap.org/wiki/Triffid_Hunter%27s_Calibration_Guide)

##### Hints & Tips
* Bed Adhesion - having trouble sticking
1. Check your bed height and level with the paper trick
2. Try improving adhesion with hairspray


### 3.4 Troubleshooting
* [Illustrated Print Quality Troubleshooting Guide](https://www.simplify3d.com/support/print-quality-troubleshooting/)
* [Common 3d Printing Problems Troubleshooting](https://all3dp.com/1/common-3d-printing-problems-troubleshooting-3d-printer-issues/)

## 4. Filament
Your printer can support most filaments that can require temperatures in the 170-275℃ range.

![Filament Chart](/Files/filament.png)

### 4.1 Filament Sources
* Amazon - Good prices and resonable shipping

### 4.2  Brands
Amazon reviews are a good indicator of what is working and what may be no good.
Here are some brands I've had luck with and a some not so much:
* Hatchbox - Premium brand +$22 per 2kg roll [Amazon Store](https://www.amazon.com/HATCHBOX/b/ref=bl_dp_s_web_14181177011?ie=UTF8&node=14181177011&field-lbr_brands_browse-bin=HATCHBOX)
* 3D Solutech - [Amazon Store](https://www.amazon.com/3D-Solutech/b/ref=bl_dp_s_web_16009070011?ie=UTF8&node=16009070011&field-lbr_brands_browse-bin=3D+Solutech)
* Melca - [Amazon Store](https://www.amazon.com/Melca/b/ref=bl_dp_s_web_12667907011?ie=UTF8&node=12667907011&field-lbr_brands_browse-bin=Melca)
* NinjaFlex - Premium Rubber/Flexible print material $$$

**Bad Experience:**
* Gizmo Dorks - Had a tough time getting good prints, inconsistent width.

### 4.3 Additional Reading
* [The Best 3D Printing Filaments of 2017](http://3dinsider.com/3d-printing-filaments/)


## 5. Further Information, Enhancements & Interesting Projects

### 5.1 Resources and Groups
* [TRONXY Facebook Group](https://www.facebook.com/groups/Tronxy/)


### 5.2 Print Servers
Control your printer remotely over the web from your PC or Smart Phone
* [OctoPrint](https://octoprint.org) - RaspPi Print Server
* [AstroPrint](https://www.astroprint.com/) - RaspPi Print Server
* [CNCjs](https://github.com/cncjs/cncjs) - G-Code runner in a browser
* [Repetier-Server](https://www.repetier-server.com/)

Article: [Choosing Which 3D Printing Software to Use: OctoPrint or AstroPrint?](https://blog.astroprint.com/octoprint_vs_astroprint/)
### 5.3 Enhancements
One of the first things many new 3D printer owners do is print enhancements to their newly built printer.

Here are some for you to consider:
* [Improved cooling fan](https://www.thingiverse.com/thing:2154068) - this improves print quality in bridging and overhangs.
* [Another Fan enhancement](https://www.thingiverse.com/thing:1954001)
* [Power Supply Cover](https://www.thingiverse.com/thing:2741239) - cover to hide high voltage wires and provide On/Off switch
* [Cable management chain](https://www.thingiverse.com/thing:1905344)
* [Filament Guide](https://www.thingiverse.com/thing:2047357)

### 5.4 Misc
* ANet portal for their i3 clone - [https://3dprint.wiki/reprap/anet/a8](https://3dprint.wiki/reprap/anet/a8.)

* Deeper reading on 3D printing - [3dhubs Knowledge base articles](https://www.3dhubs.com/knowledge-base)


## Glossary


#### #


**3D model**	A 3D design typically produced on a CAD program.


**3D modelling**	The act of using 3D CAD programs to produce a design.


**3D printer**	An additive manufacturing machine that constructs a solid shape by building one layer at a time.


**3D printing**	The act of using an additive manufacturing machine (3D printer) to produce a solid object one layer at a time (also known as additive manufacturing).


**3D scan**	A process that captures the geometry of a real-world object and uses that data to produce a 3D model.
#### A


**ABS**	Acrylonitrile butadiene styrene (ABS) is a thermoplastic polymer commonly used in FDM 3D printing.


**Acetone treatment**	A post processing treatment often applied to 3D printed ABS parts to smooth the surface.


**Additive manufacturing**	The process of fabricating a part by adding material in layers (also known as 3D printing).


**Amorphous**	Any noncrystalline solid in which the atoms and molecules are not organized in a definite lattice pattern. Glass and polymers are typical amorphous solids. The opposite to crystalline.


**Anisotropic**	A material that has varying physical properties when measured in different directions. Wood and composites are common examples of anisotropic materials. The opposite to isotropic.
#### B


**Binder jetting**	Binder Jetting uses thin layers of powder to build up a 3D model. A colored binding agent extruded from a nozzle binding the powder together, solidifying the object with the desired colored surface. After the printing process, the models are strengthened with superglue and UV coated to prevent de-coloration by sunlight.


**Brim**	A single flat layer printed around the base of a model to prevent warping. The width of the brim can typically be altered in a slicer program.


**Bridge**	Occurs when the printer is required to print between 2 supports or anchor points. Because there is no support offered for the initial layer being printed (there is nothing to build upon) and it is required to “bridge” a gap.


**Brittleness**	A property of materials where it breaks without significant deformation. Chalk and ceramics are examples of brittle materials.


**Build plate**	The area where a 3D print is printed upon.


**Build resolution**	Typically refers to the layer height that a 3D print is printed at. Similar to the resolution on a television or computer monitor but in 3D the lower the build layer height the higher the part resolution.


**Build time**	The total time it takes for a 3D printer to complete a 3D print.
#### C


**CAD**	Computer aided design - a method of design where a computer program is used to create 3D objects in the form of electronic files.


**Casting**	The process of pouring a liquid material (typically metal) into a hollow cavity to produce a solid part of a specific shape.


**CNC machining**	Computer numerically controlled machining - a subtractive method of manufacturing that involves a computerized machine removing material over a predetermined path to produce a final part.


**Creep**	The tendency for materials to move or deform over time when subjected to a continuous load. Resins and polymers often experience this phenomena.


**Crystalline**	Any solid in which the atoms and molecules are organized in a lattice pattern. Metals are crystalline solids. The opposite to amorphous.


**Cupping**	Occurs in the SLA process when a hollow section of a print sucks up resin during the peel process (similar to a an upside down empty cup entering water). This suction effect can cause a part with thin walls to fracture.


**Curing**	Hardening of resin or photopolymers used for 3D printing typically done with a UV light.
#### D


**Ductility**	A material is said to be ductile if it is able to be deformed without losing toughness. Wire is an example of a ductile material. The opposite to brittle.
#### E


**Elongation**	Pulling or stretching a material. An important term in plastics to understand how a material will deform under load.


**End part**	A component that is intended to be used directly in a functional capacity.
#### F


**Flexural strength**	The stress (in MPa) at failure in bending.


**Filament**	The general term given to the material used in FDM. Typically supplied in coils or rolls the filament is heated up and fed through the nozzle to deposit the material on the build plate.


**FDM**	Fused Deposition Modeling (FDM) uses a string of solid material (filament), pushing it through a heated nozzle and melting it in the process. The printer continuously moves this nozzle around, laying down the melted material at a precise location, where it instantly cools down and solidifies. This builds up the model layer by layer. The most common 3D printing technology.
#### G


**Glass transition temperature**	The temperature region where a material transitions from a hard, glassy material to a soft, rubbery material.


**G-code**	The common name for the most widely used numerical control (NC) programming language. It is used in computer-aided manufacturing to control automated machine tools (like CNC's and 3D printers).
#### H


**Hollow**	A 3D print that is not solid and also does not contain any infill. Hollow models are much faster and cheaper to print but have very low strength.
#### I


**Infill**	A value usually represented in percentage that shows how much a solid model should be filled in with material when printed. 100% infill means the part is completely solid. Infill is used to make 3D printing cheaper and faster.


**Islands**	Occur in SLA printing and refer to cross sectional areas of a model that are not connected.


**Injection molding**	The process of injecting plastic in a melted liquid form into a die. The plastic fills the empty cavities of the die and cools until it has solidified. The solid plastic part is then ejected from the die and the process is repeated again.


**Isotropic**	A material that has the same physical properties in all directions. Glass and metal are common examples of isotropic materials. The opposite to anisotropic.
#### J


**Jig**	A frame used to hold components or parts in a fixed position used in the assembly or manufacturing process.
#### K
#### L


**Layer height**	Sometimes called print resolution this is the height of each layer of a 3D print typically measured in microns.
#### M


**Melting point**	The temperature a solid melts or turns into a liquid.


**Metal printing**	The process of 3D printing in metal. Objects are created from thin layers of powdered material by selectively sintering or melting it using a high power laser. There are a large range of metal printing technologies.


**Metal powder**	The material used for metal printing.


**Micron**	A measurement of distance regularly used to describe 3D printing layer height. 1000th of a millimeter. A human hair is approximately 17 microns thick.
#### N


**Nozzle**	The part of a 3D printer where the build material is extruded from.


**Nozzle diameter**	The diameter of the material that is extruded out of the nozzle. This plays an important role in FDM where shells and walls should be a multiple of nozzle diameter.


**Nylon powder**	A common build material used in the SLS printing process.
#### O


**OBJ file**	A geometry definition file. CAD models are exported as OBJ files then imported into a slicer program. The slicer program then converts the file into G-code to be interpreted by the 3D printer. Similar to .STL files.


**Offset**	In 3D printing offset refers to layers that are not printed directly inline with one another and are instead shifted to the side. This is often a printer calibration issue and will impact the quality of a print.


**Overhang**	Overhangs occur when a newly printed layer of material is only partially supported by the layer below. Angled walls are considered overhangs and depending on the print technology and angle often require support to print successfully.
#### P


**PLA**	Polylactic acid (PLA) is a thermoplastic polymer commonly used in FDM 3D printing. It is derived from corn starch or sugar cane.


**Photopolymer**	A polymer that changes its properties when exposed to light. For 3D printing this generally refers to photopolymers that are in a liquid/resin state and harden when exposed to UV light.


**Polyjet**	Similar to inkjet printing, but instead of jetting drops of ink onto paper, jets droplets of liquid photopolymer (in layers) onto a build tray and cures them instantly using UV light. The results are fully cured objects that can be handled and used immediately.


**Polymer**	A material whose molecular structure is composed of multiple repeating units. Natural polymeric materials include amber, wool, silk and natural rubber while synthetic polymers include resin, nylon, polystyrene and silicon.


**Post processing**	Any act of improving the appearance or material properties of a 3d print after it has been printed. This covers a large range of processes in 3D printing that vary by technology (support removal, UV curing, heat treating, sanding, tumbling, polishing, painting etc).


**Print head**	The part of a 3D printer where material is extruded/jetted from. Is an assembly of multiple components including the nozzle in the case of FDM.


**Print speed**	The speed the print head moves around the build plate typically measured in mm/s. 50mm/s is a common speed for desktop FDM printing.


**Print volume**	The largest possible dimensions a 3D printer is able to print at. Varies significantly by technology.


**Prototype**	An early part or model of a design built before production to test form, function, aesthetics and interaction usually at a low cost. Prototypes are typically items to learn from to improve a design.
#### Q
#### R


**Raft**	A thick grid with a roof that is added to the base of the part to limit the likelihood of warping occurring. Different to a skirt or brim.


**Rapid prototyping**	The process of creating physical prototypes directly from digital data.


**Resin**	A solid or highly viscous substance which is typically converted into a polymer. SLA uses resin exposed to UV light (a lazer) to build a part layer by layer.
#### S


**Shell**	In FDM printing the shell refers to the walls of the print that are exposed to the outside of the model. FDM will print shells at the perimeter of the model and then fill the model with infill. Different to wall thickness.


**Sintering**	The process of fusing particles together to form a solid mass of material using heat or pressure without melting it.


**Skirt**	A line that is initially printed around the print (but not connected to the print) to clean the nozzle head.


**SLA**	Stereolithography (SLA) creates 3D prints out of a liquid (photopolymer) resin, solidifying the material layer by layer using a lazer.


**SLS**	Selective Laser Sintering (SLS) uses a laser to shape and form extremely thin layers of powdered material by melting or sintering it together one layer at a time to create a solid structure.


**STL file**	STL (Standard Triangle Language) - A geometry definition file that uses triangles to describe the surfaces of a 3D model.. CAD models are exported as STL files then imported into a slicer program. The slicer program then converts the file into G-code to be interpreted by the 3D printer.


**Strain**	Measure of the deformation of the material relative to its original shape measured in mm/mm (or a dimensionless ratio).


**Stress**	The internal forces that particles of a material exert on each other measured in Pascals.


**Subtractive manufacturing**	Any manufacturing process that removes material to form a final shape (milling, turning etc). The opposite to additive manufacturing (3D printing).


**Support**	Support is the extra material that is printed during a 3D print allowing a design with complex geometry to be successfully printed. Support is required to successfully print overhangs and bridges and is removed and discarded in the post processing stage.


**Surface finish**	In 3D printing this refers to the roughness of the surface of a 3D printed part. Generally qualitative.
#### T


**Tank (resin)**	The area where resin sits before being cured in the SLA process.


**Temperature differential**	The difference in temperature between 2 points. In 3D printing reducing the temperature differential between 2 nearby points reduces the likelihood of warping or deformation.


**Tensile strength (ultimate)**	The stress (usually in MPa) at which a material will fracture or break when subjected to a tensile load.


**Tensile strength (yield)**	The stress (usually in MPa) at which a material will shift from elastic deformation (returning to its original shape) to plastic deformation (permanent deformation) when subjected to a tensile load.


**Thermoplastic**	A plastic material that becomes pliable or moldable above a specific temperature and solidifies upon cooling.
#### U


**UV light**	For 3D printing this refers to the type of light that is used to cure (harden) photopolymers in SLA and Polyjet 3D printing.
#### V
#### W


**Wall thickness**	Generally associated with minimum wall thickness - the thinnest dimension a wall can be printed at such that it can support the model. Varies by technology. Different from shell thickness.


**Warping**	Due to the high heat involved in most 3D printing process differential cooling results in areas of a print cooling at different rates resulting in deformation.
#### X


**X-axis**	The side to side (left and right) direction relative to the print bed
#### Y


**Y-axis**	The back to forth direction relative to the print bed.
#### Z


**Z-axis**	The up and down direction relative to the print bed.


### Appendix
#### 20 Best Free Software List - From https://all3dp.com


| Software |Function|Level|System
|--|--|--|--|
|[TinkerCAD](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#tinkercad)|3D Design, CAD|Beginner|Web Browser
|[3D Slash](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#3d-slash)|3D Design, CAD|Beginner|PC, Mac, Linux, Web Browser
|[Sculptris](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#sculptris)|3D Design, CAD|Beginner|PC, Mac
|[SketchUp](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#sketchup)|3D Design, CAD|Intermediate|PC, Mac, Linux
|[Fusion 360](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#fusion-360)|3D Design, CAD|Intermediate|PC, Mac
|[FreeCAD](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#freecad)|3D Design, CAD|Intermediate|PC, Mac, Linux
|[Blender](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#blender)|3D Design, CAD|Professional|PC, Mac, Linux
|[Onshape](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#onshape)|3D Design, CAD|Professional|Web Browser
|[Netfabb](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#netfabb)|Slicer, STL Checker, STL Repair|Intermediate|	PC, Mac, Linux
|[3D-Tool Free Viewer](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#3d-tool-free-viewer)|STL Viewer, STL Checker	|Intermediate|PC
|[MakePrintable](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#makeprintable)|STL Checker, STL Repair|Intermediate|Web Browser
|[MeshLab](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#meshlab)|STL Editor, STL Repair|Professional|PC, Mac, Linux
|[Meshmixer](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#meshmixer)|STL Checker, STL Repair, STL Editor	|Professional|PC, Mac
|[Cura](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#cura)|Slicer, 3D Printer Host|Beginner|PC, Mac, Linux
|[CraftWare](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#craftware)|Slicer, 3D Printer Host|Beginner|PC, Mac
|[KISSlicer](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#kisslicer)|Slicer|Beginner|PC, Mac, Linux, Raspberry Pie
|[MatterControl](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#mattercontrol)|Slicer, 3D Printer Host|Beginner|PC, Mac, Linux
|[Repetier](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#repetier)|Slicer, 3D Printer Host|Intermediate|PC, Mac, Linux
|[Slic3r](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#slic3er)|Slicer|Professional|PC, Mac, Linux
|[OctoPrint](https://all3dp.com/1/best-free-3d-printing-software-3d-printer-program/#octoprint)|3D Printer Host|Professional|PC, Mac, Linux


Article: [Top 20: Most Popular 3D Modeling & Design Software for 3D Printing (2017 Update)](https://i.materialise.com/blog/top-25-most-popular-3d-modeling-design-software-for-3d-printing/)

Article: [Top 16 Free 3D Printer Software for Beginners in 2018](https://www.dobot.cc/resource/top-15-free-3d-printer-software-for-beginners.html)