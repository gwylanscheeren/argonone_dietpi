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
Now the system is ready to run the install script. 1st option is to use the last version known to be working. 2nd option is to run the latest version directly from the Argon40 website. 

### Run from terminal
Last version known to be working
- `curl https://raw.githubusercontent.com/gwylanscheeren/argonone_dietpi/master/argon1.sh | bash`  

Latest version directly from Argon40 website
- `curl https://download.argon40.com/argon1.sh | bash`  

### Add service to DietPi managed services
go to dietpi services configuration by entering in terminal:

`dietp--services`

'Add' `argononed`
go to new service 'argononed' entry and 'Include' into list of services managed by DietPi.

That's it. Enjoy your Argon One case fan and buttons.

&nbsp;  

## Change fan settings:

Run from terminal: 
- `argone-config`
