# PERSONAL FORENSICS TOOLKIT

## MEMORY ANALYSIS
### OSXpmem
My rating: ** / 5 <br><br>
This is a small, command-line based tool that captures the volatile memory on a computer running OSX. While this was a fairly straight-forward tool to use, I find it a little bit annoying that it only really works on the OSX platform. This tool analysis, when done, spits out a .dump file and takes quite a while to run. <br><br>
To use this tool: ```$ ./osxpmem.app/osxpmem -o <output_dir>```<br><br>
Setup/usage: https://oscp.tech/apple-mac-memory-forensics-setup/

### Hexdump
My rating: *** / 5 <br><br>
This tool has both a GUI and a command line version. I primarily use it to view/save files in hex, which is especially helpful for converting between encodings, doing memory analysis, and re-engineering various software programs. I gave it a 3/5 stars because the command line tool can be a little less than graceful to use at times, although I have not used the GUI version. <br><br>
To use this tool: ```$ hexdump <filename>```<br><br>
Setup/usage: https://sourceforge.net/projects/hexdump/

### LiMe
My rating: **** / 5 <br><br>
This is a small tool that is Linux based and is for capturing live memory on Linux-based devices (also includes Android). It returns a .dump format when it's done analyzing. It's also handy to use in conjunction with Netcat; this combination allows for live memory capture to be completed remotely. <br><br>
To use this tool: ```insmod ./lime.ko "path=<outfile | tcp:<port>> format=<raw|padded|lime> [digest=<digest>] [dio=<0|1>]"```<br><br>
Setup/usage: https://directory.fsf.org/wiki/LiME

### Netcat
My rating: *** / 5 <br><br>
This tool is used for moving files directly from one host to another, across the network. Used in conjunction with LiMe, forensic investigators are able to caputre live memory dumps remotely and then access them on their own host computer. I gave this tool a 3 because, while it is handy to use after you have it set up and are familiar with it, its documentation was a bit difficult to pick up on for first time users. <br><br>
To use this tool: [depends on the OS] https://kapeli.com/cheat_sheets/Netcat.docset/Contents/Resources/Documents/index <br><br>
Setup/usage: http://netcat.sourceforge.net/

### Volatility
My rating: ** / 5 <br><br>
This is kind of the industry standard tool used for memory capture analysis, as far as I can tell. However, I only gave it a 2 because I had an incredibly difficult time getting this setup; it appears that the windows .exe installer fails to install this tool correctly, and it must be installed via the choco installer. After getting this setup, it is a pretty handy tool to be able to view processes and threads, if it works.<br><br>
To use this tool: python vol.py --info <br><br>
Setup/usage: https://github.com/volatilityfoundation/volatility

### Redline
My rating: *** / 5 <br><br>
This is a GUI based tool from FireEye that allows for pretty easy file and memory analysis. This tool does have a really handy feature that allows for an easy way to make a timeline from various logs and events. However, this tool is a bit annoying in that, to get the actual download link, you have to sign up for Redline's email list.<br><br>
To use this tool: https://resources.infosecinstitute.com/memory-analysis-using-redline/#gref<br><br>
Setup/usage: https://www.fireeye.com/services/freeware/redline.html

### Rekall
My rating: **** / 5 <br><br>
Rekall is particularly cool because it is basically not at all platform dependent; it runs on anything that can run any version (2 or 3) of Python. It's widespread usability makes this framework standout! It actually has expanded recently, as well; it started life justa s a memory analysis tool and, now, is an entire, open-source suite of data forensics tools.<br><br>
To use this tool: http://www.rekall-forensic.com/ <br><br>
Setup/usage: https://github.com/google/rekall

## NETWORK ANALYSIS
### TCPDump
### Wireshark
### Ngrep
### Flowgrep
### Snort
### Suricata
### TCPDump 
### WinPCap
### Security Onion

## IMAGE ANALYSIS
### FTK Suite / FTK Imager
### Autopsy
### WinPreFetch
### EventViewer
### Pestudio
### Remnux
### Yara and Loki
### Event2Timeline
### VirusTotal.com
