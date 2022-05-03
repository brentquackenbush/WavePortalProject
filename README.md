## Running React on Repl.it

[React](https://reactjs.org/) is a popular JavaScript library for building user interfaces.

[Vite](https://vitejs.dev/) is a blazing fast frontend build tool that includes features like Hot Module Reloading (HMR), optimized builds, and TypeScript support out of the box.

Using the two in conjunction is one of the fastest ways to build a web app.

### Getting Started
- Hit run
- Edit [App.jsx](#src/App.jsx) and watch it live update!

By default, Replit runs the `dev` script, but you can configure it by changing the `run` field in the `.replit` file.

# WAVE PORTAL - LOVE PORTAL

The original project contemplates a simple portal where users can send waves(messages) that are stored in the blockchain.  Any user can interact with the contract and all the messages are displayed by the time the user connects with the application using MetaMask. The contract is written in solidity and the frontend developed with React.

The reinterpretation turns the portal in a Love Portal, adding a love theme, the ability to Send Love (like) to a message and maybe win a prize in eth, multiple features to avoid misuse and to clarify the new functionality.


### Original Features

#### Contract
- Code in Solidity.
- Function to send message (Wave).
- Function to get all waves.
- Function to get total amount of waves.
- Time wait period to avoid a same address to spam messages.
- Interaction to randomly draw a prize every time someone sends a wave.
- Event emmition for every nem wave.

#### Application
- Built with React.
- MetaMask communication to retrieve address and interact with the contract.
- Message list display with address and timestamp sorted by most recent wave.

### New Features
#### Contract
- Function to check if the address can wave again (30 second wait period).
- Function to Send heartfelt message that ensures the right amount of ether is being charged (0.0001 ether) from the user to avoid a malicious applictaion wrongfully interacting with the contract. Other than that, verifies that the user is not trying to like it's own waves and then decide randomly if the user, and the message creator, won the prize.

#### Application
- Checking current account everytime it needs to interact with the contract to make sure it's using the users current account, even if it was only changed in Metamask.
- Alerts for when there's any error and for when the user wins eth
