# [](https://youtu.be/KT9anz_V9ns?t=0) Introduction to On-Chain Games on Solana

Section Overview: In this section, the speaker introduces the topic of on-chain games on Solana and outlines the agenda for the session.

## Why Build Games on Solana?

- Confirmation times of blocks are 400 to 500 milliseconds. 
- Transaction fees are extremely low (0.0005 SOL per transaction).
- Ability to reward players with tokens or NFTs.
- Composability allows for reusing components from other games.
- Decentralized nature ensures availability and eliminates server downtime.
- No need for backend infrastructure or account management; users can log in with their wallets.
- Replaces traditional payment providers, saving fees on microtransactions.
- Challenges with iOS store regulations when incorporating NFTs.

# [02:15](https://youtu.be/KT9anz_V9ns?t=135) Advantages of Building on Solana

Section Overview: The speaker discusses additional advantages of building games on Solana.

## Advantages

- Free for all, like running your own backend in the cloud.
- Decentralization ensures data security and availability.
- Users can log in with their wallets, using digital identities and showcasing their NFTs as profile pictures.
- Replaces traditional payment providers, saving fees imposed by Apple and Google (30% fee).
  
# [03:35](https://youtu.be/KT9anz_V9ns?t=215) Considerations for Building On-chain Games

Section Overview: The speaker highlights some considerations when building on-chain games.

## Considerations

- Crypto may not be suitable for every game; find a reason why it makes sense for your game before integrating blockchain technology.
- Regulations regarding tokens, gambling, money laundering, etc., vary by country and need to be taken into account.
- Real-time games may face challenges due to blocktimes (500 milliseconds); turn-based or slower-paced games are more suitable for on-chain implementation.

# [04:19](https://youtu.be/KT9anz_V9ns?t=259) Opportunities and New Developments

Section Overview: The speaker discusses current opportunities and new developments in the Solana ecosystem.

## Opportunities

- Solana Phone and Backpack wallet offer new possibilities for engagement.
- Backpack wallet allows execution of XNFTs, enabling direct gameplay within the wallet.
  
# Conclusion

The transcript provides an introduction to on-chain games on Solana, highlighting the advantages of building on Solana's blockchain infrastructure. It also covers considerations when developing on-chain games and mentions opportunities in the Solana ecosystem.
# [t=384s] Multiplayer Action Adventure Game on the Blockchain

Section Overview: The speaker introduces a multiplayer action adventure game built on the blockchain. The game consists of a grid with 4x4 tiles, each containing a player's public key and an Avatar public key (NFT). Players can spawn characters, kill other players to steal their soul, deposit and withdraw soil in the in-game wallet for fluid gameplay.

## Game Mechanics and Features

- The game is a multiplayer action adventure game built on the blockchain.
- Each player has a grid with 4x4 tiles containing their public key and an Avatar public key (NFT).
- Players can spawn characters using different wallets and minted 3D NFTs.
- Killing other players allows stealing their soul.
- Auto-approved wallet allows depositing soil in the in-game wallet for fluid gameplay.
- Chest spawns allow collecting free soul.
- The game works on mobile devices as well.

# [t=406s] Solana Plays Pokemon - A Crowd-Controlled Game

Section Overview: The speaker introduces "Solana Plays Pokemon," a crowd-controlled game where players vote for certain key presses to control the game. Similar to "Twitch Plays Pokemon," this game allows multiple players to collectively play a Game Boy Pokemon game by voting for moves on-chain.

## Solana Plays Pokemon Mechanics

- "Solana Plays Pokemon" is a crowd-controlled game where players vote for key presses.
- It is similar to "Twitch Plays Pokemon" where chat controls the game.
- Players collectively control the movements and actions of the character in real-time through voting on-chain.

# [t=536s] Examples of On-chain Games

Section Overview: The speaker showcases various examples of games built on Solana's blockchain. These examples include Lumia Online, Lettercaster, and Kyojin Clash. Each game demonstrates different features and mechanics that can be implemented on-chain.

## Examples of On-chain Games

- Lumia Online: A basic adventure game with monster killing, missions, and spawning.
- Lettercaster: An interesting game where players can walk around, collect items, and get tokens. It features a crank system where someone needs to press a button to proceed to the next round.
- Kyojin Clash: An amazing on-chain game utilizing an entity component system called Arc. Players can have entities (NFTs) with traits, fight each other, and move units on a big map.

