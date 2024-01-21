### This is for the latest 6.1.y XU4 kernel as of October 2023

### What does it do?

Makes Odroid XU4 fan silent on idle load and quite on medium load

### Is it safe to use?

When script quits it brings fan mode back to *automatic* "factory" settings.

## Usage
``` 
sudo apt-get install git
git clone https://github.com/f1vefour/odroid-xu4-fan-control.git
cd odroid-xu4-fan-control
chmod +x odroid-xu4-fan-control.sh
sudo ./odroid-xu4-fan-control.sh
```
## Installation

To make it start when system boots:

edit odroid-fan-controller and add the path of the odroid-xu4-fan-control.sh script (full-pathname), then do the following to add it
to the runlevels

    cd /etc/init.d/
    #adjust to correct, absolute path below
    sudo cp ~/odroid-xu4-fan-control /etc/init.d/odroid-fan-controller
    sudo update-rc.d odroid-fan-controller defaults

you can also use the following to start the controller

    sudo /etc/init.d/odroid-fan-controller start

or

    sudo /etc/init.d/odroid-fan-controller stop

to stop the controller

Modificar el archivo odroid-fan-controller que va a estar en /etc/inid.d/
dir=""  PONER EL DIRETORIO DONDE VA ESTAR EL ARCHIVO
cmd="/opt/odroid-xu4-fan-control/odroid-xu4-fan-control.sh"  -- POR EJEMPLO ruta completa donde esta el scripts ejecutable.
