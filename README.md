# Slogger #

This is the code for a data logger currently being created at the UCSC Autonomous Systems Lab.

See http://byron.soe.ucsc.edu/wiki/Slogger for more documentation.

## Using the Slogger ##
Put a valid "config.txt" file onto the target micro SD card. Insert the card and connect the Slogger to a serial input. A new file will be created on the card with a name like "0001.txt". (The number increases by one for every reset.) When logging is finished, use the "dataExract.py" tool to remove headers and footers from the data.

### Other Usage Notes ###
> Send data to the device with 115200 baud UART

> Put a valid "config.txt" file on the target SD card. See documentation for an example file. NOTE: The config file does not set the baudrate of the device, but a valid config file with BAUD [number] tag is still required.

> Inserting an SD card might cause the device to reset.

> Resetting the device will cause a new file to be created

> Data is recorded in chunks of 506 bytes. It is possible for the last 505 bytes of data to be lost.

> __IMPORTANT:__ This project is still in development. Chunks of data might be lost. Please take note of any issues, and send them to the developer: Jesse Harkin (jdharkin@ucsc.edu).
