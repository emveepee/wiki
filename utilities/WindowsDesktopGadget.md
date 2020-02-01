# NextPVR Windows Desktop Gadget


![](utilities/images/DesktopGadget1.png#center)

This is a Windows Desktop/Sidebar gadget that shows a few scheduled
recordings in the gadget and the full schedule in the flyout. It also
optionally shows the available disk space in the gadget and full system
status in a separate flyout. It works on any Windows 10/8/7.1 client with
network access to your NextPVR server.


## Enable Windows Gadget support

Microsoft stopped support for gadgets in 2012 citing security concerns. The concern is not really
gadget related, it is the same as installing any program from an unknown source on your system. To get Sidebar Gadget support again

  - Download and install the Windows Gadget (Sidebar) from https://8gadgetpack.net/


## Install and configure

  - Close and uninstall any previous versions of the gadget that you may
    be running on the target PC (right click entry in Gadget Gallery and
    choose 'Uninstall').
  - [Download](utilities/downloads/NPVRStatus.gadget.zip) the NextPVR Desktop Gadget
  - Unzip the NPVRStatus.gadget.zip file into "%userprofile%\AppData\Local\Microsoft\Windows Sidebar\Gadgets"
    - This should create a folder "%userprofile%\AppData\Local\Microsoft\Windows Sidebar\Gadgets\NPVRStatus.gadget"
  - From the Sidebar option "Add Gadgets" select NextPVR
  - On the gadget click the wrench or right-click the gadget and choose 'Options'.
  - Enter the appropriate server IP,  port and PIN
  - Click OK for it to connect and show the recording schedule and (optionally) free disk space.

## Usage

  - Click on the recording schedule area to show a flyout with the full
    recording schedule.

![](utilities/images/DesktopGadget2.png)

  - Click on the free disk space area to show a flyout with the system
    status.

![](utilities/images/DesktopGadget3.png)

## Support

[Windows Desktop Gadget support thread in the Addon On support
forum.](https://forums.nextpvr.com/forumdisplay.php?fid=12)

## Customize Recording Schedule Item

Customizing what is displayed for each recording schedule item is
possible in the Options. It is a javascript string that is easy to mess
up so edit with care. The "rec" object has the following properties
available for each schedule item: Title, Subtitle, Description, Start,
Stop, ChannelName, ChannelNumber, ChannelLogo, Status, oid, rid

### Example

The following example adds the channel logo and Subtitle for each item
(see image below). Go to the Schedule Options page in the gadget, change
the 'Schedule item height' to 50, and copy all the text below and
replace the text that is in the 'HTML string' text box in the Options.

```
"<div class='RecordingTitle' style='height:20px'>"
+ "<img style='position:relative;top:3px' height='15px' src='" + rec.ChannelLogo + "' />&nbsp;"
+ rec.Title + "</div>"
+ (rec.Subtitle != "" ? "<div class='RecordingSub'>" + rec.Subtitle + "</div>" : "" )
+ "<div class='RecordingSub'>" + (isRecordingNow ? "-" + rec.Stop.format(gTimeFormat) : (date != today ? date : rec.Start.format(gTimeFormat))) + " " + rec.ChannelName + "</div>"
```

[Download: NextPVR Desktop Gadget](utilities/downloads/NPVRStatus.gadget.zip)


## Author(s)

Developed by [cncb](https://forums.nextpvr.com/member.php?action=profile&uid=13622)
updated for v5 [mvallevand](https://forums.nextpvr.com/member.php?action=profile&uid=5939).

Thanks to [BrettB](https://forums.nextpvr.com/member.php?action=profile&uid=8873) who did most of the testing of the netcore update.


Category: [Utilities](Utilities)
