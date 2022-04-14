# Machinekit Basic 3 Axis Example With PRU-BeagleBone Black
- Machinekit İmage: https://rcn-ee.com/rootfs/bb.org/testing/2020-06-01/stretch-machinekit/
- İnstalling Guide: https://learn.adafruit.com/beaglebone-black-installing-operating-systems/flashing-the-beaglebone-black
- Hal_Pru_Generic Pinmap: https://github.com/cdsteinkuehler/beaglebone-black-pinmux/blob/hal_pru_generic/pinmux.ods
- Step Motor Drive Timing Values: http://wiki.linuxcnc.org/cgi-bin/wiki.pl?Stepper_Drive_Timing
# How to Install and Use
-----------------------------
- Go to download machinekit image from rcn-ee.com
- Flash to sd card with balena.io etc...
- Flash BeagleBone Black using adafruit blog.
- Connect a monitör beaglebone with HDMI to Micro-HDMI cable
- Open BeagleBone Black - default id:psswd machinekit:machinekit
- Open the Terminal




``` 
cd /home/machinekit/ 

mkdir config   

cp pru-3axis.hal /home/machinekit/pru-3axis.hal 

cp pru-3axis.ini /home/machinekit/pru-3axis.ini 

linuxcnc pru-3axis.ini # started axis screen code 
``` 


- copy file metod: uart(xmodem,ymodem), ssh(scp) ..etc
- text editor: nano,vim,gedit etc..
- Open the hal file with text editor.
- change to **Dirsetup** **Dirhold** **Steptime** **Stepspace** using first line websites wiki.linuxcnc.org
- Set to step and dir pin using hal_pru_generic pinmux.ods
- Go to run :=)
