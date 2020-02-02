### Install/Upgrade
The one of the following command can be used to either install (or upgrade) NextPVR on your device.

amd64 device (such as a PC or some NAS devices):<br/>
> docker pull nextpvr/nextpvr_amd64:latest

On a arm32v7 device (such as RPi):<br/>
> docker pull nextpvr/nextpvr_arm32v7:latest

### Running NextPVR
The following command can be used to run NextPVR in the backgrow. As you can see from the command line, docker needs to have "/config" in the container mapped to some local directory so that NextPVR can store it's configuration data.

> docker run -d \
>     --volume /home/graeme/config:/config \                      
>     --volume /home/graeme/videos:/recordings \
>     --volume /home/graeme/videos:/buffer \
>     --publish 8866:8866 \
>     nextpvr/nextpvr_amd64:latest
<!-- Should we add timezone? -->
If you're using an older legacy HDHomeRun, you'll also need a couple more parameters (replacing 192.168.1.51 with your host's IP address):

>     --env HOST_IP=192.168.1.51 \
>     --publish 8026:8026/udp \

In this example:
1) the /config directory in the container will map to the user's ~/config directory
2) the /recordings directory the container will map to the user's ~/videos directory
3) the /buffer directory in the container will map to the user's ~/videos directory
4) the local port 8866 will mapped to port 8866 in the container. NextPVR has historically used port 8866, so exposing it as port 8866 allows apps like Kodi to continue to access it easily.

### Using NextPVR
After running NextPVR, you can access it via a web browser at http://localhost:8866/index.html , and logging in with the default credentials of admin/password. If you intend to remotely access the NextPVR web app over the internet, you must change your username and password.
In addition to the web app, other popular ways to access it are via Kodi, or the our iOS / Android apps in their respective app stores. For more information see https://nextpvr.com/download.html