# [t=642s] Building "Tiny Adventure" Game on Solana

Section Overview: The speaker demonstrates how to build a simple game called "Tiny Adventure" using Solara Playground. The game allows the player to move left or right and reach the end for a happy character animation.

## Building "Tiny Adventure"

- Use Solara Playground, a web UI for building and deploying Solana programs.
- Create a wallet in the playground by clicking on the bottom left corner.
- Type "build" in the playground to build the project.
- Follow step-by-step instructions provided in the tutorial for deploying the program.
- The "Tiny Adventure" game allows moving left or right and reaching the end for a happy character animation.

Note: Timestamps are approximate as they are based on seconds mentioned in the transcript.
# [12:47](https://youtu.be/KT9anz_V9ns?t=767) Setting up Endpoints and Airdrops

Section Overview: In this section, the speaker explains how to select different endpoints and troubleshoot common issues by using airdrops on Solana.

## Selecting Endpoints

- Different endpoints can be chosen by clicking on "Build" and selecting from the options available in the bottom left corner.
- If encountering problems like errors during program deployment or needing an airdrop, selecting a different endpoint may help.

## Airdrops for Troubleshooting

- To receive an airdrop, type "Solana airdrop 2" in the command line. This will initiate an RPC call to the RPC and provide free SOL tokens.
- A successful airdrop ensures that you have enough tokens to deploy your program.

# [13:35](https://youtu.be/KT9anz_V9ns?t=815) Deploying the Program

Section Overview: This section covers deploying the program on Solana, including creating new accounts and handling upgrade authority.

## Creating New Account for Deployment

- If encountering issues with upgrade authority, it is recommended to create a new account before deploying the program.
- Note that creating a new account may result in losing upgrade authority if not saved beforehand.

## Deploying Unchained Program

- The program is built and compiled into an .so file which is then stored in the data of an account.
- Due to transaction size limitations on Solana, multiple transactions are required for deploying larger programs.
- Once deployed successfully, further actions can be taken.

# [14:55](https://youtu.be/KT9anz_V9ns?t=895) Running the Client Program

Section Overview: This section focuses on running the client program after deployment and resolving any compatibility issues with program IDs.

## Updating Program ID for Client Run

- Before running the client program, ensure that the correct program ID is used. If there are compatibility issues, update the program ID accordingly.

## Running the Client Program

- To run the client program, type "run" in the command line.
- The output should display a message indicating that the journey begins and the player moves to the right.

# [15:18](https://youtu.be/KT9anz_V9ns?t=918) Understanding Solana Game Structure

Section Overview: This section provides an overview of how Solana games are structured, including program accounts and game data.

## Creating Program Account for Level

- A program account, known as a PDA (Program Derived Address), is created for each level in the game.
- PDAs are addresses derived from the program ID and specific seeds, allowing programs to sign and modify associated accounts.
- These PDAs function as database entries with tables representing different levels.

## Initializing and Modifying Game Data Account

- If an account does not exist, it is initialized with default values.
- The move right instruction increases the player's position by one.
- The move left instruction decreases the player's position by one.

# [16:31](https://youtu.be/KT9anz_V9ns?t=991) Exploring Solana Program Structure

Section Overview: This section explains how Solana programs are structured using Rust and Anchor framework.

## Introduction to Solana Programs in Rust

- Solana programs are written in Rust and utilize the Anchor framework for easier development.
- The Anchor framework provides features like serialization of accounts and signer checks to simplify working with Solana programs.

## Key Components of Game Program

- The main focus of this game program is tracking player positions.
- Initialization creates a game data account with initial player position.
- Instructions like move right or move left modify the player's position accordingly.

# [17:44](https://youtu.be/KT9anz_V9ns?t=1064) Initializing Game Data Account

Section Overview: This section covers initializing game data accounts within Solana programs using specific seeds.

## Initializing Game Data Account

- The initialize struct is used to initialize the game data account.
- The same seeds used in the client program are passed to this struct.
- The transaction pays for the space required by the account on-chain.

# [18:31](https://youtu.be/KT9anz_V9ns?t=1111) Understanding System Program and Parallel Execution

Section Overview: This section explains the role of the system program in creating new accounts and how Solana achieves parallel execution.

## Role of System Program

