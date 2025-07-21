<style>
  html {
    scroll-behavior: smooth;
  }
</style>


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

#

>#####  Classifications of logic gates :
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