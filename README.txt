Reed–Solomon error correction

For run the script

	python reed_solomon_code.py --message="Desired text"

when:
    message (str) - Human readable string. 
		    Default value ("We were all a little drunk with spring, like the fat bees reeling from flower to flower, and a strange insurrectionary current ran among us")

*****For run the script with a default value
	
	python reed_solomon_code.py

The program will print sentence, encoding the message, in few index create erroes, find errors and correct them.
In addition the software chect software integrity

==========================
Example of code execution
==========================

Sentence to encode and test 'Reed–Solomon code'
"We were all a little drunk with spring, like the fat bees reeling from flower to flower, and a strange insurrectionary current ran among us"
Length of message: 139

Message codeword: 
[87, 101, 32, 119, 101, 114, 101, 32, 97, 108, 108, 32, 97, 32, 108, 105, 116, 116, 108, 101, 32, 100, 114, 117, 110, 107, 32, 119, 105, 116, 104, 32, 115, 112, 114, 105, 110, 103, 44, 32, 108, 105, 107, 101, 32, 116, 104, 101, 32, 102, 97, 116, 32, 98, 101, 101, 115, 32, 114, 101, 101, 108, 105, 110, 103, 32, 102, 114, 111, 109, 32, 102, 108, 111, 119, 101, 114, 32, 116, 111, 32, 102, 108, 111, 119, 101, 114, 44, 32, 97, 110, 100, 32, 97, 32, 115, 116, 114, 97, 110, 103, 101, 32, 105, 110, 115, 117, 114, 114, 101, 99, 116, 105, 111, 110, 97, 114, 121, 32, 99, 117, 114, 114, 101, 110, 116, 32, 114, 97, 110, 32, 97, 109, 111, 110, 103, 32, 117, 115, 16, 11, 69, 249, 69, 179, 52, 212, 90, 112, 178, 93, 39, 119, 69, 244, 109, 36, 182, 78, 152, 164, 249, 85, 239, 56, 27, 97, 158, 159, 240, 131, 65, 194, 40, 59, 195, 81, 46, 83, 145, 214, 11, 97, 204, 158, 113, 158, 85, 146, 93, 80, 202, 46, 82, 154, 244, 82, 175, 191, 174, 206, 47, 157, 214, 225, 4, 218, 18, 132, 134, 150, 23, 6, 149, 21, 166, 190, 111, 18, 51, 86, 241, 92, 244, 241, 71, 14, 60, 151, 140, 217, 58, 245, 241, 130, 152, 132, 138, 56, 69, 83, 69, 251, 42, 223, 244, 160, 191, 162, 6, 188, 122, 48, 9, 180, 5, 36, 133, 22, 220, 102, 212, 49, 232, 222, 156, 62, 113, 202, 84, 201, 229, 225, 191, 134, 92, 221, 25]

Introduce errors/erasures
Error one index: 46, value error: 69
Error two index: 69, value error: 37
Error three index: 119, value error: 78

Message codeword (with three errors/erasures): 
[87, 101, 32, 119, 101, 114, 101, 32, 97, 108, 108, 32, 97, 32, 108, 105, 116, 116, 108, 101, 32, 100, 114, 117, 110, 107, 32, 119, 105, 116, 104, 32, 115, 112, 114, 105, 110, 103, 44, 32, 108, 105, 107, 101, 32, 116, 69, 101, 32, 102, 97, 116, 32, 98, 101, 101, 115, 32, 114, 101, 101, 108, 105, 110, 103, 32, 102, 114, 111, 37, 32, 102, 108, 111, 119, 101, 114, 32, 116, 111, 32, 102, 108, 111, 119, 101, 114, 44, 32, 97, 110, 100, 32, 97, 32, 115, 116, 114, 97, 110, 103, 101, 32, 105, 110, 115, 117, 114, 114, 101, 99, 116, 105, 111, 110, 97, 114, 121, 32, 78, 117, 114, 114, 101, 110, 116, 32, 114, 97, 110, 32, 97, 109, 111, 110, 103, 32, 117, 115, 16, 11, 69, 249, 69, 179, 52, 212, 90, 112, 178, 93, 39, 119, 69, 244, 109, 36, 182, 78, 152, 164, 249, 85, 239, 56, 27, 97, 158, 159, 240, 131, 65, 194, 40, 59, 195, 81, 46, 83, 145, 214, 11, 97, 204, 158, 113, 158, 85, 146, 93, 80, 202, 46, 82, 154, 244, 82, 175, 191, 174, 206, 47, 157, 214, 225, 4, 218, 18, 132, 134, 150, 23, 6, 149, 21, 166, 190, 111, 18, 51, 86, 241, 92, 244, 241, 71, 14, 60, 151, 140, 217, 58, 245, 241, 130, 152, 132, 138, 56, 69, 83, 69, 251, 42, 223, 244, 160, 191, 162, 6, 188, 122, 48, 9, 180, 5, 36, 133, 22, 220, 102, 212, 49, 232, 222, 156, 62, 113, 202, 84, 201, 229, 225, 191, 134, 92, 221, 25]

Error count:  3
Located errors:  [119, 69, 46]
Decoded message:  [87, 101, 32, 119, 101, 114, 101, 32, 97, 108, 108, 32, 97, 32, 108, 105, 116, 116, 108, 101, 32, 100, 114, 117, 110, 107, 32, 119, 105, 116, 104, 32, 115, 112, 114, 105, 110, 103, 44, 32, 108, 105, 107, 101, 32, 116, 104, 101, 32, 102, 97, 116, 32, 98, 101, 101, 115, 32, 114, 101, 101, 108, 105, 110, 103, 32, 102, 114, 111, 109, 32, 102, 108, 111, 119, 101, 114, 32, 116, 111, 32, 102, 108, 111, 119, 101, 114, 44, 32, 97, 110, 100, 32, 97, 32, 115, 116, 114, 97, 110, 103, 101, 32, 105, 110, 115, 117, 114, 114, 101, 99, 116, 105, 111, 110, 97, 114, 121, 32, 99, 117, 114, 114, 101, 110, 116, 32, 114, 97, 110, 32, 97, 109, 111, 110, 103, 32, 117, 115, 16, 11, 69, 249, 69, 179, 52, 212, 90, 112, 178, 93, 39, 119, 69, 244, 109, 36, 182, 78, 152, 164, 249, 85, 239, 56, 27, 97, 158, 159, 240, 131, 65, 194, 40, 59, 195, 81, 46, 83, 145, 214, 11, 97, 204, 158, 113, 158, 85, 146, 93, 80, 202, 46, 82, 154, 244, 82, 175, 191, 174, 206, 47, 157, 214, 225, 4, 218, 18, 132, 134, 150, 23, 6, 149, 21, 166, 190, 111, 18, 51, 86, 241, 92, 244, 241, 71, 14, 60, 151, 140, 217, 58, 245, 241, 130, 152, 132, 138, 56, 69, 83, 69, 251, 42, 223, 244, 160, 191, 162, 6, 188, 122, 48, 9, 180, 5, 36, 133, 22, 220, 102, 212, 49, 232, 222, 156, 62, 113, 202, 84, 201, 229, 225, 191, 134, 92, 221, 25]

Test the integrity of the software
The lists are identical
The software works properly





