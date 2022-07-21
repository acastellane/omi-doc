# OMI ENABLEMENT Description

## Hardware Description

For the purpose of opensourcing the design, a collaboration between OMI members led to a tuning of omi host fpga design "Fire" to be used in a [VCU128 Card]

[VCU128 Card]: https://www.xilinx.com/products/boards-and-kits/vcu128.htmlhttps://www.xilinx.com/products/boards-and-kits/vcu128.html

With addition of a simple FMC+ connected add-on card, any OMI compatible memory DDIMM module can be evaluated.

![vcu_tormem_setup](../pictures/vcu_tormem_setup.PNG)

The setup allows evaluation of 2 DDIM modules in slots A and B.

Some code is required to synchronise and test the OMI DDIMMs.

Either the code is executed in a companion raspberry pi, or it can be run in an embedded microblaze processor.

Example of python code is available at : [Python Code]

[Python Code](https://github.com/OpenCAPI/omi_enablement/tree/main/python)

- Checks I2C tree
- Synchronizes DDIMMs
- Executes simple transfers in memory (not published yet)

!!! Note    The Raspberry pi can host an Cronus server, should you want to evaluate in a Cronus environment.

