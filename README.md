v800_downloader
===============

Normally if you sync over iPhone then hook the watch up to a PC and run FlowSync it will check to see if all the sessions have been uploaded, and if so not download anything from the watch. V800 Downloader will let you download the session data even if it's already been uploaded by your phone or FlowSync. This data then can be converted to TCX/GPX/HRM using Bipolar (https://www.github.com/pcolby/bipolar). This tool is not a standalone conversion tool but meant to be used as a supplement to Bipolar.

The tool looks through the filesystem on the V800 and determines which sessions still have valid data. FlowSync will only sync a session once but it doesn't delete the session; it just creates a file that is checked whenever FlowSync runs. The actual session data (route, samples, laps, etc.) are still on the watch until they are automatically deleted by some process, probably a housekeeping thing that deletes the older data as the watch gets full from newer data. Older sessions still retain the summary and statistics but lose the route and all the detailed data.

This tool lets you download the older session that still exist (in my case my watch has about a month worth of data on it when running ~4-5/hours a week). The data is output to the Bipolar directory to be converted by the Bipolar program.

Finally, there is an Advanced Options mode accessed by pressing Shift+A. This will allow you select to download the files off the watch and save them in a directory with their raw names. This will also allow you to open up the V800 Filesystem Browser. Both of these features are not useful to users but might interest developers/curious folks who are interested in seeing how the V800 is layed out software-wise internally.
