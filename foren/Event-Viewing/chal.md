There is a windows event log folder you can open with the event viewer app.

There are three parts to this challenge:

Step 1:
Looking through the logs, you will find a suspicious executable which downloaded Totally-Legit-Software.exe published by cGljb0NURntFdjNudF92aTN3djNyXw== or picoCTF{Ev3nt_vi3wv3r_1s

Step 2:
It created a registry key in \Software\Microsoft\Windows\CurrentVersion\Run to run custom_shutdown.exe with a value name of Immediate Shutdown (MXNfYV9wcjN0dHlfdXMzZnVsXw==) or a_pr3tty_us3ful_

Step 3:
Filtering by event ID 1074 (system shutdown by process) we find that the system is shut down repeatedly with a comment dDAwbF84MWJhM2ZlOX0= or t00l_81ba3fe9}

picoCTF{Ev3nt_vi3wv3r_1s_a_pr3tty_us3ful_t00l_81ba3fe9}