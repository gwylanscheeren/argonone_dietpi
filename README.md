# argonone_dietpi
Argon One fan control script, adapted for the DietPi operating system

## Installation instruction:

Run from terminal: `curl https://raw.githubusercontent.com/gwylanscheeren/argonone_dietpi/master/argon1.sh | bash`

### Changes made to the original script:
#### In order to adapt the script to the DietPi operating system I replaced the following lines:

`sudo raspi-config nonint do_i2c 0`  
`sudo raspi-config nonint do_serial 0`

to:

`sudo /DietPi/dietpi/func/dietpi-set_hardware i2c enable`  
`sudo /DietPi/dietpi/func/dietpi-set_hardware serialconsole enable`

#### Furthermore I removed the warning and confirmation step before the menu appears from `argonone-config`.
