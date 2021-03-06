#CPSC 223P - Python Programming

__Author Name:__ Kathy Saad<br>
__Project Title:__ Assignment 2 - Vigenere Cipher<br>
__Project Status:__ Working<br>
__External Resources:__<br>
- Class notes<br>
- https://www.python.org/<br>
- http://inventwithpython.com/hacking/chapter19.html<br>
- http://rosettacode.org/wiki/Vigen%C3%A8re_cipher#Python<br>
- http://web.cs.mun.ca/~michael/c/ascii-table.html

*******************************************************************************************************************************************

__Instructions:__

_PART 1_<br>
Write a program named vigenerecipher.py that takes a file name and a code word/phrase as arguments. Open the file and use the Vigenère cipher to encode the contents of the file according to the cipher. The program should output the cipher text into 'filename'-cipher.txt where 'filename' was the original file name. For example, if the file's name is message.txt the ciphered text would be saved in message-cipher.txt.
The Vigenère cipher is a polyalphabetic substitution cipher. It is a variation of Caesar's cipher where the alphabet is shifted by a fixed number of letters. For example, if the alphabet is shifted by eight, then the unshifted alphabet (first line) will map the following letters (second line):<br>
&nbsp;&nbsp;&nbsp;&nbsp;ABCDEFGHIJKLMNOPQRSTUVWXYZ<br>
&nbsp;&nbsp;&nbsp;&nbsp;IJKLMNOPQRSTUVWXYZABCDEFGH
 
The Vigenère cipher uses 26 alphabets that are each progressive shifted from 0 to 26. The code word provides an index into which one of the shifted alphabets will be used to cipher each letter of the clear text message into cipher text. For example, the clear text is "The eagle has landed" and the code word is "lime".<br>
&nbsp;&nbsp;&nbsp;&nbsp;The eagle has landed<br>
&nbsp;&nbsp;&nbsp;&nbsp;lim elime lim elimel
 
The first letter 'T' is ciphered using the alphabet that matches 'l', which is a shift of 12 letters; 'l' is the twelfth letter of the alphabet. The next letter 'h' matches 'i' which is a shift of 9 letters, etc.
The above text would be ciphered to:<br>
&nbsp;&nbsp;&nbsp;&nbsp;Epq iloxi sie plvpio

_PART 2_<br>
Write a program named vigeneredecipher.py that takes a file name and a code word/phrase as arguments. Open the file and use the Vigenère cipher to decode the contents of the file according to the cipher. The program should output the clear text into 'filename'-clear.txt where 'filename' was the original file name. For example if the input is message-cipher.txt the output of the program is saved in message-cipher-clear.txt.

*******************************************************************************************************************************************

__Sample Run:__

	[CIPHER]
	$python3.4 vigenerecipher.py message.txt lime
	$cat message-cipher.txt
	Epq iloxi sie plvpio

	[DECIPHER]
	$python3.4 vigeneredecipher.py message.txt lime
	$cat message-clear.txt
	The eagle has landed
