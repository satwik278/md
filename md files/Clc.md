<style>
  html {
    scroll-behavior: smooth;
  }
</style>

----

*<h1 align="center">Combinational Circuits</h1>*

----

<a id="up1"></a>

>####  Key Contents :
#

<details>
<summary>Combinational Circuits</summary>

- [Multiplexers](#mux)
- [Demultiplexers](#demux)
- [Encoders](#enc)
- [Decoders](#dec)
- [Arithmetic Logic Unit](#alu)
- [MOV instruction](#mov)
  
</details>

<details>
<summary>Realization with CMOS</summary>

- [2 to 1 MUX](#mux1)
- [1 to 2 DEMUX](#demux1)
- [4 to 2 ENC](#enc1)
- [2 to 4 DEC](#dec1)
- [ALU](#alu1)
- [MOV](#mov1)
  
</details>

#

>#####  Different Combinational Circuits :

#

```mermaid
graph TD
A[***Combinational Circuits***]--->B[Multiplexers]
A[***FCombinational Circuits***]--->C[Demultiplexers]
A[***Combinational Circuits***]--->C1[Encoders]
A[***Combinational Circuits***]--->C2[Decoders]

```
# 

*Some of the Combinational Circuits are :* 

- Multiplexers
- Demultiplexers
- Encoders
- Decoders

*Additional add ons :*

- Arithmetic Logic Unit
- MOV instruction Circuit

#

<a id="mux"></a>

> #####  Multiplexers :
#
A multiplexer takes $ 2^n $ inputs and gives $ 1 $ output. It uses $ n $ selection lines to select which input should be given at the output.

#
- **Logic symbol :**
#
![alt text](<Screenshot (123).png>)

*<h5 align="center">2 to 1 MUX</h5>*


#
- **Truth table :**
#

|S|A|B|Y|
|--|--|--|:--:|
|0|0|0|0|
|0|0|1|0|
|0|1|0|1|
|0|1|1|1|
|1|0|0|0|
|1|0|1|1|
|1|1|0|0|
|1|1|1|1|

# 

S stands for selection line.
A and B are the data inputs, and Y is the output.

#
[Go Up](#up1)


#

<a id="demux"></a>

> #####  Demultiplexers :
#
A demultiplexer takes $ 1 $ inputs and gives $ 2^n $ output. It uses $ n $ selection lines to select which output should contain the given input.

#
- **Logic symbol :**
#
![alt text](<Screenshot (124).png>)

*<h5 align="center">1 to 2 DEMUX</h5>*


#
- **Truth table :**
#

|I|S|Y1|Y2|
|--|--|--|:--:|
|0|0|0|_|
|0|1|_|0|
|1|0|1|_|
|1|1|_|1|


# 

S stands for selection line.
Y1 and Y2 are the outputs, and I is the output.

#
[Go Up](#up1)
#


<a id="enc"></a>

> #####  Encoders :
#
An Encoder takes $ 2^n $ inputs and gives $ n $ outputs.

#
- **Logic symbol :**
#
![alt text](<Screenshot (132).png>)

*<h5 align="center">4 to 2 ENC</h5>*


#
- **Truth table :**
#

|D0|D1|D2|D3|Y0|Y1|
|:--:|:--:|:--:|:--:|:--:|:--:|
|1|0|0|0|0|0|
|0|1|0|0|0|1|
|0|0|1|0|1|0|
|0|0|0|1|1|1|


# 

D0,D1,D2,D3 are the inputs.
Y0,Y1 are the outputs.

#
[Go Up](#up1)
#

<a id="dec"></a>

> #####  Decoders :
#
A Decoder takes $ n $ inputs and gives $ 2^n $ outputs.

#
- **Logic symbol :**
#
![alt text](<Screenshot (126).png>)

*<h5 align="center">2 to 4 DEC</h5>*


#
- **Truth table :**
#

|D0|D1|Y0|Y1|Y2|Y3|
|:--:|:--:|:--:|:--:|:--:|:--:|
|0|0|1|0|0|0|
|0|1|0|1|0|0|
|1|0|0|0|1|0|
|1|1|0|0|0|1|


# 

D0,D1 are the inputs.
Y0,Y1,Y2,Y3 are the outputs.


#
[Go Up](#up1)
#

<a id="alu"></a>

> #####  Arithmetic Logic Unit :
#

An Arithmetic Logic Unit is a combinational logic circuit that can perform various arithmetic and logical opertaions like additon,subtraction,multiplication,divison,and,or,not,etc.

The given ALU performs addition and multiplcation of two $ 1 $ bit numbers.

It consists of a full adder circuit, AND gate and, a $2$ to $1$ MUX to select the desired output.

The reason for using a full adder circuit instead of half adder is that, when multibit operations have to be performed, two or more circuits of these can be connected together to achieve the output.

#
- **Logic symbol :**
#
![alt text](<Screenshot (133).png>)

*<h5 align="center">ALU</h5>*

#
- **Truth table :**
#

|A|B|C|S|Y|
|--|--|--|--|--|
|0|0|X|0|0|
|0|0|X|1|0|
|0|1|X|0|0|
|0|1|X|1|1|
|1|0|X|0|0|
|1|0|X|1|1|
|1|1|X|0|1|
|1|1|X|1|0|
#


A,B,C are the inputs and Y is the output of the MUX.
S is the selection line of the MUX which selects whether the output is sum or product.
The input C need not to be given everytime, we can set it to zero for performing operations between A and B.

#
[Go Up](#up1)
#

<a id="mov"></a>

> #####  MOV instruction  :
#

The MOV instruction is used to copy data from one location to another in assembly language programming.

MOV Destination, Source is the syntax for moving data between two locations.

Examples: 
- MOV A,B
- MOV A,#25H
- MOV P1,A

#
- **Logic symbol :**
#
![alt text](<Screenshot (134).png>)

*<h5 align="center">MOV</h5>*

#

The output of the B register is given to the input of first AND gate. 

An enable signal is given to both of the AND gates. When the enable input is HIGH the AND gates are activated and the data provided to them will be flowed to the Register A.

The flow of data from Register B to Register A takes some clock cycles.

#

>####  Realization with CMOS :
#
<a id="mux1"></a>

>###### 2 to 1 MUX :
#
![alt text](<Screenshot (128).png>)
#
[Go Up](#up1)
#
<a id="demux1"></a>

>###### 1 to 2 DEMUX :
#
![alt text](<Screenshot (129).png>)
#
[Go Up](#up1)
#
<a id="enc1"></a>

>###### 4 to 2 ENC :
#
![alt text](<Screenshot (130).png>)
#
[Go Up](#up1)
#
<a id="dec1"></a>

>###### 2 to 4 DEC :
#
![alt text](<Screenshot (131).png>)
#
[Go Up](#up1)
#


<a id="alu1"></a>

>###### ALU :
#
![alt text](<Screenshot (139).png>)
#
[Go Up](#up1)
#


<a id="mov1"></a>

>###### MOV :
#
![alt text](<Screenshot (135).png>)
#
[Go Up](#up1)
#