- The system program is necessary for creating new accounts in Solana programs.
- All accounts required by a transaction must be passed as inputs to enable parallel execution.

## Achieving Parallel Execution

- Solana's ability to execute transactions in parallel is due to its design that allows transactions not writing to the same account to be executed simultaneously.
- This parallel execution significantly enhances Solana's speed compared to other blockchains.

# [19:17](https://youtu.be/KT9anz_V9ns?t=1157) Moving Right and Left within the Game

Section Overview: This section demonstrates moving right or left within the game and provides an overview of related instructions.

## Moving Right or Left

- Instructions like move right or move left are used to change the player's position within the game.
- These instructions modify the player position stored in the game data account.
# [19:55](https://youtu.be/KT9anz_V9ns?t=1195) Player Position and Function

Section Overview: In this section, the speaker explains how the player position is increased by one using a function. They also discuss a function that prints different messages based on the player's position.

## Player Position and Function

- The player position is increased by one using the formula `player_position = player_position + 1`.
- A function is used to print different messages based on the player's position.
- If the player position is zero, it displays "A Journey Begins".
- If the player position reaches three, it displays "You reach the end".

# [20:15](https://youtu.be/KT9anz_V9ns?t=1215) Initializing an Account and Printing Animation

Section Overview: This section covers initializing an account and printing a game animation in the client.

## Initializing an Account and Printing Animation

- To initialize an account, the `playground program methods initialize` function is called.
- The necessary accounts are passed as parameters, including the new game data account and signer.
- The system program is also included for creating the account.
- After initializing, a game animation is printed in the client.

# [21:00](https://youtu.be/KT9anz_V9ns?t=1260) Moving Left and Right in the Game

Section Overview: Here, moving left and right in the game is demonstrated. The transaction details are shown in Solana Explorer.

## Moving Left and Right in the Game

- By commenting out specific lines of code, players can move left or right within the game.
- The transaction details can be viewed in Solana Explorer by copying and pasting its ID.

# [22:32](https://youtu.be/KT9anz_V9ns?t=1352) Building a Play-to-Earn Game

Section Overview: This section introduces building a play-to-earn game where players collect rewards from chests when reaching certain positions.

## Building a Play-to-Earn Game

- In this example, players transfer soil into a chest vault and collect the reward when reaching the end.
- The chest reward is represented by a diamond symbol.
- The program includes an instruction called "reset level and spawn chest" to set the player at the beginning and transfer soil into the chest vault.
- Cross-program invocation is used to call the system program for transferring soil from the payer account to the chest vault.
- The lampards are subtracted from the chest vault account and added to the player account as a workaround for limitations with cross-program invocations.

# [25:12](https://youtu.be/KT9anz_V9ns?t=1512) Transferring Soil into Chest Vault

Section Overview: This section explains how soil is transferred into the chest vault and how it differs from transferring soil between accounts.

## Transferring Soil into Chest Vault

- Soil is transferred into the chest vault using cross-program invocation.
- Cross-program invocation allows calling system programs with system accounts.
- To overcome this limitation, lampards are subtracted from the chest vault account and added to the player account.

Note: The summary has been created based on available information in English.
# [t=1609s] Creating a Soul and Chest Vault Account

Section Overview: In this section, the speaker explains how to create a soul account and a chest vault account in Solana.

## Creating the Soul Account

- To create a soul account, the Solana runtime checks if the account already exists.
- The print player function is used to display the created accounts.
- The level one account remains the same as in the previous example.

## Creating the Chest Vault Account

- The chest vault account is created similarly to other accounts.
- Using "init" ensures that the function is called only once.
- The chest world account does not contain any data, so it only requires 8 bytes for the discriminator.
- It is important to include seats when creating accounts to ensure security and ownership verification.

## Moving and Collecting

- When moving or interacting with accounts in Solana, all relevant accounts need to be included in the instruction.
- The program's main focus is on CPI (Cross Program Invocation) and transferring SOL from one account to another.

# [t=1740s] JavaScript Client and Deployment

Section Overview: This section covers deploying and testing using a JavaScript client.

## Building and Deploying

- The correct update authority needs to be set before deployment.
- Checking the chest balance before sponsoring it shows that it has 0.1 SOL less after sponsorship.
- Walking through positions one, two, and three demonstrates collecting the chest successfully.

# [t=1866s] Adding Password Protection

