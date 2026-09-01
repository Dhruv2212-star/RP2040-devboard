# RP2040 based devboard. 
**why did i make this board??**  
hmmmm.. well one day i realised that i have made many projects wit devboard but i have never made my own devboard.  
this was it! so this was a golden project opportunity for me to challenge myself to make something.  
i went and search some tutorials on how devboards worked and how to make them.  
Out of all of the possible devboards out there. one particular board caught my eye, it was the **RP2040** Devboard because it was reallllyy easy to make and really functional and powerful because of it's storage capacity and the no. of GPIO pins it had.  


**Now let me explain to you how i built this devboard :)**  
for a Devboard to work you need to have the basic idea of the chip architecture, with our *RP2040* chip, it uses 3.3v for the main power pins but uses 1.1v for the logic pins and fortunately for our chip it has a built in voltage control which reduces the voltage to 1.1v so no need of extra components  


**decoupling capacitors**- we are using 100nF capacitors per each power pin (IOVDD) and 1uF capacitors for VREG_IN and VREG_OUT each and 2 100nF capacitors for DVDD pin, 100nF capacitor for ADC_AVDD and 100nF for USB VDD  


**Flash storage-** for storing our code in the devboard we are using W25Q128JVS chip for this function, we are going to use QSPI pins for this connection  

**Crystal oscillator**- for this build the data sheet recommends 12Mhz crystal, and in our board we are using   
ABLS-12.000MHZ-B4-T for this  

**GPIO pin extensions**- using 1x20 connectors, we extend it to connectors where we can utilize them.  

# BOM ( Bill of materials)  
## Bill of Materials (BOM)

| Reference          | Qty | Value / Part                | Footprint                               | Purchase                                      |
| ------------------ | --: | --------------------------- | --------------------------------------- | --------------------------------------------- |
| C1, C2             |   2 | 10 µF                       | `C_0603_1608Metric`                     | [Link](https://amzn.in/d/0bsal2JG)            |
| C3, C4, C5, C9–C15 |  10 | 100 nF                      | `C_0402_1005Metric`                     | [Link](https://amzn.in/d/0h4zQ3Lf)            |
| C6, C7             |   2 | 1 µF                        | `C_0402_1005Metric`                     | [Link](https://amzn.in/d/0exjZiSL)            |
| C8                 |   1 | 100 nF                      | `C_0402_1005Metric`                     | [Link](https://amzn.in/d/0hHEodPN)            |
| C16, C17           |   2 | 27 pF                       | `C_0402_1005Metric`                     | [Link](https://amzn.in/d/0bekUa1Y)            |
| D1                 |   1 | LED                         | `LED_0603_1608Metric`                   | [Link](https://amzn.in/d/0jdhjUcx)            |
| J1                 |   1 | USB-C Receptacle USB2.0 16P | `USB_C_Receptacle_GCT_USB4105-xx-A_16P` | [Link](https://amzn.in/d/03EJbP2P)            |
| J2                 |   1 | 1×2 Pin Header              | `PinHeader_1x02_P2.54mm_Vertical`       | Cut from 1×40 header                          |
| J3                 |   1 | 1×4 Pin Header              | `PinHeader_1x04_P2.54mm_Vertical`       | Cut from 1×40 header                          |
| J4, J5             |   2 | 1×20 Pin Header             | `PinHeader_1x20_P2.54mm_Vertical`       | [Link](https://amzn.in/d/06pAoX1t)            |
| R1, R2             |   2 | 5.1 kΩ                      | `R_0603_1608Metric`                     | [Link](https://amzn.in/d/05xfBy6B)            |
| R3, R9             |   2 | 10 kΩ                       | `R_0402_1005Metric`                     | [Link](https://amzn.in/d/02u6eVpk)            |
| R4, R5             |   2 | 27.4 Ω                      | `R_0603_1608Metric`                     | [Link](https://amzn.in/d/07J2YWcO)            |
| R6, R7, R8         |   3 | 1 kΩ                        | `R_0603_1608Metric`                     | [Link](https://amzn.in/d/02u6eVpk)            |
| SW1                |   1 | RESET — TL3301AF160QG       | `SW_Push_1P1T_NO`                       | [Link](https://www.digikey.in/short/r89qvhmn) |
| U1                 |   1 | NCP1117-3.3                 | `TO-252-2`                              | [Link](https://www.digikey.in/short/ff3dmq3j) |
| U2                 |   1 | RP2040                      | `QFN-56-1EP_7x7mm`                      | [Link](https://amzn.in/d/011fsK23)            |
| U3                 |   1 | W25Q128JVS                  | `SOIC-8_5.3x5.3mm_P1.27mm`              | [Link](https://www.digikey.in/short/zzb4v2bb) |
| Y1                 |   1 | Crystal                     | `Crystal_SMD_HC49-SD`                   | [Link](https://www.digikey.in/short/9m893pn7) |


# Final schematic look: 

<img width="848" height="481" alt="image" src="https://github.com/user-attachments/assets/1f0f263c-ea28-43bc-83b0-067503d9ceb7" />

# PCB tracing pics on KIcad  

<img width="399" height="466" alt="image" src="https://github.com/user-attachments/assets/c9e58091-d6bc-4d9c-973d-52f97042af91" />
<img width="395" height="453" alt="image" src="https://github.com/user-attachments/assets/3f0f60b2-e7a0-4ed0-af22-3f7b5dc8da82" />
<img width="384" height="458" alt="image" src="https://github.com/user-attachments/assets/879b0c32-7587-4e4f-bc4d-c721a43e715b" />

# Acutual PCB preview 

<img width="861" height="474" alt="Thumbnail" src="https://github.com/user-attachments/assets/548f1b23-0ab1-4747-8e6b-8f9092c0f219" />  

# 3D model view in Kicad 

<img width="672" height="603" alt="image" src="https://github.com/user-attachments/assets/f44c7aa3-5bcd-44ce-aa03-fe0cfc3a1074" />





