Using volatility 2 to inspect the memory dump, (of which the final version on the github page must be used) we can use one of many plugins such as breppo's bitlocker to decrypt the full volume encryption key (fvek). 
vol.py --profile=Win10x64_10941 -f memdump.mem
Once these are obtained we can use dislocker to decrypt the disk image and read the flag.
This can be done in one line with 
vol.py --profile=Win10x64_10941 -f memdump.mem --dislocker ./bitlocker-2-out.