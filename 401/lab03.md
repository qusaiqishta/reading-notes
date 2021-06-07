# Reading and Writing files in python 

## What is a file ?
At its core, a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.


##Files on most modern file systems are composed of three main parts:

- Header: metadata about the contents of the file (file name, size, type, and so on)

- Data: contents of the file as written by the creator or editor

- End of file (EOF): special character that indicates the end of the file


## File Paths

- Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

- File Name: the actual name of the file

- Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

## Character Encodings

An encoding is a translation from byte data to human readable characters. This is typically done by assigning a numerical value to represent a character. The two most common encodings are the ASCII and UNICODE Formats. ASCII can only store 128 characters, while Unicode can contain up to 1,114,112 characters.parsing a file with the incorrect character encoding can lead to failures or misrepresentation of the character. For example, if a file was created using the UTF-8 encoding, and you try to parse it using the ASCII encoding, if there is a character that is outside of those 128 values, then an error will be thrown.


## Opening and Closing a File in Python
This is done by invoking the open() built-in function

```
file = open('dog_breeds.txt')

```

When you’re manipulating a file, there are two ways that you can use to ensure that a file is closed properly, even when encountering an error. The first way to close a file is to use the try-finally block:


```
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()

```


The second way to close a file is to use the with statement:
```
with open('dog_breeds.txt',charecter) as reader:
    # Further file processing goes here
 ```


Character:
'r'	Open for reading (default)

'w'	Open for writing, truncating (overwriting) the file first

'rb' or 'wb'	Open in binary mode (read/write using byte data)


# Raising an Exception

We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.


If you want to throw an error when a certain condition occurs using raise, you could go about it like this:
```
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
When you run this code, the output will be the following:

```

```
Traceback (most recent call last):
  File "<input>", line 4, in <module>
Exception: x should not exceed 5. The value of x was: 10

```


## The try and except Block: Handling Exceptions

The try and except block in Python is used to catch and handle exceptions. Python executes code following the try statement as a “normal” part of the program. The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.

![](https://files.realpython.com/media/try_except.c94eabed2c59.png)


```
try:
    with open('file.log') as file:
        read_data = file.read()
except FileNotFoundError as fnf_error:
    print(fnf_error)
 ```
In this case, if file.log does not exist, the output will be the following:
```
[Errno 2] No such file or directory: 'file.log'
```


## Finally and else 

![](https://files.realpython.com/media/try_except_else_finally.a7fac6c36c55.png)


else statement run when there is no exception while finally statement always run