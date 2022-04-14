# SmartContract_Docker
A step-by-step guide to create and deploy a smart contract(ERC20) on the Ethereum TestNetwork and the Node.js application for token distribution

# Compile and Deploy Smart Contract
Step1 : Create Metamask account
Once it is created user will be provided with public and private key
Public Address:0x08882E6D3606d188EF1Be5a95a4931480b243085
Private Key: 7828a13e4a5ac01494975cf315ee097e707386225fc010d2d276011ea3c7152c
we have selected Ropsten network to perform the transaction


Step2 : Remix IDE  for the Deploying the contract

The DeployedContract.sol will be compiled and deployed
Before Compiling the code edit 
constructor() {
        _name = "MY SPECIAL TOKEN";
        _symbol = "MST";
        
        _mint(msg.sender, 1000000000000000000000000);
    }
	
	_name= Give unique name
	_symbol= Any symbol
Choose compiler version as similar to the solidity version=0.8.0
Once it is successfully compiled then it is ready to deploy
Before deploy 
Select Environment =Injected web3
Select Account No  =Owner Account Address(0x08882E6D3606d188EF1Be5a95a4931480b243085)
Before you start deploying, make sure you have the right contract name.

Step3 : Node.js Application for performing token distribution

Prerequsites :
1.Install latest Node version
2.Install web3 
3.Create an account in Infura to get the link of network end point
Edit .env file to provide  below details to node js application in order to connect to Ethereum network

INFURA_TOKEN=77c46502739f469ea80e5033bb0d24d1
CONTRACT_ADDRESS=0x01e41d2ea69295c6d7edb9d7ccbf9dc4b2961d87
OWNER_ADDRESS=0x08882E6D3606d188EF1Be5a95a4931480b243085
SUPER_SECRET_PRIVATE_KEY=7828a13e4a5ac01494975cf315ee097e707386225fc010d2d276011ea3c7152c

Once entered all of the information, open a command prompt and type the command.
node distribute.js
It will then display a message similar to a node application linked to the Ethereum network.
And perform the distribution of tokens to the ten different addresses

Step4 : We can acquire the token distribution details from Etherscan, and ether will be taken from the owner's account following the transaction.







 
 


