On Linux NextPVR supports IPTV, HDHomeRun, digital tuners (DVB-T, DVB-C, DVB-S, ATSC and QAM), and SAT>IP tuner (DVB-S, DVB-C, DVB-T).

### Installation from .deb file
The easiest way to install NextPVR is using the .deb file (thanks Martin for creating it!). 

> curl https://nextpvr.com/nextpvr-helper.deb -O<br/>
> sudo apt install ./nextpvr-helper.deb --install-recommends

Give it a half a minute or so to start, then you should be able to open http://127.0.0.1:8866 in your browser to setup NextPVR.

You can find more information about installing from the .deb file here, and updating when there is a new release, see here:
https://forums.nextpvr.com/showthread.php?tid=59576


### Manual Installation
If you're running on a platform that doesn't support .deb files, or prefer to manually install it, the application can be installed using the following steps. 

The latest files can be downloaded from
http://nextpvr.com/beta/linux/NPVR.zip

NextPVR needs a current .NET Core 2.2.x runtime to be installed. You can find download install information at: https://dotnet.microsoft.com/download/dotnet-core/2.2

Other packages you'll probably need include:

> sudo apt update <br/>
> sudo apt install mediainfo<br/>
> sudo apt install libc6 <br/>
> sudo apt install libgdiplus<br/>
> sudo apt install ffmpeg<br/>


**_Extract the NPVR.zip to a directory like /home/graeme/NPVR_**<br/>
> cd NPVR<br/>
> find . -name DeviceHostLinux -exec chmod 755 {} \;<br/>
> dotnet ./NextPVRServer.dll<br/>

If you'd trying to use an older legacy HDHomeRun on Linux, then you'll also need "sudo apt install hdhomerun-config"