Image Steganography in C

Overview

Image Steganography is a C programming project that implements encoding and decoding of secret messages using the Least Significant Bit (LSB) technique in BMP images.

The project demonstrates bitwise manipulation, binary file handling, and modular programming in C.

Features:
1.Encode secret files into BMP images using the Least Significant Bit (LSB) technique.
2.Decode and retrieve hidden data from encoded images.
3.Support multiple secret-file formats, including .txt, .c, .cpp, .py, and .sh, provided the implementation handles their contents as raw bytes.
4.Perform byte-level data manipulation using bitwise operations.
5.Handle file operations using C standard library functions.
6.Organize encoding and decoding functionality into modular source and header files.

Technologies Used
1.C Programming
2.Bitwise Operations
3.Pointers and Arrays
4.File Handling
5.Binary Data Processing
6.Structures
7.Modular Programming

Project Structure

The project is organized into separate source files and header files for encoding, decoding, and supporting operations.

main.c — Program entry point
encode.c and related files — Encoding functionality
decode source files — Decoding functionality
encode.h and decode.h — Header files
common.h — Shared declarations and definitions

How It Works:

Encoding Process

1.Accept the source BMP image and secret file as input.
2.Validate the input files, file extensions, and encoding requirements.
3.Calculate the required capacity to store the secret file in the BMP image.
4.Copy the BMP header to preserve the image structure.
5.Encode the secret file extension and file size into the image using LSB manipulation.
6.Embed the secret file data byte by byte into the image's pixel data using Least Significant Bit (LSB) techniques.
7.Generate the output BMP image containing the hidden data.

Decoding Process

1.Accept the encoded BMP image as input.
2.Validate the image and identify the hidden data.
3.Extract the secret file extension and file size.
4.Retrieve the hidden data from the image using LSB extraction.
5.Reconstruct the original secret file using the extracted data.
6.Save the decoded file with its original extension.

Supported File Types
The project supports encoding and decoding different types of files, including:
C source files (.c)
C++ source files (.cpp)
Text files (.txt)
Python files (.py)
Shell scripts (.sh)
File support depends on the implementation's file-handling logic and validation rules.


Build and Execution
Compilation

Compile the source files using GCC:
gcc *.c -o steganography
gcc *.c

Encoding
Hide a secret file inside a BMP image using LSB(Least Significant Bit) encoding.
Command:
./stegnography -e beautiful.bmp secret.cpp
./stegnography -e beautiful.bmp secret.cpp stego.bmp
./a.out -e beautiful.bmp secret.cpp stego.bmp

Sample Output:
                Encoding Process Started

Validation of encode arguments done successfully.
Files were opened successfully.
width = 1024
height = 768
Capacity checking done successfully.
Copied header bytes from src to dest done successfully.
Magic string encoding done successfully.
Secret file extension encoding done successfully.
Secret file data encoding done successfully.
Remaining img data copied to output file successfully.

              Encoding Process Ended

Decoding
Extract the hidden file from the stego image.
Command:
./steganography -d stego.bmp decoded
./a.out -d stego.bmp decoded

Sample Output:
              Decoding Process Started

Decode arguments validation done successfully.
Img file is opened successfully.
Magic string decoded successfully.
Decoding the secret file done successfully.
Decoding the secret file data done successfully.

              Decoding Process Ended
The decoded file will be generated with its original extension.

Error Handling:
Tested with a non-existent secret file.
Command:
./steganography -e beautiful.bmp Akash.cpp

Sample Output:

Validation of encode arguments done successfully.
fopen: No such file or directory
ERROR: Unable to open file Akash.cpp

The application handles file-opening errors and displays an appropriate error message.


Learning Outcomes:
1.Practical application of bitwise operations.
2.Understanding of binary file I/O in C.
3.Experience with pointers, arrays, strings,and structures.
4.Modular code organization.
5.Debugging and handling file-processing operations.

Future Improvements
1.Improve input validation and error handling.
2.Add more comprehensive test cases.
3.Support additional image formats where appropriate.
4.Improve memory and file-resource management.

Author
Akash Mangi

Electronics and Communication Engineering Graduate
Interested in C Programming, Embedded Systems, and Embedded Software Development


