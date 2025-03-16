Looking at the hint we are provided we can tell this is an affine transformation. 

When we run the challenge we get a netcat instance that can be used as an encryption oracle (i.e we can choose a plaintext for it to encrypt), with the caveat we must provide the name of a cheese. 

By choosing a choose of our choice (I used "brie") we can recover the key (a,b in affine(x) = bx+a), which we can use to decrypt the encrypted cheese to be handed the flag.

picoCTF{ChEeSy696d4adc}