# Smart contract collection for DeFi Lending

## Block Borrower Smart contract

### Introduction
The `BlockBorrower` smart contract, implemented in Solidity, facilitates a range of decentralized finance (DeFi) activities. It enables the creation and management of banks, handling of loans with NFTs as collateral, and the execution of auctions in the event of loan defaults.

### Key Features

#### Bank Management
- **createBank**: Allows for the creation of a new bank with specified parameters such as interest rate, tenure, and loan percentage.
- **joinBank**: Enables users to join a bank as lenders by depositing a certain amount.
- **depositToBank**: Facilitates additional fund deposits by lenders into the bank.
- **withdrawBalance**: Permits lenders to withdraw their funds from the bank.
- **setInterestRate**: Bank admins can adjust the bank's interest rate.
- **setTenure**: Bank admins are enabled to modify the loan tenure.
- **LeaveBank**: Allows lenders to exit a bank under specific conditions.
- **closeBank**: Bank admins can shut down a bank, contingent on certain criteria.

#### Loan and NFT Management
- **depositNFT**: Users can deposit NFTs as collateral to secure loans.
- **withdrawNFT**: Users can retrieve their NFTs post loan repayment or closure.
- **repayEmi**: Facilitates loan EMI repayments by users.
- **claimBalanceFromLoan**: Users can claim any remaining balance post-loan repayment.

#### Auction Management
- **startAuction**: Enables lenders to initiate an auction for a defaulted loan.
- **finalizeAuctionBeforeTime**: Lenders can conclude an auction ahead of schedule.
- **checkIfAuctionHasExpired**: Checks if an auction has expired and takes necessary action.
- **cancelAuctionBeforeTime**: Permits lenders to cancel an auction before its due time.

#### Utility Functions
- **checkIfAuctionable**: Verifies the eligibility of a loan for auction.
- **isLoanClosed**: Checks the closure status of a loan.
- **apportionProfitOrLoss**: Distributes profit or loss among lenders.

#### View Functions
- **getAllCustomersOfBank**: Retrieves all customers of a particular bank.
- **getAllLendersOfBank**: Acquires a list of all lenders in a bank.
- **getAllNftDepositsOfBank**: Lists all NFT deposits of a user in a bank.
- **getMyBankBalance**: Provides a user's balance in a bank.
- **getStatusOfLender**: Displays a lender's status in a bank.
- **getTotalNumberOfBanks**: Counts the total number of banks.
- **getRepaymentSchedules**: Fetches a loan's repayment schedule.
- **calculateDues**: Calculates the dues owed for a loan.

### Technology Stack
- Solidity for smart contract development.
- OpenZeppelin contracts for ERC721 (NFT) implementations.
