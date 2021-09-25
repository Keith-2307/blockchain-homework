# blockchain-homework

## Proof of Authority Development Chain

---

Four deliverables:
-	Set up your custom testnet blockchain.
-	Send a test transaction.
-	Create a repository.
-	Write instructions on how to use the chain for the rest of your team.

### Backgroud:

As a new hire of ZBank, I was tasked with creating a private testnet that I and my team of developers can use to explore potential for blockchain at the bank. Zbank is a small innovative bank that is interested in exploring what blockchain technology can do for them and their customers. Setting up a testnet was decided upon because there is no real money involved, which will give my team of developers the freedom to experiment since testnets allow for offline development.  

Before we begin with the development of the Testnet Proof of Authority Development Chain, we will have to setup and install a Crypto Wallet.  

Points to note: It is generally recommended that one gets a hardware wallet or using MetaMask as a method to access their wallet and store your funds.  

The following assumes you are not using a hardware wallet or MetaMask. Due to their ease of use and security, **we recommend a hardware wallet for cold storage.**  

Remember to back up any wallets you create! Including the 12-word or 24-word Secret Recovery Phrase for your hardware wallets! MyCrypto CANNOT recover any lost passwords or access accounts. MyCrypto only has access to information that is publicly available on the blockchain. The security and responsibility of your funds rests on your own shoulders! But MyCrypto will always be here for guidance and to answer any questions that you may have regarding how to be safe with your funds.  

As mentioned above, this exercise is a trial by ZBank in exploring the potential for blockchain at the bank and therefore we will recommend using the MyCrypto desktop app, which is all that’s required at this time. Should this test run be successful, we will be providing the appropriate install guidelines for a hardware wallet or MetaMask mentioned above.  

### Downloading and Installing MyCrypto desktop app:  