Section Overview: This section explains how to add password protection for collecting chests.

## Implementing Password Protection

- A password string is added for authentication purposes.
- Checking if the password matches determines whether collection of chests is allowed or not.
  
# [t=1918s] Testing Password Protection

Section Overview: This section demonstrates testing password protection functionality.

## Testing with Incorrect Password

- Providing an incorrect password results in a panic and the game stops.

## Testing with Correct Password

- Providing the correct password allows for successful collection of chests.

# [t=1944s] Viewing Error Messages on Chain

Section Overview: This section explains how to view error messages on chain.

## Adding Parameters for RPC Call

- To view error messages on chain, parameters need to be added for the RPC call.
# [33:41](https://youtu.be/KT9anz_V9ns?t=2021) Exploring the Game and Error Handling

Section Overview: In this section, the speaker demonstrates how to explore the game and handle errors in Solana programming.

## Game Exploration and Error Handling

- The speaker shows how to test the game by inputting correct and incorrect passwords. If a wrong password is entered without skipping preflight checks, the transaction fails.
- It is mentioned that although it is helpful for error investigation, users have to pay fees for failed transactions. However, since fees are cheap, it is not a significant concern.
- The speaker suggests fixing typos in passwords and creating custom error codes instead of panicking when an error occurs.
- By creating proper error handling mechanisms, different error messages can be displayed based on specific conditions (e.g., wrong password or insufficient resources).
  
# [34:55](https://youtu.be/KT9anz_V9ns?t=2095) Writing Programs Locally in Visual Studio

Section Overview: This section focuses on writing Solana programs locally in Visual Studio using auto-completion and AI assistance.

## Writing Programs Locally with Auto-completion

- Working locally in Visual Studio provides advantages such as auto-completion and AI assistance (e.g., co-pilot).
- The speaker copies code snippets to create a custom error code for better error handling.
- By returning an error instead of panicking, proper error handling can be implemented on the client-side as well.
  
# [36:05](https://youtu.be/KT9anz_V9ns?t=2165) Introduction to Tiny Adventure Game

Section Overview: This section introduces the Tiny Adventure game and explains its data structure.

## Introduction to Tiny Adventure Game

- The Tiny Adventure game features a character represented by ASCII art that can move left or right.
- The game has a data account that stores information about the character's position.
  
# [36:25](https://youtu.be/KT9anz_V9ns?t=2185) Transaction Process in Solana

Section Overview: This section explains the transaction process in Solana and how clients interact with RPC nodes.

## Transaction Process in Solana

- Clients create transactions containing instructions (e.g., move right) and send them to RPC nodes.
- RPC nodes are responsible for validating and updating the state of the transaction.
- Transactions are serialized, sent to the leader of validators, and validated by all validators.
- The updated state is then sent back to RPC nodes in small chunks called shreds.
- Clients can establish a websocket connection to an RPC node to receive real-time updates on account changes.
  
# [38:19](https://youtu.be/KT9anz_V9ns?t=2299) Real-time Updates in Solana Games

Section Overview: This section highlights the benefits of real-time updates in Solana games using websocket connections.

## Real-time Updates with Websocket Connections

- Establishing a websocket connection allows for immediate updates when account data changes.
- In games like Tiny Adventure, this enables fast and seamless updates without constant polling for data.
  
# [39:03](https://youtu.be/KT9anz_V9ns?t=2343) Tiny Adventure 2 and Game Possibilities

Section Overview: This section introduces Tiny Adventure 2 and discusses potential game enhancements.

## Introduction to Tiny Adventure 2 and Game Possibilities

- Tiny Adventure 2 is similar to its predecessor but includes additional features such as a chest vault account with seeds and leopards.
- The speaker mentions that various enhancements can be made, such as creating grids for movement or incorporating quiz elements into the game.
- Multiplayer functionality is also suggested as a possible extension of the game.
# [40:37](https://youtu.be/KT9anz_V9ns?t=2437) Connecting Wallet Configurations

Section Overview: In this section, the speaker discusses how to connect wallet configurations and token accounts in Solana. They mention that manually creating account discriminators can be inconvenient, but there is a solution to generate a C# client from the code.

## Generating a C# Client from IDL

