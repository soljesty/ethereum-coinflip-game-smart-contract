# Coinflip Game for Ethereum

This is a `Solidity` contract for a coin flip game on the `Ethereum` blockchain. The contract allows a player to place a bet on the outcome of a coin flip, and then to flip the coin and determine the result. If the player wins the coin flip, they can withdraw double the bet amount, if they lose the coin flip, the bet amount gets sent to contract owner.

The contract includes several methods to implement the different steps of the coin flip game. The `placeBet` method allows the player to place a bet by sending a specified amount of ether to the contract. The `flip` method flips the coin and emits a `CoinFlipResult` event with the result of the coin flip. The `withdraw` method allows the player to withdraw the bet amount if they win the coin flip.

The contract also includes several checks to ensure that only the player can perform certain actions, and that the actions are performed correctly. For example, the `placeBet` method checks that the player is sending the correct amount of ether, and the flip method checks that only the player can flip the coin.

Overall, this contract provides a basic implementation of a coin flip game on the Ethereum blockchain.

# Order of Execution

In this contract, the order of execution is enforced by using the `require` statement in the different methods. For example, the `flip` method includes a `require` statement that checks that the player has placed a bet before flipping the coin, and the `withdraw` method includes a `require` statement that checks that the player has won the coin flip before withdrawing the bet amount. Additionally, the fallback function includes a `require` statement that checks that the player has lost the coin flip before transferring the bet amount to the contract owner.

These checks ensure that the contract is executed in the correct order, and that the player can only perform actions that are valid in the current state of the contract. For example, the `flip` method cannot be called before the `placeBet` method, and the `withdraw` method cannot be called before the `flip` method.
