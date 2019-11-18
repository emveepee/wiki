NextPVR will call certain scripts if they exist, to allow the user plugin their own custom handling of certain events. On Windows these scripts are created as batch files (.bat), in the C:\Users\Public\NPVR-data\scripts directory. On Linux these scripts are created as shell scripts (.sh), in the ... directory.

### Events

| Script        | Event |
| ------------- |-------------|
| ParallelProcessing      | Called when a recording is started |
| PostProcessing      | Called when a recording is completed  |
| PostCancel | Called when a recording is cancelled |
| PreStartup      | Called at startup before the recording service is started |
| UpdateEPG      | Called prior to processing the EPG  |
| PostLoadEPG | Called after the EPG has been loaded, but before recurring recordings have been processed |
| PostUpdateEPG | Called after the EPG update has been completed |
| PreArchive | Called prior to archiving (moving) a file to another volume |
| PostArchive | Called after archiving (moving) a file to another volume  |

When these script files are run, NextPVR will capture the output and send it to the NextPVR logs, to help you diagnose any problems with your scripts.

### Parameter

Some of these scripts are passed parameters. The table below details the parameters for those scripts.


### Linux example


### Windows example
