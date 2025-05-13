# Argon ONE fan script for DietPi
These installation steps are specific to the **DietPi** operating system on Raspberry Pi and will enable you to use the fan and button behaviour as intended on the [Argon ONE mini Case]
(https://argon40.com/products/argon-one-v2-case-for-raspberry-pi-4)
## Installation instructions:

### Required software packages:

- Pytyhon 3 [130]
- Python 3 RPI.GPIO [69]
- I2C [72] 

use 'dietpi-software' to install missing software packages

### Required hardware settings:

use 'dietpi-config' then 'Advanced Options' to enable required hardware
Serial/UART -> ttyS0 | toggle On
I2C state | toggle On

Now the system is ready to run my customised (or the original) install script (changes denoted below) from argon to enable fan and button behaviour. 

Run from terminal: 
`curl https://raw.githubusercontent.com/gwylanscheeren/argonone_dietpi/master/original_script.sh | bash`

alternatively: 
`curl https://download.argon40.com/argon1.sh | bash`

## Change fan settings:

Run from terminal: `argoneone-config`

&nbsp;  

## Changes made to the original script:
In order to adapt the script to the DietPi operating system I removed the following lines:

`sudo raspi-config nonint do_i2c 0`  
`sudo raspi-config nonint do_serial 0`

Furthermore I removed the annoying warning and confirmation step before the menu appears from `argonone-config`. And changed initial temperature=fan speed pairs to:
50=1  
55=20  
60=80  
65=100
