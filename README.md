# EXPERIMENT--01-ALP-FOR-8086
Name : Shaik Sameer Basha

Roll No: 212222240093

Date of experiment : 





## Aim: 
To Write and execute ALP on fundamental arithmetic and logical operations
## Components required: 
8086  emulator 
## Theory : 
Running The Emulator (emu8086) Intro 8086 Microprocessor Emulator, also known as EMU8086, is an emulator of the program 8086 microprocessor. It is developed with a built-in 8086 assembler. This application is able to run programs on both PC desktops and laptops. This tool is primarily designed to copy or emulate hardware. These include the memory of a program, CPU, RAM, input and output devices, and even the display screen. There are instructions to follow when using this emulator. It can be executed into one of the two ways: backward or forward. There are also examples of assembly source code included. With this, it allows the programming of assembly language, reverse engineering, hardware architecture, and creating miniature operating system (OS). The user interface of 8086 Microprocessor Emulator is simple and easy to manage. There are five major buttons with icons and titles included. These are “Load”, “Reload”, “Step Back”, “Single Step”, and “Run”. Above those buttons is the menu that includes “File”, “View”, “Virtual Devices”, “Virtual Drive”, and “Help”. Below the buttons is a series of choices that are usually in numbers and codes. At the leftmost part is an area called “Registers” with an indication of either “H” or “L”. The other side is divided into two, which enables users to manually reset, debug, flag, etc. What is 8086 emulator emu8086 is an emulator of Intel 8086 (AMD compatible) microprocessor with integrated 8086 assembler and tutorials for beginners. Emulator runs programs like the real microprocessor in step-by-step mode. it shows registers, memory, stack, variables and flags.


 ## Running the Emulator :
1.	Download and install emu8086 (www.emu8086.com) It is usually installed in C:\EMU8086 subfolder in the “Windows” directory
2.	  Run  emu8086 icon (on the desktop or in the c:\EMU8086 folder of window) It has green color 
 
 
3.		write the code for the appropriate program for ADDITION,SUBTRACTION, MULTIPLICATION,  DIVISION operations.

4.	 Compile the program and check for the errors 
5.	Run (once there is no syntax error) 

6.	Click OK to see/view the output of your program on the Emulator screen. 


7.	After running the program, another menu screen will be displayed, where you have the option to “View” symbol table,
8.	 


![image](https://user-images.githubusercontent.com/36288975/189273263-d65baae9-4b8f-4723-afb3-c0ffa4052b04.png)











9.	Click on emulate to start emulation 








![image](https://user-images.githubusercontent.com/36288975/189273273-9bb36ec1-e2e8-4892-8d35-37707332bfdc.png)








10.	If no errors are found click on run the program and check the status of various flags in the flags tab as shown below 






![image](https://user-images.githubusercontent.com/36288975/189273277-113a2a33-4a40-4ff8-95a5-ecd3a1f504fe.png)







## Programs for arithmetic  operations

## Addition of 8 bit ALP : 
```
org 100h  
MOV SI,1200h;
MOV CL,00h;
MOV AL,08H;
MOV BL,09H;
ADD AL,BL;
JNC L1;
INC CL;
L1:MOV [SI],AL;
MOV [SI+2],CL;
HLT;
```

## Output  
![1 1](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/6dbfd964-432c-462b-9360-eba13baa2871)



## Subtraction of 8 bit numbers ALP : 
 ```
org 100h
MOV SI,1200h;
MOV CL,00h;
MOV AL,08H;
MOV BL,07H;
SUB AL,BL;
JNC L1;
NEG AL;
INC CL;
L1:MOV [SI],AL;
MOV [SI+1],CL;
HLT;
```

## Output 

![1 2](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/e2ed575e-f677-459f-ad8e-ca8cb798c54e)


## Multiplication of 8 bit numbers ALP :
```
org 100h  
MOV SI,1200h;
MOV CL,00h;
MOV AL,10H;
MOV BL,03H;
MUL BL;
MOV [SI],AL;
MOV [SI+1],AH;
HLT;
```

 ## Output  

![1 3](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/7d5a0807-b23a-497d-8383-5fb78409f3be)


## Division of 8 bit numbers ALP :
```
org 100h  
MOV SI,1200h;
MOV CL,00h;
MOV AL,15H;
MOV BL,04H;
DIV BL;
MOV [SI],AL;
MOV [SI+1],AH;
HLT;
```

## Output  
![1 4](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/f2d4da12-5d2c-44f2-a3f3-21bda9704f8d)
## Programs for logical  operations

## AND
```python
org 100h
MOV bx,1000h;
AND bx,1111h;
MOV [0040h+02],bx;
ret
```
## Output 

![1 5](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/edec7e8e-afd6-4114-8b2a-8730ba443005)

## OR
```python
org 100h
MOV ax,[0070h];
MOV bx,1000h;
OR ax,bx;
MOV [0060h],ax;
ret
```
## Output

![1 6](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/b0661c3b-8a1b-4196-8b54-98f27e9dd218)

## NOT
```python
org 100h
MOV bx,0060h;
MOV ax,[bx]; 
NOT al;
MOV [0060h+04],ax;
ret
```
## Output
![1 7](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/b4fdb0ed-adf0-4b0d-917a-7bb54070e596)


## XOR
```python
org 100h
MOV bx,0050h;
MOV ax,[bx]; 
XOR ax,bx;
MOV [0050h+03],ax;
ret
```
## Output

![1 8](https://github.com/shaikSameerbasha5404/EXPERIMENT--01-ALP-FOR-8086/assets/118707756/406cf04c-daf4-4b99-8068-9312fcf7d80c)


## Result :
Thus, a program is executed on ALP for the fundamental arithmetic and logical operations.
 







