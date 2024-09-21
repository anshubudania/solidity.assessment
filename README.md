# PROJECT

## Create a token
## Description
Here the code create the token that contain the details like Token name, Token Abbrv. and Total Supply, and a mapping of address to uint name as balance, with some additional function:

* min function: takes two paramenter a address and a value and add the value to total supply and the address of the balance.

* burn function: it works opposite to the mint function and delete the value from total supply and a balance of sender. and to use solidity we have to install remix ide or we can use it online by visiting the website remix.ethereum.org it works same as VS code.

## Getting Started
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.



REQUIREMENTS
 1. Your contract will have public variables that store the details about your coin (Token Name, Token Ab., Total Supply)
2. Your contract will have a mapping of addresses to balances (address => uint)
3. You will have a mint function that takes two parameters: an address and a value. 
The function then increases the total supply by that number and increases the balance 
of the “sender” address by that amount
4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
and from the balance of the “sender”.
5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
to the amount that is supposed to be burned.

## Executing program
    pragma solidity 0.8.26;
    contract MyToken {

     string public token_name="Ajure";
    string public token_ab="Abb";
     uint public total_supply=100;


       mapping (address=>uint) public balance;

    function mint(address ad, uint value) public {
    total_supply+=value;
     balance[ad]+=value;
    }

     function burn(address ad, uint value) public {
     total_supply-=value;
      balance[ad]-=value;
    }

    }
Author

Anshu Budania

anshubudania1070@gmail.com

License

This project is licensed under the MIT License - see the LICENSE.md file for details
