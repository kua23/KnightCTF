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

##
