# blockchain-simple-contract

## My First blockchain contract (using Ethereum)

You need to install some tools before use this token:

### Tools

Git - https://git-scm.com/downloads

Visual Studio code - https://code.visualstudio.com/download

Solidity support for Visual Studio code - https://marketplace.visualstudio.com/items?itemName=JuanBlanco.solidity

Geth version 1.8.1-stable - https://geth.ethereum.org/downloads/

Installation guide - https://blockchain-br.slack.com/files/U3GDWNHTR/F6F6VJXTL/novo_-_ambiente_ethereum

NodeJS version  8.9.1  - https://nodejs.org/en/

Compiler Solidity (requisito NodeJS)

npm install -g solc

Framework Truffle (requires NodeJS)

npm install -g truffle

MetaMask - metamask.io/

Installing on chrome

Installing on firefox

### Creating your account

Suggestions for Windows developers

Link 1: https://docs.microsoft.com/en-us/windows/wsl/install-win10

Link 2: https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/



==========
### How to use

solcjs --abi MyToken.sol

solcjs --bin MyToken.sol

var contract = eth.contract(abi)

var myToken = contract.new(1000, {from: eth.accounts[0], data: '0x', gas: '4700000'}, function (erro, contract){ console.log('ERRO:', erro); console.log('CONTRACT:', contract); if(typeof contract.address !== 'undefined'){ console.log('Contract deployed! address: '+ contract.address + 'transactionHash: '+ contract.transactionHash); }})

## NOTE: on data:'0x' complete (append) with the token generated on the bin file, somethng like:

data: '0x6060604052341561000f57600080fd5b60405160208061031883398101604052808051906020019091905050806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020819055505061029a8061007e6000396000f30060606040526004361061004c576000357c0100000000000000000000000000000000000000000000000000000000900463ffffffff16806370a0823114610051578063a9059cbb1461009e575b600080fd5b341561005c57600080fd5b610088600480803573ffffffffffffffffffffffffffffffffffffffff169060200190919050506100e0565b6040518082815260200191505060405180910390f35b34156100a957600080fd5b6100de600480803573ffffffffffffffffffffffffffffffffffffffff169060200190919080359060200190919050506100f8565b005b60006020528060005260406000206000915090505481565b806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020541015151561014557600080fd5b6000808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002054816000808573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019081526020016000205401101515156101d257600080fd5b806000803373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060008282540392505081905550806000808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019081526020016000206000828254019250508190555050505600a165627a7a72305820e26f5c8de64579f16e4b589b64d84b9ef9f5e9f179ee2b8cdd7c0ee326771a8a0029'

