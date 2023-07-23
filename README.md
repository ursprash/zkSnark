# circum_circuit
To implement a zkSNARK circuit that proves you know the inputs A (0) and B (1) that yield a 0 output, we'll use the circom programming language to define the circuit and then use ZoKrates to generate the proof and verification keys. Finally, we'll deploy a verifier smart contract on-chain to verify the proofs generated by the zkSNARK circuit.
![Screenshot 2023-07-23 163335](https://github.com/ursprash/zkSnark/assets/111697531/bba84173-4412-47b9-ab12-a5f9da841bd8)

## Description
This project implements a logical gate circuit using the circom programming language. The circuit implements the following truth table:

A B X Y Q

0 0 0 1 1

0 1 0 0 0

1 0 0 1 1

1 1 1 0 1

## Project Implementation
1. Write a correct circuit.circom implementation.
2. Compile the circuit to generate circuit intermediaries.
3. Generate a proof using inputs A=0 B=1.
4. Deploy a solidity verifier to Goerli/Mumbai Testnet.
5. Call the verifyProof() method on the verifier contract and assert output is true.

## Circuit Code 
![1111](https://github.com/ursprash/zkSnark/assets/111697531/309f0a52-15eb-4f51-bb6c-df4ae0fced87)

## Step 
1. Step 1: Install the required dependencies: npm install
2. Step 2: Update Hardhat Configuration File
3. Step 3: Compile the Contract: npx hardhat compile
4. Step 4: Deploy the Contract: npx hardhat run scripts/deploy.ts --network mumbai
5. Step 5: Verify the Deployment:

After successfully deploying the contract, the script deploy.ts should print "true" in the terminal if the deployment is successful. If you encounter any issues, make sure to review your contract code and the Hardhat configuration.

Remember that using a .env file to store private keys is a common practice to keep them secure. However, always ensure that you do not commit your .env file to version control systems to avoid leaking sensitive information. Additionally, be cautious when deploying contracts and make sure to test your code thoroughly before deploying it to the mainnet or any production environment.

## Author
urspras





