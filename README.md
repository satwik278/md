<style>
  html {
    scroll-behavior: smooth;
  }
</style>

----

<a id="lgs"></a>

*<h1 align="center">Logic Gates</h1>*

----

<a id="kc"></a>

>####  Key Contents :
#

<details>
<summary>Basic Gates</summary>

- [AND Gate](#and)
- [OR Gate](#or)
- [NOT Gate](#not)
  
</details>

<details>
<summary>Universal Gates</summary>

- [NAND Gate](#nand)
- [NOR Gate](#nor)
  
</details>

<details>
<summary>Exclusive Gates</summary>

- [EX-OR Gate](#xor)
- [EX-NOR Gate](#xnor)
  
</details>

<details>
<summary>Realization of Basic Gates with Universal Gates</summary>

<details>
<summary>Realization with NAND</summary>

- [AND Gate](#and1)
- [OR Gate](#or1)
- [NOT Gate](#not1)

  
</details>

<details>
<summary>Realization with NOR</summary>

- [AND Gate](#and2)
- [OR Gate](#or2)
- [NOT Gate](#not2)
  
</details>
  
</details>


<details>
<summary>Realization of Basic Gates with CMOS</summary>

- [AND Gate](#and3)
- [OR Gate](#or3)
- [NOT Gate](#not3)
- [NAND Gate](#nand1)
- [NOR Gate](#nor1)
- [EX-OR Gate](#xor1)
- [EX-NOR Gate](#xnor1)
  
</details>
  
</details>

<details>

<summary>Go To</summary>

- [Flip Flops](#ffs)
- [Combinational Circuits](#clc)

</details>

#
>####  Classifications of logic gates :
#
```mermaid
graph TD
A[***Logic Gates***]--->B[Basic Gates]
A[***Logic Gates***]--->C[Universal Gates]
A[***Logic Gates***]--->C1[Exclusive Gates]
B[**Basic Gates**]-->D[_AND Gate_]
B[**Basic Gates**]-->E[_OR Gate_]
B[**Basic Gates**]-->F[_NOT Gate_]
C[**Universal Gates**]-->G[_NAND Gate_]
C[**Universal Gates**]-->H[_NOR Gate_]
C1[**Exclusive Gates**]-->I[_EX-OR Gate_]
C1[**Exclusive Gates**]-->J[_EX-NOR Gate_]
```

#

*Logic Gates are classified into three types:* 
- Basic gates 
- Universal gates
- Exclusive gates
#

>####  Basic  gates :
#
<a id="and"></a>

> ######  AND GATE :
#
- **Logic symbol :**
#
![alt text](<Screenshot (94).png>)
#
- **Truth table :**


|A|B|A.B|
|--|--|:--:|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|1|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "A·B", "wave": "0001", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

The output will be HIGH if and only if all the inputs are HIGH. 
 #
[Go Up](#kc)
#
<a id="or"></a>

> ######  OR GATE :
#
- **Logic symbol :**
#
![alt text](<Screenshot (95).png>)
#

- **Truth table :**


|A|B|A+B|
|--|--|--|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "A+B", "wave": "0111", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

The output will be LOW if and only if all the inputs are LOW.

 #
[Go Up](#kc)

#
<a id="not"></a>

> ######  NOT GATE :
#
- **Logic symbol :**
#
![alt text](<Screenshot (100).png>)
#

- **Truth table :**

#

|A|Y|
|--|--|
|0|1|
|1|0|
|0|1|
|1|0|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "Y", "wave": "1010", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

The output will be complement of the input. 
#
 
[Go Up](#kc)

#
>####  Universal  gates :
#

<a id="nand"></a>

> ######  NAND GATE :
#
- **Logic symbol :**
#
![alt text](<Screenshot (96).png>)
#
- **Truth table :**
#

|A|B|Y|
|--|--|--|
|0|0|1|
|0|1|1|
|1|0|1|
|1|1|0|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "Y", "wave": "1110", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

The output will be LOW if and only if all the inputs are HIGH. 
#
 
[Go Up](#kc)

#

<a id="nor"></a>

> #####  NOR GATE :
#
- **Logic symbol :**
#
![alt text](<Screenshot (97).png>)
#
- **Truth table :**
#

|A|B|Q|
|--|--|--|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|0|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "q", "wave": "1000", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

The output will be HIGH if and only if all the inputs are LOW.

#
 
[Go Up](#kc)


#
>####  Exclusive  gates :
#

<a id="xor"></a>

> ######  EX-OR GATE :
#
- **Logic symbol :**
#
![alt text](<Screenshot (98).png>)
#
- **Truth table :**
#

|A|B|Y|
|--|--|--|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "q", "wave": "0110", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

The output will be LOW if EVEN number of HIGH inputs are given.
#


 
[Go Up](#kc)

#

<a id="xnor"></a>

> ######  EX-NOR GATE :
#
- **Logic symbol :**
#
![alt text](<Screenshot (99).png>)
#
- **Truth table :**
#

|A|B|Y|
|--|--|--|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|1|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "q", "wave": "1001", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

The output will be HIGH if EVEN number of HIGH inputs are given.

#
 
[Go Up](#kc)


#
> ####  Realization of Basic Gates with Universal Gates :
#

*All the Logic Gates can be realized using Universal gates.
i.e., by NAND and NOR gates.*
#

<a id="and1"></a>

> ###### AND by NAND :

#
- **Logic symbol :**
#
![alt text](<Screenshot (101).png>)
#
- **Truth table :**


|A|B|A.B|
|--|--|:--:|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|1|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "A·B", "wave": "0001", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#

#
 
[Go Up](#kc)

#

<a id="or1"></a>

> ###### OR by NAND :

#
- **Logic symbol :**
#
![alt text](<Screenshot (102).png>)
#

- **Truth table :**

#
|A|B|A+B|
|--|--|:--:|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "A+B", "wave": "0111", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#
 
[Go Up](#kc)

#

<a id="not1"></a>

> ###### NOT by NAND :

 #
- **Logic symbol :**
#
![alt text](<Screenshot (106).png>)
#

- **Truth table :**

#

|A|X|
|--|--|
|0|1|
|1|0|
|0|1|
|1|0|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "X", "wave": "1010", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#
 
[Go Up](#kc)

#

<a id="and2"></a>

> ###### AND by NOR :

#
- **Logic symbol :**
#
![alt text](<Screenshot (103).png>)
#
- **Truth table :**
#

|A|B|A.B|
|--|--|--|
|0|0|1|
|0|1|0|
|1|0|0|
|1|1|1|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "A·B", "wave": "0001", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#
 
[Go Up](#kc)

#

<a id="or2"></a>

> ###### OR by NOR :

#
- **Logic symbol :**
#
![alt text](<Screenshot (104).png>)
#

- **Truth table :**

#
|A|B|X|
|--|--|--|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|1|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "B", "wave": "0011", "phase": 0 },
    { "name": "X", "wave": "0111", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```
#
 
[Go Up](#kc)

#

<a id="not2"></a>

> ###### NOT by NOR :

 #
- **Logic symbol :**
#
![alt text](<Screenshot (105).png>)
#

- **Truth table :**

#

|A|X|
|--|--|
|0|1|
|1|0|
|0|1|
|1|0|

# 
- **Timing diagram :**
# 
```wavedrom
{
  "signal": [
    { "name": "A", "wave": "0101", "phase": 0 },
    { "name": "X", "wave": "1010", "phase": 0 }
  ],
  "config": { 
    "hscale": 2
  }
}
```

#
 
[Go Up](#kc)


#
> ####  Realization of Basic Gates with CMOS :
#

<a id="and3"></a>

> ###### AND Gate :
#

![alt text](<Screenshot (107).png>)

#
 
[Go Up](#kc)

#

<a id="or3"></a>

> ###### OR Gate :
#

![alt text](<Screenshot (108).png>)

#
 
[Go Up](#kc)

#

<a id="not3"></a>

> ###### NOT Gate :
#

![alt text](<Screenshot (109).png>)

#
 
[Go Up](#kc)

#
> ####  Realization of Universal Gates with CMOS :
#

<a id="nand1"></a>

> ###### NAND Gate :
#

![alt text](<Screenshot (110).png>)

#
 
[Go Up](#kc)

#

<a id="nor1"></a>

> ###### NOR Gate :
#

![alt text](<Screenshot (111).png>)

#
 
[Go Up](#kc)

#
> #####  Realization of Exclusive Gates with CMOS :
#

<a id="xor1"></a>

> ###### EX-OR Gate :
#

![alt text](<Screenshot (112).png>)

#
 
[Go Up](#kc)

#

<a id="xnor1"></a>

> ###### EX-NOR Gate :
#

![alt text](<Screenshot (113).png>)

#
 
[Go Up](#kc)

#

<a id="ffs"></a>

-----

*<h1 align="center">Flip Flops</h1>*

----

<a id="up"></a>

>####  Key Contents :
#

<details>
<summary>Flip Flops</summary>

- [SR Flip Flop](#srff)
- [JK Flip FLop](#jkff)
- [D Flip FLop](#dff)
- [T Flip FLop](#tff)
  
</details>

<details>
<summary>Realization with CMOS </summary>

- [SR Flip Flop](#srff1)
- [JK Flip FLop](#jkff1)
- [T Flip FLop](#tff1)
  
</details>

<details>
<summary>Go To</summary>

- [Logic Gates](#lgs)
- [Combinational Circuits](#clc)

</details>

#

>#####  Classifications of Flip Flops :
```mermaid
graph TD
A[***Flip Flops***]--->B[SR Flip Flop]
A[***Flip Flops***]--->C[JK Flip Flop]
A[***Flip Flops***]--->C1[D Flip Flop]
A[***Flip Flops***]--->C2[T Flip Flop]

```
#



*Flip Flops are classified into four types:* 
- SR Flip Flop 
- JK Flip Flop
- D Flip Flop
- T Flip Flop

#

<a id="srff"></a>

> #####  SR FLIP FLOP :
#
- **Logic symbol :**
#
![alt text](<Screenshot (114).png>)
#
- **Truth table :**
#

|S|R|Q|Q+1|
|--|--|--|:--:|
|0|0|0|0|
|0|0|1|1|
|0|1|0|0|
|0|1|1|0|
|1|0|0|1|
|1|0|1|1|
|1|1|0|X|
|1|1|1|X|

# 

S stands for set and R for Reset.
Q is present output state, and Q+1 is next state.

#
[Go Up](#up)
#

<a id="jkff"></a>


> #####  JK FLIP FLOP :
#
- **Logic symbol :**
#
![alt text](<Screenshot (115).png>)
#
- **Truth table :**
#

|J|K|Q|Q+1|
|--|--|--|:--:|
|0|0|0|0|
|0|0|1|1|
|0|1|0|0|
|0|1|1|0|
|1|0|0|1|
|1|0|1|1|
|1|1|0|1|
|1|1|1|0|

#
[Go Up](#up)
#

J acts like set, and R like Reset.
Q is present output state, and Q+1 is next state.

#

<a id="dff"></a>


> #####  D FLIP FLOP :
#
- **Logic symbol :**
#
![alt text](<Screenshot (117).png>)
#
- **Truth table :**
#

|D|Q|Q+1|
|--|--|:--:|
|0|0|0|
|0|1|0|
|1|0|1|
|1|1|1|


# 

D is the input, and the letter D in D Flip Flop means "Delay".
Q is present output state, and Q+1 is next state.


#
[Go Up](#up)
#

<a id="tff"></a>


> #####  T FLIP FLOP :
#
- **Logic symbol :**
#
![alt text](<Screenshot (121).png>)
#
- **Truth table :**
#

|T|Q|Q+1|
|--|--|:--:|
|0|0|0|
|0|1|0|
|1|0|1|
|1|1|0|


# 

T is the input, and the letter T in T Flip Flop means "Toggle".
Q is present output state, and Q+1 is next state.

#
[Go Up](#up)
#



> ####  Realization with CMOS :
#


<a id="srff1"></a>

> ###### SR Flip Flop :
#

![alt text](<Screenshot (119).png>)

#
 
[Go Up](#up)

#



<a id="jkff1"></a>

> ###### JK Flip Flop :
#

![alt text](<Screenshot (120).png>)

#
 
[Go Up](#up)

#

<a id="tff1"></a>

> ###### T Flip Flop :
#

![alt text](<Screenshot (122).png>)

#
 
[Go Up](#up)

#


<style>
  html {
    scroll-behavior: smooth;
  }
</style>

----

<a id="clc"></a>

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

<details>
<summary>Go To</summary>

- [Logic Gates](#lgs)
- [Flip Flops](#ffs)

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

