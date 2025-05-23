
### REMIX ID USED : 0x5B38Da6a701c568545dCfcB03FcB875f56beddC4

### Table of Contents:
- `Voting System`
- `Student Record Management`
- `Access Control Using Modifiers`
- `Ether Value System (EVS)`
- `Simple Auction`

##  1. `votingSystem.sol` – **Simple Voting System**

### Description:
This contract implements a basic decentralized voting system where users can vote for predefined nominees. It ensures one person can only vote once.

### Key Functions:
- `constructor(string[] memory names)` – Initializes the list of nominees.
- `castVote(uint nomineeIndex)` – Allows users to vote by specifying nominee index.
- `viewNominee(uint index)` – Returns nominee's name and vote count.
- `numberOfNominees()` – Returns the total number of nominees.

![BCP_1](https://github.com/user-attachments/assets/d84b8fb8-f1c9-4b23-bae7-685a264a5609)

![BCP_1_2](https://github.com/user-attachments/assets/8589340c-31d1-44b9-aeda-b51e6baa0e11)

![BCP_1_3](https://github.com/user-attachments/assets/5355292e-3374-470e-b84e-0338175b965b)

---

##  2. `AcademicDirectory.sol` – **Student Profile Registry**

### Description:
A simple academic directory where profiles of students are stored with their name and unique ID. Anyone can register or fetch student records.

### Key Functions:
- `registerProfile(string memory _fullName, uint _id)` – Registers a new student profile.
- `fetchProfile(uint _id)` – Fetches a student's profile by ID.

![BCP_2_1](https://github.com/user-attachments/assets/9a69b0be-7328-4325-b929-b9a923446adb)

![BCP_2_2](https://github.com/user-attachments/assets/7a4db160-eb68-4e44-b1a1-9da336306367)

![BCP_2_3](https://github.com/user-attachments/assets/211461fa-7c4d-40a0-b4ec-2fcfb66b48ec)

---

##  3. `ACD.sol` – **Role-Based Academic Data Access**

### Description:
This contract enforces access control where only registrars can assign faculty roles, and only faculty members can register learners. The registrar can also remove learner records.

### Key Functions:
- `authorizeFaculty(address _faculty)` – Registrar assigns faculty roles.
- `registerLearner(string memory _fullName, uint _idNumber)` – Faculty registers a learner.
- `viewLearner(uint _idNumber)` – View learner profile.
- `removeLearner(uint _idNumber)` – Registrar removes a learner.

![BCP_3_1](https://github.com/user-attachments/assets/e1cd5264-bbc9-4a36-9445-6018b38a615e)

![BCP_3_2](https://github.com/user-attachments/assets/130b372a-3a99-41ca-ab17-c74c3a8c8241)

![BCP_3_3](https://github.com/user-attachments/assets/cdde66b3-4128-4669-8a03-388edd6c824c)

![BCP_3_4](https://github.com/user-attachments/assets/82d7a630-fb4a-4eca-ad9e-c9f400583014)

![BCP_3_5](https://github.com/user-attachments/assets/58083f2d-2d53-4927-893d-1a8899f5fbe0)

---

##  4. `EVS.sol` – **Ether Value System (FundDropBox)**

### Description:
A secure donation box system where users can send Ether to the contract. The contract keeps track of each donor’s contributions and allows the founder to release funds to recipients.

### Key Functions:
- `dropFund()` – Accepts ETH from donors.
- `donorHistory(address supporter)` – Shows how much ETH a donor has contributed.
- `getPotStatus()` – Shows current balance of the fund.
- `unlockFund(address payable receiver, uint256 payout)` – Founder can release funds to any recipient.

![BCP_4_1](https://github.com/user-attachments/assets/96b1edca-239b-46c6-9ac4-affe4d4822dc)

![BCP_4_2](https://github.com/user-attachments/assets/6a01d371-d92d-4ab7-ac11-6ce6ea3a93c3)

![BCP_4_3](https://github.com/user-attachments/assets/55562079-cc5b-4097-87b3-59b0b09fe054)

---

##  5. `BiddingHub.sol` – **Simple Auction System**

### Description:
An auction system where users can place bids. The highest bidder wins, and non-winning participants can withdraw their bid amounts. Only the auction master can close the auction.

### Key Functions:
- `placeBid()` – Accepts bids, must be higher than current highest.
- `withdrawRefund()` – Allows users to withdraw their previous bids.
- `endAuction()` – Ends the auction and transfers ETH to auction master.

![BCP_5_1](https://github.com/user-attachments/assets/6ee96eb4-2e71-4d62-9f2d-976d81a0501b)

![BCP_5_2](https://github.com/user-attachments/assets/993df7e4-16ff-453b-8816-d9a0af003964)

![BCP_5_3](https://github.com/user-attachments/assets/2951c456-900a-4709-a1b3-2701f49ccabb)

![BCP_5_4](https://github.com/user-attachments/assets/0c242acd-74ff-4a78-88ce-888e954b6902)

---

##  6. `EHS.sol` – **Ether Splitter (ValueDivider)**

### Description:
A smart contract that accepts Ether and splits the total amount equally between three fixed beneficiaries. Each can later withdraw their accumulated share.

### ID:
Registrer ID: 0x5B38Da6a701c568545dCfcB03FcB875f56beddC4

Beneficiary Account A: 0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2

Beneficiary Account B: 0x4B20993Bc481177ec7E8f571ceCaE8A9e22C02db

### Key Functions:
- `deposit()` – Accepts Ether and distributes it equally.
- `receive()` – Fallback function, also deposits.
- `withdrawPortion()` – Allows a beneficiary to withdraw their credited share.
- `checkBalance(address account)` – View how much Ether a beneficiary can withdraw.

![BCP_6_1](https://github.com/user-attachments/assets/e31b25d6-b29f-4dd8-a71f-688886b6e278)

![BCP_6_2](https://github.com/user-attachments/assets/1a74b7dc-6a64-49cb-9dc9-dc0351f43a72)

![BCP_6_3](https://github.com/user-attachments/assets/d87c551b-4e23-4928-ab82-6da757daa1e0)

![BCP_6_4](https://github.com/user-attachments/assets/ba4c5ebf-b6e0-4512-8d98-0763aa0d6901)

![BCP_6_5](https://github.com/user-attachments/assets/2a38323d-2dc9-4578-9d2c-65998fb2d9e7)

---