To set up your local MyCrypto, start off by downloading the latest release of the desktop application from [download.mycrypto.com](https://download.mycrypto.com). Click on the “Download Now” for Windows tab on the left of your screen.  
![Picture1](https://user-images.githubusercontent.com/83662813/134529926-16a2a6f2-710f-44e2-90c4-e15b63cb9448.png)  

To open the MyCrypto application, double-click the executable. This should open a new window on your computer with the local version of MyCrypto running. You will get a warning that says it is unable to connect to the network, but this is completely normal.  

### How to Create a Wallet:  

Once you have downloaded and successfully installed the app, open the app from your applications folder. This should open the MyCrypto Desktop interface. Please navigate the initial setup screens as shown below:
![Picture2](https://user-images.githubusercontent.com/83662813/134531321-72a48f48-b40c-4707-abda-2f05533a6e75.gif)  

Click select “Create New Wallet” from the page below:   
![Picture3](https://user-images.githubusercontent.com/83662813/134531680-048960cd-2cd5-41db-88cb-2ccf0a1f6942.png)  

After Clicking on the "Create New Wallet" in the left side navigation bar. The following page appears with three options:  
![Picture4](https://user-images.githubusercontent.com/83662813/134532571-47d9de83-1e82-49c3-a329-ebd10418b052.png)  

Select an option for a type of wallet to create. In this case, click "Generate a Wallet" in the "Create New Wallet" box.  
![Picture5](https://user-images.githubusercontent.com/83662813/134532859-b7c495fb-14ee-4c1e-bc85-1347cfa54865.png)  

### Generate a Mnemonic Phrase:  

Record the list of words on a Notepad in the exact order as has been generated.  
![Picture6](https://user-images.githubusercontent.com/83662813/134533226-2fcf2d8e-28db-4a4a-bd8d-a6da3aaadca3.png)  

Click on the ‘Confirm Phrase’ button to Create your wallet by selecting the words in the order that they appeared.  
![Picture7](https://user-images.githubusercontent.com/83662813/134533657-a641125e-02c3-4e2c-9075-da8eb1a53e5e.gif)  

To confirm your wallet has been created please click on "Go to Account"  
![Picture8](https://user-images.githubusercontent.com/83662813/134534052-6c944524-2263-45a3-a8ad-01dcac8ee988.jpg)  

On the next page, click on the bottom left on “Change Network” and navigate to the top of the left side to switch the Crypto Wallet to the Ropsten Network. The bottom left should now say: “Connected to Ropsten Network”. As shown below.  
![Picture9](https://user-images.githubusercontent.com/83662813/134534754-950b32d4-3722-4d43-8506-aa092faf662c.png)  

Navigate to the “Mnemonic Phrase” and select it. The next screen will require you to copy and paste the list of words (Mnemonic Phrase) into the password section and select unlock.  
![Picture10](https://user-images.githubusercontent.com/83662813/134535304-a082eb37-27c4-4eeb-b5b5-290ce93103a8.png)  

At the following screen, after opening the wallet, you will be asked to select an address. It is recommended that you select the first address from the list as shown below and click on “Unlock”.  
![Picture11](https://user-images.githubusercontent.com/83662813/134535506-3de58b85-0538-44a6-9c2e-2ca86747f874.png)  

The next page shows the MyCrypto Wallet That you have now created. Please copy the address on the top right of your wallet and save it on your “NotePad”.  
![Picture12](https://user-images.githubusercontent.com/83662813/134535812-0d47895f-ef39-412e-b7e5-fb9f5fbda834.png)  

Navigate to the ‘Wallet Info” chevron on the top of your wallet to obtain the “Private key”, which should be copied and pasted to the NotePad txt file.  
![Picture13](https://user-images.githubusercontent.com/83662813/134536071-691b60a4-c76b-4849-94c8-80232461fe64.png)  

The NotePad .txt file should now contain the “Mnemonic Phrase”, the “Public Address Key” for your wallet and the “Private Key”. It is recommended that you save this txt file both on your computer and off the computer for safe keeping.  
![Picture14](https://user-images.githubusercontent.com/83662813/134536472-30250f8f-f9bd-428d-8df1-7129a67eb50f.png)  

The MyCrypto Wallet is now created and setup. Click on the “Send Ether and Tokens” chevron on the top to return to the wallet’s main page.  
![Picture15](https://user-images.githubusercontent.com/83662813/134536693-e763b09c-a2e4-4c03-af85-4cee9a92dbfa.png)  

## Now on to the second part of setting up this Network:  
**Installing Go Ethereum Tools:**  

Go Ethereum is one of the three original implementations of the Ethereum protocol. It is written in Go, fully open-source and licensed under the GNU LGPL v3. We will be using “Go Ethereum Tools” to create the blockchain for this Testnet project. To provide some insight on the processes to be carried out, we will be creating the blockchain from the “Genesis block” to mine tokens and eventual send a test transaction to a MyCrypto Wallet.  

We will be installing the necessary tools on the ZBank’s windows 10 computers and the following steps are required.  

Open your browser and navigate to the Go Ethereum Tools download page at [geth.ethereum.org/downloads](https://geth.ethereum.org/downloads/)  

Click on the "Geth & Tools 1.9.7 Archive Application" to download the bundle of tools. Please see the steps below to install the Go Ethereum Tools: Scroll down to the "Stable Releases" section and proceed with the download.  
![Picture16](https://user-images.githubusercontent.com/83662813/134537905-c8b1d0ba-a944-43cd-8180-4f373608edc9.gif)  

Please ensure you are running a 64bit computer to download and install the 64-bit version of the executable file. If not please download the 32-bit version for Microsoft Windows. For assistance in determining whether your computer is 64 or 32-bit please email the I.T. department and we will be happy to help.  

After downloading the tools archive, open your "Downloads" folder, and you will find a file called geth-alltools-windows-amd64-1.9.7-a718daa6.zip. Please note that the last numbers in the filename could vary depending on the last update by the site.  

Decompress the archive in the location of your preference in your computer's hard drive and rename the containing folder as Blockchain-Tools. I recommend using a location that can be easily accessed from the terminal window like the user's home directory.  

## With the Go Ethereum Tools downloaded and Saved to your renamed folder: Blockchain-Tools 

We can move to the third step: Setting up your Ethereum Environment in Gitbash. This can be done by following the steps below:  

1.	Open your GitBash Terminal and execute the following commands to install **web3.py** and **bit**, respectively. However, we need to create an environment to run the Ethereum testnet transaction. The Ethereum Environment is created as follows:  

     **conda create -n ethereum** python=3.7 **anaconda**  

2.	Activate the Ethereum environment that you created by executing the following:  

    **conda activate Ethereum**  

3.	Install **web3.py** and **bit**, respectively, by running the following commands: 

    **pip install web3**  

    **pip install bit**  

#### It is recommended that you verify the installs have been successful before proceeding, 

Use the **pip list** function with a **grep** argument to identify if the **web3** library installed successfully.  

   **pip list | grep web3**  
    
Use the **conda list** function with a **grep** argument to identify if the **bit** library installed successfully  

   **pip list | grep bit**  
    
![Picture17](https://user-images.githubusercontent.com/83662813/134540500-4fc9ef1b-8894-402a-8852-891e7cc45b4e.png)  

## Create Node accounts in the Ethereum Environment

1. With your Terminal in the Ethereum Environment, navidate to a folder **Blockchain-Tools** and create the node accounts “Node1” and “Node2”. Your block chain folder can be opened by the command:  

   **$cd Blockchain-Tools**  
            
 **Please see the steps below to create the accounts:**   
 
 o	From your gitbash Terminal, in the Ethereum environment, run the command:  
 
   **./geth --datadir node1 account new** 
             
You will be prompted to enter a password: For simplicity and convenience, we recommend using the following password: **2468**, confirm password when prompted before moving forward.  

The resulting public address key, which will be required later, should be copied, and saved to your notepad txt file.  

example of a 'Public address key’:  
**0x623027E7C5FFD773c7078FCED62f8FE9c874542d**

You will also be given a secret Key which has to be saved to your notepad txt file as well.  

Example of a path to the 'Secret key': 
**UTC--2021-09-20T14-36-45.255541500Z--623027e7c5ffd773c7078fced62f8fe9c874542d**  

o	From your gitbash Terminal, in the Ethereum environment, run the command:
**./geth --datadir node2 account new**  

The resulting public address key, which will be required later, should be copied, and saved to your notepad txt file.  

example of a 'Public address key’: 
**0x442740Cc829F0c88695471c5272BeC6B602C207F**  

You will also be given a secret Key which has to be saved to your notepad txt file as well.  

Example of a path to the 'Secret key':
**UTC--2021-09-20T14-39-30.591617600Z--442740cc829f0c88695471c5272bec6b602c207f**

![Picture18](https://user-images.githubusercontent.com/83662813/134544663-15a2e9ce-6598-4cf1-9c52-660673e0a324.png)  

2.	The next step is to use node1 and node2 to generate the “Genesis block”. This is done by running the following command in the Ethereum Environment from your terminal in your **Blockchain-Tools** folder:  

  **./puppeth**  
  
  ![Picture19](https://user-images.githubusercontent.com/83662813/134545051-4b8eff14-c80a-40c3-9f4e-a78a7950aa2f.png)  
  
It is now recommended that you name your network to ‘zbanknet’. It is recommended that you type this network name in your terminal as shown and expect the following response.  
![Picture20](https://user-images.githubusercontent.com/83662813/134545331-902f76ea-7d9a-4701-ae06-091aa30b7f34.png)   

Type 2, and enter to select: Configure new genesis  
![Picture21](https://user-images.githubusercontent.com/83662813/134545631-4865f9b3-a7d6-4926-8278-2b9bdd1f09bb.png)  

Type 1, and enter to select: Create new genesis from scratch  
![Picture22](https://user-images.githubusercontent.com/83662813/134545826-3b1985c4-5d12-40e5-999f-e33e11436995.png)  

Type 2, and enter to select: Clique – proof-of-authority  
![Picture23](https://user-images.githubusercontent.com/83662813/134546025-7110acd1-7531-41f6-bb6d-ffb5ec0bf9ca.png)  

Type 15 and enter for the seconds each block should take.  
![Picture24](https://user-images.githubusercontent.com/83662813/134546245-12153425-682d-4c4e-9f5e-973b7a4fef92.png)  

Paste both account addresses from the first step one at a time into the list of accounts to seal. Copy and paste the public address for node one here, when answering the following “Which accounts are allowed to seal?” (Mandatory at least one) Please omit the “0x” from the copied address.  
![Picture25](https://user-images.githubusercontent.com/83662813/134546560-e272c378-f705-4493-9cf7-1e018b136ceb.png)  

Paste both account addresses from the first step again in the list of accounts to pre-funded. There are no block rewards in Proof of Authority (POA), so you'll need to pre-fund.  
![Picture26](https://user-images.githubusercontent.com/83662813/134546797-6fe09ae0-1ec5-462f-a22b-2d9c0b6f7302.png)  

You are requested to press **enter** to move on from the screen below: for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei. This keeps the genesis cleaner.  
![Picture27](https://user-images.githubusercontent.com/83662813/134547043-10d91990-474d-4b98-a5dc-8e6e035a6e76.png)  

At the next prompt: Specify your chain/network ID if you want an explicit one (default = random) Please enter:		**777**
![Picture28](https://user-images.githubusercontent.com/83662813/134547258-3d5a585a-2f8f-43a7-bdd3-c24936ee6d31.png)  

Please select option 2, for Manage existing genesis.  
![Picture29](https://user-images.githubusercontent.com/83662813/134547603-1ace3473-9e98-4e67-bc98-2083fb112fcf.png)  

Please select option 2, for Export genesis configurations.  
![Picture30](https://user-images.githubusercontent.com/83662813/134547775-380f9c9f-099f-42bf-99c7-a6a006cec22f.png)  

Please type the zbanknet to save to the desired folder, when answering the question: Which folder to save the genesis specs into? Then exit the running terminal.  
![Picture31](https://user-images.githubusercontent.com/83662813/134547975-c945103a-26d9-4e6c-88e6-5e04e291d0e1.png)  

With the genesis block creation completed, we will now initialize the nodes with the genesis' json file.  

Using **geth**, initialize each node with the new **zbanknet.json**.  

**./geth --datadir node1 init zbanknet/zbanknet.json**  

**./geth --datadir node2 init zbanknet/zbanknet.json**  
![Picture32](https://user-images.githubusercontent.com/83662813/134548410-196859d2-e63c-475b-99a3-6927e62e1c39.png)  

## Activate your local blockchain  

With your MyCrypto Wallet installed and the Ethereum Environment in place, we can now proceed to activate our Blockchain. Follow these instructions to get your local Ethereum-based blockchain mining. Using this, you can build a cheat sheet to get your geth nodes up and running anytime.  

**This is done as follows:**
**1.	Start Node1**
Start the first node by opening a new terminal and running the following command, the "SEALER_ONE_ADDRESS" must be substituted with the public address of the first node that was created in the previous session (do **not** include the leading **0x**). Please ensure you are in the Ethereum environment and in the Blockchain-Tools folder.

o	**./geth --datadir node1 --unlock** "SEALER_ONE_ADDRESS" **--mine --minerthreads 1 --allow-insecure-unlock**

o	Terminal 1 Command: **./geth --datadir node1 --unlock "** 0x246C401561ECd83F5f5022798f7D6Fc23C447127" **--mine --minerthreads 1 --allow-insecure-unlock**
![Picture33](https://user-images.githubusercontent.com/83662813/134550147-30ea68ca-7098-4338-9a9f-837f14d7d20d.png)

o	Important: Type your password and hit enter when prompted – *Entering your password may not be visible!*   

o	Copy the resulting enode address from the terminal to your notepad.
**"enode://c68da51cda265fae6cdae610c948b117b346c4676a4bde713995af8641978329000669104e74c824f6e284f5ab18a7526682207da7ede0e812235a6c56700362@127.0.0.1:30303"** 

**2.	Start Node2**  

Please note that this installation and process is strictly to be done on a windows-based system, should anyone require these installations to be done on another system other than windows please contact the I.T. department for the system base installations instructions.

**Windows Install:**

o	Start node two by opening a second new terminal and running the following command:  

**./geth --datadir node2 --unlock** "SEALER_TWO_ADDRESS" **--port 30304 --rpc --bootnodes** "SEALER_ONE_ENODE_ADDRESS" **–ipcdisable --allow-insecure-unlock**  

o	Substitute the "SEALER_TWO_ADDRESS" with the the public address of the second node that was created in the previous session. (Do **not** include the leading 0x).  

o	Substitute the "SEALER_ONE_ENODE_ADDRESS" with the enode address of node 1 that was copied in step 1.

o	Terminal 2 Command: **./geth --datadir node2 --unlock** "0x78f8306ef80dD7c73c17a541c3C776517A6432A0" **--port 30304 --rpc --bootnodes** "enode://c68da51cda265fae6cdae610c948b117b346c4676a4bde713995af8641978329000669104e74c824f6e284f5ab18a7526682207da7ede0e812235a6c56700362@127.0.0.1:30303" **–-ipcdisable --allow-insecure-unlock**  
![Picture34](https://user-images.githubusercontent.com/83662813/134552469-ed7a0bed-aa35-44fe-8f2d-39af908a349b.png)
o	**Important:** Type your password and hit enter when prompted – *Entering your password may not be visible!* 

The display below shows your Terminal outputs.
![Picture35](https://user-images.githubusercontent.com/83662813/134553050-a0065e33-3449-479d-9a78-3d44aa056b14.png)  
o	The chain should be up and running after you start the second node.  

Once you get the chain running, copy and paste the commands you used for each node into a README.md inside your network's folder. This will allow you to get your chain started anytime.

### With both nodes up and running, the blockchain can be added to the MyCrypto APP for testing.

Open the MyCrypto app, then click Change Network at the bottom left:  
![Picture36](https://user-images.githubusercontent.com/83662813/134553779-d047de90-afb6-476d-814b-75c27cd82092.png)

Click "Add Custom Node", then add the custom network information that you set in the genesis.
![Picture37](https://user-images.githubusercontent.com/83662813/134554119-7224db42-d951-4495-9617-7c6f5a2b068d.png)  

Setup your **Custom Node** as follows:

o	Make sure that you scroll down to choose **Custom** in the "Network" column to reveal more options like **Chain ID**:  

o	Type **ETH** in the Currency box.  

o	In the Chain ID box, type the chain id you generated during genesis creation  

o	In the URL box type: **http://127.0.0.1:8545.** This points to the default RPC port on your local machine. It is recommended that you type the URL as shown above without the (s) after http. 

Finally, click **Save & Use Custom Node**
![Picture38](https://user-images.githubusercontent.com/83662813/134555261-faa45e72-624e-4f1b-b071-ec93544af976.gif)

### After connecting to the custom network in MyCrypto, it can be tested by sending money between accounts.
o	Select the View & Send option from the left menu pane, then click Keystore file.  
![Picture39](https://user-images.githubusercontent.com/83662813/134555629-dfaec184-4475-45b3-8d9e-ca2a9d74dbd4.png)  

o	On the next screen, **click Select Wallet File**, then navigate to the keystore folder inside your Node1 directory(see step2), select the file located there, provide your password (step3) when prompted and then click **Unlock**.

**Step 1.**
![Picture40](https://user-images.githubusercontent.com/83662813/134555974-b8f13007-98e9-4786-9182-0ed8b6756546.png)  

**Step 2.**
![Picture41](https://user-images.githubusercontent.com/83662813/134556133-675923ea-9f54-44f0-b380-3699602ed645.png)

**Step 3.** *Password: 2468*
![Picture42](https://user-images.githubusercontent.com/83662813/134556518-698663e0-6bd9-4629-96b8-0e0552c71dec.png)  

o	This will open your Zbanknet account wallet inside MyCrypto.

o	The balance that was pre-funded for this account in the genesis configuration is shown in your wallet; Please note that these millions of ETH tokens are just for testing purposes. 
![Picture43](https://user-images.githubusercontent.com/83662813/134556704-f6ba8caa-dd9c-41b8-b9b5-9a48eba473b7.png)  

o	In the To Address box, type the account address from Node2, then fill in an arbitrary amount of ETH: Recommended 10,000 ETH.

o	Confirm the transaction by clicking "Send Transaction", and the "Send" button in the pop-up window.
![Picture44](https://user-images.githubusercontent.com/83662813/134556901-a2b33702-1a11-487b-a347-b3f4382b6b9e.gif)

Click the Check TX Status when the message pops up, confirm the logout:
![Picture45](https://user-images.githubusercontent.com/83662813/134557046-fb8b81c7-bb0c-42f2-8fd1-53ebd8e5133a.gif)

The transaction confirmation will change from **Pending** to **Successful** in around the same blocktime you set in the genesis.
![Picture46](https://user-images.githubusercontent.com/83662813/134557412-dfcf4503-1a16-4373-89cd-be12b8ba6456.png)  

Terminal Confirmation of transaction:  
![Picture47](https://user-images.githubusercontent.com/83662813/134557648-86e1bce9-4d5b-4019-8a91-a461dcc3eac4.png)

The following screen will show the transaction of the recommended 10,000 ETH is pending to transfer to your Node 2 address:
![Picture48](https://user-images.githubusercontent.com/83662813/134557873-e57d2de1-db2d-48f3-9765-e8af15987eea.png)

You can click the Check TX Status button to update the status.
![Picture49](https://user-images.githubusercontent.com/83662813/134558302-2a6cffa9-e22c-4cef-828f-a1e35511b4f3.png)

***Congratulations, you successfully created your own private blockchain network! – Zbanknet, and transferred 10000 ETH from account: Node1 to Node2.***

(Screen shot of Successful Transaction)

## As ZBank employees you may encounter the following Difficulties:

The nodes require significant RAM/memory to be executed and a 4-gigabit machine do not possess sufficient capacity to run the nodes. As a result, the terminal nodes will become stagnant and eventual give the following errors:
1.Peer Connection dropped
(screen shot)

2. Fail Connection: after sitting Idle for more than 30 minutes.
(screen shot)

3. Unsolicited response received on idle HTTP channel
![Picture51](https://user-images.githubusercontent.com/83662813/134786740-6674c08d-c0b7-4e39-99ea-395d8d042f41.png)  

**Note:**  

To ensure your computer system isn’t running at max memory capacity during the mining process, please navigate your mouse to the date and time display on your bottom right in the task bar. Right click, then scroll to Task Manager on the list, click select to illustrate the processes (Display 1) currently running as well as the performance (Display 2) tab to display your memory usage during this process.

Display 1: Running Processes
![Picture52](https://user-images.githubusercontent.com/83662813/134786768-10e0d44e-4dec-41e3-9484-5a6d1ad67048.png)  

Display 2: Memory Usage on GPU
![Picture53](https://user-images.githubusercontent.com/83662813/134786784-23a1ef90-48bb-4307-ac91-9eb6e8294e81.png)  

If the values displayed are like your operating system, then you will not be able to mine the Blockchains as required. We encountered similar issues with our main operating system and had to use a different computer to test this setup. We therefore recommend a complete install of all the preliminary setups as per the information provided, such as installing dependencies and environment configuration. 

Thank you
Keith Louis **(Manager, ZBank BlockChain Solutions)** 







            







  







