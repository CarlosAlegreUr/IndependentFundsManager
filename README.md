<hr/>
<hr/>

<a name="readme-top"></a>

# InputControl Contract

<hr/>

# Ensures your functions are only called with certain values as inputs depending on the caller

## 💽Testing and implementation example repo => [(click)](https://github.com/CarlosAlegreUr/InputControl-SmartContract-Testing) 💽

## 💽NPM repo => [(click)](https://www.npmjs.com/package/input-control-contract) 💽

<hr/>

If further elaboration or development please mention me in your work.

😉 https://github.com/CarlosAlegreUr 😉

<hr/>

## 🙀 A PROBLEM THAT SOLVES 🙀

Imagine you have an NFT collection and you have to update a token URI due to some improvement for your
client's NFT.

Making the ""updateURI()"" function only callable by you will force your client to hope and trust that you will call it passing a correct URI.

Using InputControl now you can make that function
external and let your client call the function with a
token URI he previously knows points to the correct
data.

And the client can't cheat either. This is because InputControl
uses hash values derived from the inputs' values to check
if the input is what it was agreed to be.
😊

<hr/>

## 🤖 General usecase explanation 🤖

InputControl can be used to control which inputs can some addresses send to your smart contracts' functions.

Furthermore you can allow your user to call a function with a defined inputs sequence.

Example: You want your client only to call a function 3 times, first time with input value = 1, second value = 2 and third time value = 3. Input control can handle that the desired values are used in the desired order.

<hr/>

## ✨ How to use ✨

1. To use InputControl make your contract inherit InputControl and add the isAllowedInput()
   modifier in the functions you desire to control their inputs. The '\_input' parameter of the
   modifier must be = keccak256(abi.encode(inputs)).

2. Additionally you can override callAllowInputsFor() if you please mixing this functionality with,
   for example, other useful ones like Owner or AccessControl contracts from [OpenZeppelin](https://docs.openzeppelin.com/contracts/4.x/access-control).

Check a simple implemented example at [UseCaseContract.sol](https://github.com/CarlosAlegreUr/InputControl-SmartContract-Testing/blob/main/contracts/UseCaseContract.sol).

<hr/>

## 📰 Last Changes 📰

- abi.encodePacked() was fatal error! Same inputs might have the same encoded value. Now using abi.encode().
- Now you can decide wheter a function allows inputs in ordered or unordered manner even after deployment.
- Handle collision with 0 value not needed: now map to bool indicates if input has already been used.
- Better memory management when unordered inputs used.
- Function selectors now are bytes4 instead of strings, like actual func selectors in ETH.
- Shortened variable names in code.
- Tests improved.

## 🎉 FUTURE IMPROVEMENTS 🎉

- Improve and review (static analysis, audit...) code's tests.
- Test in testnet.
- Check gas implications of changing 4 bytes function selector to 32 bytes hashed function signatures.

<hr/>

<a name="realcase"></a>

## 📨 Contact 📨

Carlos Alegre Urquizú - calegreu@gmail.com

<hr/>

## ☕ Buy me a CryptoCoffee ☕

Buy me a crypto coffe in ETH, MATIC or BNB ☕🧐☕
(or tokens if you please :p )

0x2365bf29236757bcfD141Fdb5C9318183716d866

<hr/>

## 📜 License 📜

Distributed under the MIT License. See [LICENSE](https://github.com/CarlosAlegreUr/InputControl-SmartContract-DesignPattern/blob/main/LICENSE) in the repository for more information.
