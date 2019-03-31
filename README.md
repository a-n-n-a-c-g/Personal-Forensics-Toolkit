# PERSONAL FORENSICS TOOLKIT

## MEMORY ANALYSIS
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

### OSXpmem
My rating: ** / 5 <br><br>
This is a small, command-line based tool that captures the volatile memory on a computer running OSX. While this was a fairly straight-forward tool to use, I find it a little bit annoying that it only really works on the OSX platform. This tool analysis, when done, spits out a .dump file and takes quite a while to run. <br><br>
To use this tool: ```$ ./osxpmem.app/osxpmem -o <output_dir>```<br><br>
Setup/usage: https://oscp.tech/apple-mac-memory-forensics-setup/

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

### Volatility
My rating: ** / 5 <br><br>
This is kind of the industry standard tool used for memory capture analysis, as far as I can tell. However, I only gave it a 2 because I had an incredibly difficult time getting this setup; it appears that the windows .exe installer fails to install this tool correctly, and it must be installed via the choco installer. After getting this setup, it is a pretty handy tool to be able to view processes and threads, if it works.<br><br>
To use this tool: ```python vol.py --info``` <br><br>
Setup/usage: https://github.com/volatilityfoundation/volatility

## NETWORK ANALYSIS
### Flowgrep
My rating: ***** / 5 <br><br>
Flowgrep is a combination of tcpflow, tcpkill, and ngrep. It's Python based, so it'll work on pretty much any platform. It's a command-line-based tool that lets you search network traffic just as you're used to searching Linux file systems. I really like this tool!<br><br>
To use this tool: ```./flowgrep OPTIONS [FILTER]```<br><br>
Setup/usage: https://monkey.org/~jose/software/flowgrep/

### Ngrep
My rating: *** /5 <br><br>
Ngrep is kind of like TCPdump but with the added functionality of letting you search for regex expressions and patterns. This can be pretty helpful if you already know what kind of patterns or signatures you're searching for, but is less helpful if you're hoping for a program that'll tell you which signatures keep appearing.<br><br>
To use this tool: ```ngrep -l -q -d eth0 -i "^GET |^POST " tcp and port 80```<br><br>
Setup/usage: http://ngrep.sourceforge.net/usage.html

### Security Onion
My rating: *** / 5 <br><br>
This is an intrusion detection focused operating system, and, when the setup process is completed, it has some really handy tools already incorporated into it. Getting Security Onion setup can be a major pain; it takes quite a while to get through the entire setup process! However, once it's setup properly, this is a really cool tool for spotting patterns and connections in network traffic. <br><br>
To use this tool: [It's a full OS...]<br><br>
Setup/usage: https://github.com/Security-Onion-Solutions/security-onion

### Snort
My rating: *** / 5 <br><br>
Snort is a light-weight, open-source, command-line-based intrusion detection/prevention tool. This tool can be a bit difficult to get setup, but it is cool when it finally works. Setup is technically more difficult than Security Onion, but it also takes less time. <br><br>
To use this tool: [depends on the version; see https://www.snort.org/documents#OfficialDocumentation] <br><br>
Setup/usage: https://www.snort.org/

### Suricata
My rating: **** / 5 <br><br>
Suricata feels like the much newer version of Snort. It's handy as an intrusion detection/prevention system, and is fairly striaghtforward to use/setup. It also allows multithreaded tasks, which means that processes can execute much faster than they can in Snort. This speed earns Suricata an extra star over Snort. <br><br>
To use this tool: [for latest instructions: https://suricata-ids.org/docs/]<br><br>
Setup/usage: https://suricata-ids.org/

### TCPDump
My rating: ** / 5 <br><br>
TCPDump just prints out packet content descriptions. It can be handy for glancing through specific packets, but is not the best tool for network and packet analysis anymore. It kind of feels like one of the original network analysis tools that never really got updated.<br><br>
To use this tool: ```tcpdump [ -AbdDefhHIJKlLnNOpqStuUvxX# ] [ -B buffer_size ]``` <br><br>
Setup/usage: https://www.tcpdump.org/manpages/tcpdump.1.html

### Wireshark
My rating: ***** / 5 <br><br>
Wireshark is a fantastic tool for both network capture and network traffic analysis, although its drawback is that it isn't the smallest, lightest-weight tool out there. Still, it has a pretty straight-forward graphical interface and is pretty easy to understand and use even for the first time user.<br><br>
To use this tool: https://www.wireshark.org/docs/<br><br>
Setup/usage: https://www.wireshark.org/

## IMAGE ANALYSIS
### Autopsy
My rating: **** / 5 <br><br>
Autopsy is a great tool for analyzing image files, but isn't capable of making said image files. One other drawback is that Autopsy's file analysis takes forever and ends up with many false positives on the credit card data category; it can't be trusted to autonomously do all analysis, basically. It is helpful in dividing up various files into their types, however, and is very user-friendly.<br><br>
To use this tool: https://www.sleuthkit.org/sleuthkit/docs.php<br><br>
Setup/usage: https://www.sleuthkit.org/autopsy/

### Event2Timeline
My rating: *** / 5 <br><br>
This is a very handy tool for dividing up specific log files into a timeline. It's pretty straight-forward to setup (they've even made it easy to install dependencies!) and has decent enough documentation to be able to understand how to use it quickly. Its downside is that it cannot parse all types of log files contained in a computer image file.<br><br>
To use this tool: ```event2timeline.py -c -f csv_filename.csv```<br><br>
Setup/usage: https://github.com/certsocietegenerale/event2timeline/blob/master/event2timeline.py

### EventViewer
My rating: **** / 5 <br><br>
This tool, which comes as part of Windows, is incredibly handy when going through event logs. It doesn't have the most easy-to-understand user interface, but, once you understand how it's laid out, this becomes an incredibly handy tool. This tool makes it easy to manually look through event logs, however, it doesn't do any of the analysis for you.<br><br>
To use this tool: Open it in Windows.<br><br>
Setup/usage: https://www.howtogeek.com/123646/htg-explains-what-the-windows-event-viewer-is-and-how-you-can-use-it/

### FTK Suite / FTK Imager
My rating: **** / 5 <br><br>
This is a great tool for both computer image analysis and capture. The interface is incredibly straightforward. The imager is free and is easier to get setup than the entire Suite is, but both are very helpful. The Suite does take quite a while to figure out how to get working, though.<br><br>
To use this tool: https://support.accessdata.com/hc/en-us/articles/204056525-FTK-User-Guide<br><br>
Setup/usage: https://accessdata.com/products-services/forensic-toolkit-ftk

### VirusTotal.com
My rating: ***** / 5 <br><br>
This website allows users to upload possibly malicious files/text/urls, and then checks to see if that text/signature/pattern is recognized as a virus in any other antivirus software. It's kept very updated and is straightforward to use, even for a first-time user. It's pretty effective at pointing out what is malicious versus what is probably not malicious.<br><br>
To use this tool: https://www.virustotal.com/ <br><br>
Setup/usage: [doesn't require setup]

### WinPreFetchView
My rating: *** / 5 <br><br>
This isn't the prettiest or most user-friendly tool, but it's efficient at doing its job; this small tool allows users to view the Windows PreFetch files easily and then export the data that they find/choose to export. It doesn't take up a lot of computer resources to do so, either!<br><br>
To use this tool: https://www.nirsoft.net/utils/win_prefetch_view.html<br><br>
Setup/usage: https://www.softpedia.com/get/System/System-Info/WinPrefetchView.shtml
