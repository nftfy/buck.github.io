# Buckie

An ERC-20 token sample contract for testnets.

If you are looking for an ERC-721 token instead, check out [Blockies](https://blockies.tk/).

### Contracts

The ABI [JSON](Buckie.json) includes a faucet method. You can interact with the smart contract using Etherscan and a [Web3](https://web3js.readthedocs.io/) compatible wallet.

| Network | Contract Address                                                                                                              |
| ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ropsten | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://ropsten.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577) |
| rinkeby | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://rinkeby.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577) |
| kovan   | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://kovan.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577)   |
| goerli  | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://goerli.etherscan.io/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577)  |

| Network | Contract Address                                                                                                              |
| ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| bsctest | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://testnet.bscscan.com/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577)  |

| Network | Contract Address                                                                                                              |
| ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ftmtest | [0xF2dA2EBfE236e067FB97409f558c5Bef41081577](https://testnet.ftmscan.com/address/0xF2dA2EBfE236e067FB97409f558c5Bef41081577)  |

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

### Support

If you would like to support this page download [Brave Browser](https://brave.com/buc011). Your BAT contributions are welcome!
