<hr/>
<hr/>

<a name="readme-top"></a>

# INPUT CONTROL CONTRACT

<hr/>

# ENSURES YOUR FUNCTIONS ARE ONLY CALLED WITH CERTAIN VALUES AS INPUTS DEPENDING ON THE CALLER
The code in this repo hasn't been tested or improved yet but I think it already gives good idea of what it is. If further elaboration or development please mention me in your work.
😉 https://github.com/CarlosAlegreUr 😉

<br/>
<hr/>
<br/>

## 🙀 A PROBLEM THAT SOLVES 🙀

Imagine you have an NFT collection and you have to update a token URI due to some improvement to your
client's NFT.
😉

<br/>
<hr/>
<br/>

## 🤖 General usecase explanation 🤖

InputControl can be used to control which inputs can some addresses send to your smart contracts functions.

<br/>
<hr/>
<br/>

## ✨ How to use ✨

1. To use InputControl make your contract inherit InputControl and add the isAllowedInput()
   modifier in the functions you desire to control their inputs. The '\_input' parameter of the
   modifier must be = keccak256(abi.encodePacked(inputs)).

2. Additionally you can override callAllowInputsFor() if you please mixing this functionality with,
   for example, other useful ones like Owner or AccessControl contracts from OpenZeppelin.

([back to top](#🙀-the-problem-🙀))

<br/>
<hr/>
<br/>

## 🎉 FUTURE IMPROVEMENTS 🎉

* Test the code. 
* Improve data types and structure.
* Add deployment script and example of use script.

([back to top](#🙀-the-problem-🙀))

<hr/>

<a name="realcase"></a>

## Contact

Carlos Alegre Urquizú - calegreu@gmail.com

([back to top](#🙀-the-problem-🙀))

<hr/>

## 📜 License 📜

Distributed under the MIT License. See `LICENSE.txt` for more information.

([back to top](#🙀-the-problem-🙀))
