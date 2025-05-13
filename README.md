# Argon ONE fan script for DietPi
These installation steps are specific to the **DietPi** operating system on Raspberry Pi and will enable you to use the fan and button behaviour as intended on the [Argon ONE mini Case]
(https://argon40.com/products/argon-one-v2-case-for-raspberry-pi-4)

## Required software packages:

- Pytyhon 3 [130]
- Python 3 RPI.GPIO [69]
- I2C [72] 

use 'dietpi-software' to install missing software packages

## Required hardware settings:

use 'dietpi-config' then 'Advanced Options' to enable required hardware

- Serial/UART -> ttyS0 | toggle On
- I2C state | toggle On

alternatively you can run the following lines in the terminal:
- `sudo /boot/dietpi/func/dietpi-set_hardware i2c enable`
- `sudo /boot/dietpi/func/dietpi-set_hardware serialconsole enable`

&nbsp;  

## Install Argon ONE deamon and config
Now the system is ready to run my customised (or the original) install script (changes denoted below) from argon to enable fan and button behaviour. 

Run from terminal:
- `curl https://raw.githubusercontent.com/gwylanscheeren/argonone_dietpi/master/argon1.sh | bash`  

alternatively: 
- `curl https://download.argon40.com/argon1.sh | bash`  

&nbsp;  

## Change fan settings:

Run from terminal: 
- `argone-config`
