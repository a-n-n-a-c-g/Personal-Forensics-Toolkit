# DATA FORENSICS-SPECIFIC TOOLS

## Autopsy
Analyzes (doesn't create) image files.
- https://www.sleuthkit.org/sleuthkit/docs.php.
- https://www.sleuthkit.org/autopsy/

## Event2Timeline
Divides up specific log files into a timeline.
To use this tool: ```event2timeline.py -c -f csv_filename.csv```
- https://github.com/certsocietegenerale/event2timeline/blob/master/event2timeline.py

## EventViewer
Manually look through Windows event logs.
- https://www.howtogeek.com/123646/htg-explains-what-the-windows-event-viewer-is-and-how-you-can-use-it/

## FTK Suite / FTK Imager
Image analysis and capture, imager is free.
- https://support.accessdata.com/hc/en-us/articles/204056525-FTK-User-Guide
- https://accessdata.com/products-services/forensic-toolkit-ftk

## LiMe
Capture live memory on Linux-based devices (also includes Android). It returns a .dump format when it's done analyzing. It's also handy to use in conjunction with Netcat; this combination allows for live memory capture to be completed remotely.
To use this tool: ```insmod ./lime.ko "path=<outfile | tcp:<port>> format=<raw|padded|lime> [digest=<digest>] [dio=<0|1>]"```
- https://directory.fsf.org/wiki/LiME

## OSXpmem
Captures the volatile memory on a computer running OSX. Spits out a .dump file.
To use this tool: ```$ ./osxpmem.app/osxpmem -o <output_dir>```
- https://oscp.tech/apple-mac-memory-forensics-setup/

## Redline
File and memory analysis, makes a timeline from various logs and events. To get the actual download link, you have to sign up for Redline's email list.
- https://resources.infosecinstitute.com/memory-analysis-using-redline/#gref
- https://www.fireeye.com/services/freeware/redline.html

## Rekall
Entire, open-source suite of data forensics tools.
- http://www.rekall-forensic.com/
- https://github.com/google/rekall

## Volatility
Memory capture analysis. To use this tool: ```python vol.py --info```
- https://github.com/volatilityfoundation/volatility

## WinPreFetchView
Allows users to view the Windows PreFetch files easily and then export the data that they find/choose to export.
- https://www.nirsoft.net/utils/win_prefetch_view.html
- https://www.softpedia.com/get/System/System-Info/WinPrefetchView.shtml

## Wireshark
Network capture and network traffic analysis
- https://www.wireshark.org/docs/
