The suggestion that the target has used a insecure password means that a brute-forcer is likely the way to go. Using bitcracker we first have to generate the hashes:
/build/bitcracker-hash/ -o bitlocker-1-hash/ -i bitlocker-1.dd which should create a file hash_user_pass.txt.
Using the appropriate bitcracker executable (in my case bitcracker_cuda) and the rockyou wordlist,
./build/bitcracker_cuda -f bitlocker-1-hash/hash_user_pass.txt -d /usr/share/wordlists/rockyou.txt -t 8 -b 24 -g 0 -u. These options vary a lot but shouldn't matter for this short an attack:
================================================
Password found: jacqueline
================================================

Using dislocker to decrypt and mount:
dislocker -V bitlocker-2.dd -u=jacqueline -- /mnt/bitlocker-2-out/
mount -o loop /mnt/bitlocker-2-out/dislocker-file /mnt/clear

Read the flag.txt file in the newly mounted device and remember to umount your mount points