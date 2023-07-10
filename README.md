## RaffleContract

This is a smart contract for a raffle. Participants can buy tickets with native token and have a chance to win a specified ERC721 (NFT) prize. The contract allows an admin to start and end the lottery, pick a winner, and manage the ticket cost and NFT prize.

## Features

- Participants can buy tickets by sending the correct amount of Ether.   
- The admin can start the lottery by setting the NFT contract address and token ID for the prize.   
- The admin can end the lottery and pick a winner randomly from the participants.   
- The ticket cost can be changed by the admin, but only when the lottery is not running.   
- The contract keeps track of the entry count for each participant.   
- The admin can withdraw the contract's balance.   
- The contract can be reset by the admin, clearing all data.   

## Contract Functions

- `startLottery`: Starts the lottery by setting the NFT contract address and token ID for the prize. The nftContract parameter represents the address of the NFT contract, and the tokenId parameter represents the token ID of the prize.   
- `endLottery`: Ends the lottery and prevents any further ticket purchases.   
- `pickWinner`: Randomly selects a winner from the participants and transfers the NFT prize to the winner.   
- `changeTicketCost`: Changes the ticket cost to the specified _newCost value. This can only be done when the lottery is not running.   
- `getPlayers`: Returns an array of addresses representing the participants who have purchased tickets.   
- `getBalance`: Returns the current balance of the contract in Ether.   
- `withdrawBalance`: Allows the admin to withdraw the balance of the contract.   

## Events

The contract emits the following events:

- `NewTicketBought`: Triggered when a new ticket is bought.   
- `LotteryStarted`: Triggered when the lottery is started.   
- `LotteryEnded`: Triggered when the lottery is ended.   
- `Winner`: Triggered when a winner is picked.   
- `TicketCostChanged`: Triggered when the ticket cost is changed.   
- `NFTPrizeSet`: Triggered when the NFT prize is set.   
- `BalanceWithdrawn`: Triggered when the contract balance is withdrawn.   
