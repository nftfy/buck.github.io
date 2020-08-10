# Buckie

An ERC-20 token sample contract for testnets.

If you are looking for an ERC-721 token instead, check out [Blockies](https://blockies.tk/).

### Contracts

The ABI [JSON](Buckie.json) includes a faucet method. You can find and interact with the smart contract using Etherscan.

| Network | Contract Address                                                                                                              |
| ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Ropsten | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://ropsten.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577) |
| Rinkeby | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://rinkeby.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577) |
| Kovan   | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://kovan.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577)   |
| Goerli  | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://goerli.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577)  |

### Source Code

Buckie was written using the [OpenZeppelin](https://openzeppelin.com/) library.

```solidity
// Buckie
// SPDX-License-Identifier: GPL-3.0-only
pragma solidity ^0.6.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract Buckie is ERC20
{
	constructor () ERC20("Buckie", "BUK") public
	{
		_setupDecimals(18);
	}

	function faucet() public
	{
		address _target = msg.sender;
		_mint(_target, 10000_000000000000000000);
	}
}
```
