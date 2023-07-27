# scaler-blockchain-challenge

Q1. You are developing a smart contract in Solidity for a decentralized application. As part of the contract, you want to implement a function that allows users to transfer tokens from one account to another.

You decide to use the following code for the transfer function:

```
function transferTokens(address _to, uint256 _amount) public {
    require(_amount > 0);
    require(balances[msg.sender] >= _amount);
    
    balances[msg.sender] -= _amount;
    balances[_to] += _amount;
}
```

Is this code implementation secure for transferring tokens? If yes, why? If no, what potential vulnerabilities or issues might arise?

Q2. You are developing a decentralized voting smart contract in Solidity for an election. Each voter is allowed to cast only one vote, and the contract should ensure that no duplicate votes are counted.

You decide to use the following code for the voting function:

```
mapping(address => bool) public hasVoted;

function vote() public {
    require(!hasVoted[msg.sender], "You have already voted.");
    
    // Code to process the vote and update the vote count
    
    hasVoted[msg.sender] = true;
}
```

Is this code implementation sufficient to prevent duplicate votes in the election? If yes, explain how. If no, identify potential issues and propose a more robust solution.


