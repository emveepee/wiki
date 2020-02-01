# Filter Check

FilterCheck is a tool for creating a report of all audio/visual
input/output components installed.

## Download

[Download:FilterCheck.zip](utilities/downloads/FilterCheck.zip) and extract to a temporary folder.

## Usage

Run the exe and a FilterCheck.log file will be created in the same location as the Filtercheck.exe. No user interaction is required. The created text file can be opened in any text editor.

**Example FilterCheck.log file**
```
14:55:16.239	INFO	Checking AM_KSCATEGORY_TVAUDIO filters
14:55:16.240	INFO	found: Hauppauge HVR USB2 TvAudio
14:55:16.241	INFO	 - (input)  TVAudio In
14:55:16.241	INFO	            [43a587b3-4486-4f58-a97d7cde9a68988a]-00000003-00000000
14:55:16.241	INFO
14:55:16.241	INFO	 - (output) TVAudio Out
14:55:16.241	INFO	            [97ff8fc4-5287-4d93-95c7c0d5ce91ad82]-00000003-00000000
14:55:16.241	INFO
14:55:16.241	INFO	Checking AM_KSCATEGORY_VBICODEC filters
14:55:16.241	INFO
14:55:16.241	INFO
14:55:16.241	INFO	Checking KSCATEGORY_BDA_NETWORK_TUNER filters
14:55:16.242	INFO	found: Hauppauge HVR USB2 ATSC Tuner/Demod
14:55:16.244	INFO	 - (input)  Input0
14:55:16.244	INFO	            [00000000-0000-0000-0000000000000000]-00000000-00000000
14:55:16.244	INFO
14:55:16.244	INFO	 - (output) MPEG2 Transport
14:55:16.244	INFO	            [4c4332e6-c822-11db-beb400a0c9f21fc7]-00000003-00000000
14:55:16.250	INFO
14:55:16.250	INFO	found: Silicondust HDHomeRun Tuner 10528531-0
14:55:16.251	INFO	 - (input)  Input0
14:55:16.251	INFO
14:55:16.251	INFO	 - (output) Output1
14:55:16.251	INFO
14:55:16.251	INFO
14:55:16.251	INFO	found: Silicondust HDHomeRun Tuner 10528531-1
14:55:16.252	INFO	 - (input)  Input0
14:55:16.252	INFO
14:55:16.252	INFO	 - (output) Output1
14:55:16.252	INFO
14:55:16.252	INFO
14:55:16.252	INFO	Checking KSCATEGORY_BDA_RECEIVER_COMPONENT filters
14:55:16.253	INFO	found: Hauppauge HVR USB2 TS Capture
14:55:16.253	INFO	 - (input)  MPEG2 Transport
14:55:16.253	INFO	            [4c4332e6-c822-11db-beb400a0c9f21fc7]-00000003-00000000
```

Category: [Utilities](Utilities)
