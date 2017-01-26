##RFM69HCW driver for BeagleBone Black
This is a driver for the RFM69HCW radio based on the universal driver by dltech. It uses Derek Molloy's SPIDevice C++ class to handle SPI communication. The SPIDevice class will be replaced with Intel's MRAA library once the proper corrections have been made to it as it currently does not support SPI properly on 4.9+ kernels.

##Original Content
This library implements packet transmittion on the RFM69 radiomodule, written in pure C. This library contains macros for all configuration registers, and macros which computes all nesessary parameters (like carrier frequency, filter bandwidth, etc). Because all parameters has computed through macros before compilation, this library will consume a little amount of memory and CPU resourses.

This is only the example of implementation, in order to use this library in your application, you have to implement your own rfm69_spi_read(), rfm69_spi_write() and rfm69_mcu_init() functions and interrupts.
