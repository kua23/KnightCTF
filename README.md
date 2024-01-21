# KnightCTF

## Levi Ackerman

Ran `exiftool`, no fruitful results
Huffman coding, little endian.

binwalk -e shows a hidden file in the .jpg of tiff data type

Oh wait! It's a web exploitation
Robots stands for the robots.txt, basically a text file which prevents robots from spidering into the website's directories which contains sensitive data.
![image](https://github.com/kua23/KnightCTF/assets/61975172/442aadf1-a350-4326-bc90-013f7b617075)
Going into the `robots.txt` file, we can find that the bots are disallowed from going into the /l3v1_4ck3rm4n.html.
![image](https://github.com/kua23/KnightCTF/assets/61975172/8f1a0ad4-7d09-46cf-b290-07a19cef7a0a)

If we go there manually, we get the flag
![image](https://github.com/kua23/KnightCTF/assets/61975172/36526cd2-e0e3-420a-b24d-3d6d47cb3a2d)

### Flag

KCTF{1m_d01n6_17_b3c4u53_1_h4v3_70}

## Kitty

![image](https://github.com/kua23/KnightCTF/assets/61975172/91efe3c5-e2be-4316-bc34-a3051e527bbd)
We first get a login page, with a username and password. 
Inspecting the source and typing a gibberish username and password, we get
![image](https://github.com/kua23/KnightCTF/assets/61975172/68b2900d-6e67-434d-8599-fe3abffef0e5)
The username and password is actually just `Username` and `Password` respectively.
Upon logging again, we get into another page
![image](https://github.com/kua23/KnightCTF/assets/61975172/9ee80982-cf11-49f2-a3a3-bee893919a41)
If we Inspect the page again, we get 
![image](https://github.com/kua23/KnightCTF/assets/61975172/fdc17db9-0e65-48b8-83f3-c7d4899eab66)
We see that, if the cat flag text command is executed, the POST method is executed which means that if we type the command, we get the flag
![image](https://github.com/kua23/KnightCTF/assets/61975172/267190d7-123e-4064-8ea2-4c73e6022c8e)

### Flag
`KCTF{Fram3S_n3vE9_L1e_4_toGEtH3R}`

## Oceanic

A .tar file is given which when extracted provides a peaceful.wav file and a clue.png file.
On using `exiftool` on the .png file, we get an encoded comment.
![image](https://github.com/kua23/KnightCTF/assets/61975172/e228e685-e659-4da5-9ce7-4ab,c0a113c3b)
Using (CacheSleuth)[https://www.cachesleuth.com/multidecoder/], we get a base 58 message
![image](https://github.com/kua23/KnightCTF/assets/61975172/52c68540-b9de-43f8-8ee7-e73b79c18b01)
which is `theoceanisactuallyreallydeeeepp`.
Then, on opening the .wav file using the DeepSound tool, and entering the password as the comment, we get a file called flag.png.

On then using `binwalk -e flag.png` 
![image](https://github.com/kua23/KnightCTF/assets/61975172/835f57b5-6b2f-4119-b4c0-76c9c5982b6b)

### Flag 
KCTF{mul71_l4y3r3d_57360_ec4dacb5}

## 


