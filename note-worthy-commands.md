## The following commands where learned and noted due to its interesting usability

The following command installs a iso file to the usb drive with command line:
> ```sudo dd bs=4M if=ubuntu-20.04-desktop-amd64.iso of=/dev/sdc conv=fdatasync  status=progress```

Starts a detached screen:
>```screen -dmS <scree-name> bash -c '<screen-command>'```

Records the screen with ffmpeg:
* left screen
    * ```ffmpeg -f x11grab -video_size 1366x768 -framerate 25 -i :0.0+0,0 output.mp4```
* right screen
    * ```ffmpeg -f x11grab -video_size 1366x768 -framerate 25 -i :0.0+1366,0 output.mp4```

ssh-copy-id installs an SSH key on a server as an authorized key:
> ```ssh-copy-id -i ~/.ssh/mykey user@host```

List all activities from a given apk:
>aapt dump badging <pulledfile.apk>


### Docker post-install
After facing some difficulties to run docker as non-root I needed to run the following commands:
> sudo groupadd docker

> sudo usermod -aG docker $USER

Yet still, docker was requiring root permissions, so I've found the following command that fixed my problem:

> sudo setfacl -m user:$USER:rw /var/run/docker.sock

Changes terminal default text editor:
> sudo update-alternatives --config editor
