# Steganography-App

App is divided into two main components :
The first is the encrpyt method which opens a file, prints the relevant file information, and encrypts the message into the picture. The encrypt method first reads 3 characters from the message to be encoded and converts these characters to their int ASCII values. We then pad 0s to the left hand side for each of these characters to ensure that they are 8 bits long. Then, we get the rgb value from each pixel and convert this old rgb value to a new one depending on how what the encoding system is. The encoding system in our project consists of making sure that a 0 is encoded if the individual component of the rgb value (i.e. red, blue, and green) is even, and a 1 is encoded if the individual component is odd. Therefore, we are able to encode three bits of information per pixel and require at least 3 pixels to encode a single character. 

The second part of the project is decrpyt. The decrypt method starts by reading 3 bytes of data (or 8 pixels) from the image. Each byte of data is converted to a char and stored. This process continues until it reaches a NULL character or the end of the image file.