- The IDL (Interface Description Language) is a JSON representation of the program.
- By exporting the IDL from the playground, you can convert it into a C# client.
- Install the Solara Unity Anchor tool and use the `dotnet anchor gen` command with the input as the downloaded JSON file.
- This generates a C# file that contains all the necessary data and functions for interacting with Solana accounts.

## Benefits of Using C# Client

- The generated C# client provides convenient access to data and functions in Solana accounts.
- It allows developers to build games in Unity and export them as WebGL.
- The speaker demonstrates how to call functions from C# using examples from Tiny Adventure 2.

# [43:09](https://youtu.be/KT9anz_V9ns?t=2589) Comparing JavaScript and C#

Section Overview: In this section, the speaker compares JavaScript and C# code side by side, showing their similarities when interacting with Solana transactions.

## Similarities between JavaScript and C#

- Both languages involve creating transactions, setting fee pairs, getting recent block hashes, etc.
- Block hashes are used for transaction expiration purposes.
- Pre-fetching block hashes can improve game performance by reducing RPC calls.

## Creating Transactions in C#

- The process of creating transactions in C# is similar to JavaScript.
- Set fee pairs, get recent block hash, add instructions, set account details, sign, and send transactions.

## Unity SDK Features

- The Unity SDK supports various features such as connecting to Phantom wallet and mobile connectivity via deep links.
- Developers can build mobile casual games using Solana.

# [44:55](https://youtu.be/KT9anz_V9ns?t=2695) Unity Client Overview

Section Overview: In this section, the speaker provides an overview of the Unity client for Solana and demonstrates how to use it.

## Setting Up the Unity Client

- The speaker directs viewers to check out the Tiny Adventure service repository for a detailed guide on setting up the Unity client.
- The code in Unity follows similar patterns as in the playground example.

## Interacting with Solana in Unity

- The code in Unity involves defining program IDs, creating program addresses, socket connections, deserializing data, and updating game data views.
- Functions like `getAccountInfoAsunc` are used to retrieve account information.
- Transactions can be created by setting fee pairs, getting recent block hashes, adding instructions, and sending them.

# [46:34](https://youtu.be/KT9anz_V9ns?t=2794) React Client Example

Section Overview: In this section, the speaker briefly mentions building a React client for Solana and provides a link for further exploration.

## Building a React Client

- The speaker mentions that a JavaScript-based React client is also possible.
- They provide a link where viewers can download an example of building a Solana application using React.
# [47:52](https://youtu.be/KT9anz_V9ns?t=2872) Building On-Chain Games on Solana

Section Overview: In this section, the speaker discusses how to build on-chain games on Solana and suggests various game ideas that can be implemented.

## Using Solana Mobile Wallet Adapter
- The Solana Mobile Wallet adapter is used in React to send transactions.
- It allows for the creation of a button that supports different wallets, such as Phantom or Soulflare.

## Building Transactions
- When the button is clicked, the move instruction is executed and game data is added to the account.
- A transaction builder is used to create a transaction.
- The transaction is confirmed with the latest block hash.

## Game Ideas
- Suggestions for game ideas are provided.
  - Solana Royale: Improve upon the open-source Soul Hunter game by adding features like shooting, round timers, unit spawning, and tower building.
  - Trading Card Game: Create a game similar to Hearthstone where cards can be represented as NFTs.
  - Puzzle Pirates: Develop a game with mini-games like match 3 puzzles using NFTs with different stats.
  - Idle Games: Implement idle games where players earn tokens based on time calculations and perform transactions using Clockwork.xyz framework for future automation.
  - Chess and Pool Cover: Explore creating chess and pool cover games on Solana.
  - Location-Based Games: Consider developing location-based games or an Airbnb-like platform where crypto payments are accepted.

## Additional Resources
- The speaker provides links to additional resources related to building games on Solana.

# [51:57](https://youtu.be/KT9anz_V9ns?t=3117) Conclusion and Contact Information

Section Overview: In this section, the speaker concludes the talk by expressing gratitude for listening and encourages viewers to reach out with their own game ideas. Contact information is also provided.

## Conclusion
- The speaker thanks the audience for listening and hopes they have learned something about building games on Solana.
- Encourages viewers to build their own games and share them.
- Contact information: Twitter handle is @soleplay_Jonas.

Note: The transcript provided does not include any content in a language other than English.

[Generated with Video Highlight](https://videohighlight.com/video/summary/KT9anz_V9ns)