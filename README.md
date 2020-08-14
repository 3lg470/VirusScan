# VirusScan your files with the VirusTotal API

 This script will scan a single file or full directories for known viruses, using the VirusTotal Service API.
 The script assumes you are using a Free/Public API key, and hence throttles requests to 4/minute.  If you have
   a paid key, you can remove the sleep.

 REQUIREMENTS: API Key in .apikey file

 OUTPUT: Will print to screen info about current file being processed.
   If malicious content is found, will print a Result and Verdict for each file 


# RUNNING THE SCRIPT:

# GET HELP
╰─⠠⠵ ./vScan.sh -h

This script will scan individual files or full directories for viruses w/ VirusTotal

Usage : ./vScan.sh [OPTION] {DATA}

  Options:
  
     -f [file]        Single file scan
     
     -d [directory]   Full directory scan
     
     -h               Help
     
# SCAN SINGLE FILE
╰─⠠⠵ ./vScan.sh -f ~/Downloads/eicar_com.zip

processing /home/usera/Downloads/eicar_com.zip

                    "result": "Malicious (score: 85)"
                    "result": "malware (ai score=100)"
-------------------------


# SCAN FULL DIRECTORY
╰─⠠⠵ ./vScan.sh -d ~/Downloads/testDir 

processing /home/usera/Downloads/testDir/eicar_com.zip

                    "result": "Malicious (score: 85)"
                    "result": "malware (ai score=100)"
-------------------------
processing /home/usera/Downloads/testDir/garbage.txt


-------------------------

