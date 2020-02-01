# NextEnd

NextEnd - Sports time extender and more.

NextEnd is a command line tool designed to monitor sports recordings and extend the recording time until the games is over. Additionally it can extend the time of shows that follow sports events.

## Downloading and Installing

The latest version of the NextEnd utility is v3.0.7317.27040

[Download NextEndV5 Release Candidate](utilities/downloads/NextEndV5~rc.zip)

#### Windows

#### Linux and macOS

#### Docker

## Un-Installing

To uninstall remove the following folder Plugins/NextEnd and modify your your sripts

#### Usage

#### Windows

To use NextEnd add the follow to your ParallelProcessing.bat file

start /b "" "C:\Users\Public\NPVR-data\Plugins\NextEnd\NextEnd.exe" --oid %3

This option will extend sports and the shows that follow sport.

To extend shows on Sunday nights in primetime add the following to your PostUpdateEPG.bat

start /b "" "C:\Users\Public\NPVR-data\Plugins\NextEnd\\NextEnd.exe" --sunday

Note if you stop the recording service on Sunday this process will stop.

#### Other Platforms

## Other Options

--cancel cancel recording when sports stop (stop padding)

--early cancel recording sports when sports stop early

--postgame time to add on for postgame chat (Default 10 minutes)

--preempt if sports overrun end of next show skip it

--resume ad a resume point to the actual game stop time

## Support

This plugin is supported in the [3rd Party Plugins Utilities & Skin support forum](https://forums.nextpvr.com/forumdisplay.php?fid=12)

Background History [Annoyances caused by sporting events](https://forums.nextpvr.com/showthread.php?tid=48785)

## Author(s)

Developed by [mvallevand](https://forums.nextpvr.com/member.php?action=profile&uid=5939).

Thanks to [greg_in_kansas](https://forums.nextpvr.com/member.php?action=profile&uid=8102) for his help testing the initial release and many users trialing the V5 netcore update.

## History

Note this is port of the the


```
v3.0.7317.27040 Release candiate for V5 netcore version


v1.0.5633.10942 (3 Jun 2015) - use Slugger's new monitor - update for FIFA WWC

v1.0.5509.22035(31 Jan 2015) - update for "Super Bowl XLIX"

v1.0.5409.33325(23 Oct 2014)

*   store .stop files in Plugins\NextEnd
*   cleans up old .stop files
*   support for CFL Football

v1.0.5406.41430(20 Oct 2014)

*   better handling of one-off recordings
*   fixed four hour limit on monitoring
*   added new sports, NBA, 2014 World Series, NASCAR Racing, Formula One Racing
*   better resume handling

v1.0.5392.36447 (13 Oct 2014) Released to wiki
```

* * *

Category:[Utility]()
