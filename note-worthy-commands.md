## The following commands where learned and noted due to its interesting usability

The following command installs a iso file to the usb drive with command line
`sudo dd bs=4M if=ubuntu-20.04-desktop-amd64.iso of=/dev/sdc conv=fdatasync  status=progress`

Starts a detached screen
`screen -dmS <scree-name> bash -c '<screen-command>'