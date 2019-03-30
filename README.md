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
### Volatility
### Redline
### Rekall

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
