# OMI ENABLEMENT Guide

## HARDWARE DESCRIPTION

For the purpose of open sourcing the design, a collaboration between OMI members led to a tuning of an omi host FPGA reference design "[Fire](../fire/)" to be used in a [VCU128 Card] from AMD/Xilinx.

[VCU128 Card]: https://www.xilinx.com/products/boards-and-kits/vcu128.htmlhttps://www.xilinx.com/products/boards-and-kits/vcu128.html

With addition of a simple FMC+ connected add-on card, any OMI compatible memory DDIMM module can be evaluated.

![vcu_tormem_setup](../pictures/vcu_tormem_setup.PNG)

The setup allows evaluation of 2 DDIMM modules in slots A and B.

Some code is required to synchronize and test the OMI DDIMMs.

Either the code is executed in a companion raspberry pi or any I2C capable computer, or even in an embedded microblaze processor (the latter being under development)

Python source code is available at : [Python Code]

[Python Code]:https://github.com/OpenCAPI/omi_enablement/tree/main/python

Python code documentation is available at : [Python Documentation]

[Python Documentation]:../python

- Checks I2C tree
- Synchronizes DDIMMs
- Executes simple transfers in memory (not published yet)

!!! Note    The Raspberry pi can host an Cronus server, should you want to evaluate in a Cronus environment.

## REQUIREMENTS

Hardware requirements :

Procure the following:

- A VCU128 Board from [AMD/Xilinx](https://www.xilinx.com/)
- An adapter board from [Tormem](https://www.tormem.com/)
- At least one DDIMM module
- A USB relay card to ensure automated fire reset / 3.3V / 12V POWER control (will be included in adapter board version 2)

Software requirements : 

- Obtain an AMD/Xilinx Licence for Vivado. Requires **2018.3** version for this contribution (best timing results at maximum bandwidth). 

## ENABLEMENT STEPS

git clone the "[no-encrypt_vcu128](https://github.com/acastellane/omi_host_fire/tree/no_encrypt_vcu128)" branch of Fire design. 

First synthetize, implement and generate bitstream of "FIRE" design for the VCU128 using the specific branch as specified in the README.md file.

git clone the [https://github.com/OpenCAPI/omi_enablement/](https://github.com/OpenCAPI/omi_enablement/) and use /python directory with a debugging raspberry pi or any computer with I2C capability to check you can see the design.

Check Python code documentation at : [Python Documentation] for further experiments.

[Python Documentation]:../python