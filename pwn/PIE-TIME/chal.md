Open the executable in gdb, find address of the flag function win with info address win which will give an address ending in 2a7. 

The program prints the address of main at runtime which ends in 33d. Connect to the remote server, change the last three digits of the address it provides to 2a7 which gives the flag. 

picoCTF{b4s1c_p051t10n_1nd3p3nd3nc3_cb52e722}