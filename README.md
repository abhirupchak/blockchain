Screenshot 2025-04-09 214501
HYPERLEDGER FABRIC PRACTICAL
installing golang

sudo apt install golang-go

Installs Golang, which is necessary for running Hyperledger Fabric binaries. Screenshot 2025-04-16 102328

Check Docker version docker --version Verifies that Docker is installed and running correctly.

Screenshot 2025-04-16 103341

Check Docker compose version docker -compose  --version Verifies the installation of Docker Compose. Screenshot 2025-04-16 103419

List Files in current dictionary is  Shows the list of files and folders in the current directory.

Clone the Fabric Samples Repository and Move into the Cloned Folder

git clone https://github.com/Akshitakaushik123/fabric-samples.git; cd fabric-samples

Downloads the official Hyperledger Fabric sample code from GitHub. Enters the cloned folder where Fabric examples are available.

Screenshot 2025-04-16 104000

Download Fabric Binaries   curl -sSL https://bit.ly/2ysbOFE | bash -s
Downloads necessary Fabric binaries and Docker images like peer, orderer, and cryptogen.

Screenshot 2025-04-16 130952

7.Enter the Test Network Directory

cd test-network Navigates to the directory that contains scripts for running a sample Fabric network.

View the Network Script ./network.sh Shows the options available with the network.sh script.
Screenshot 2025-04-16 133627

Start the Fabric Network ./network.sh up Starts the network by launching peer, orderer, and CA containers, and generates the required cryptographic materials.
10.Create a Channel ./network.sh createChannel Creates a default channel (usually named mychannel) and joins the peers to it.

Screenshot 2025-04-16 132703

Shut Down the Network ./network.sh down Stops all containers and deletes the crypto material and artifacts created during the setup.
Screenshot 2025-04-16 132938

#solidity

#1. Use Remix (Beginner-Friendly, No Setup Needed) Go to https://remix.ethereum.org

It’s an online IDE to write, compile, deploy, and test Solidity contracts.

Example: Hello World Contract

pragma solidity ^0.8.0;

contract HelloWorld {
    string public message = "Hello, Blockchain!";

    function setMessage(string memory _message) public {
        message = _message;
    }
}
In Remix:

Click File Explorer → Create new file → name it HelloWorld.sol

Paste the code above.

Click Solidity Compiler → Compile

Go to Deploy & Run Transactions → Deploy the contract

Use the UI to call setMessage() or read message

#2. Install Hardhat (For Local Dev with Node.js) If you want to build real projects:

npx hardhat
Choose "Create a basic sample project".

Then you can:

Write your contracts in contracts/

Write tests in test/

Deploy using scripts in scripts/

✅ Hardhat also supports local Ethereum nodes (Hardhat Network) and real testnets.

#3. Use MetaMask for Deployments to Testnet Install MetaMask, create a wallet, and connect to a testnet like Goerli or Sepolia. You’ll need free test ETH from a faucet (I can help with that too). Tools & Resources Remix IDE: best for quick testing

Hardhat: advanced dev workflows
