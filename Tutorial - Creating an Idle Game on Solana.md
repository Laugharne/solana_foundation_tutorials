<!-- TOC -->

- [[]https://youtu.be/ax0Si3Vkvbo?t=0](#httpsyoutubeax0si3vkvbot0)
	- [Introduction to Clockwork and Lumberjack Game](#introduction-to-clockwork-and-lumberjack-game)
- [01:08 Understanding Thread Transactions](#0108-understanding-thread-transactions)
	- [Understanding Thread Transactions](#understanding-thread-transactions)
- [02:16 Exploring Worker Network Transactions](#0216-exploring-worker-network-transactions)
	- [Exploring Worker Network Transactions](#exploring-worker-network-transactions)
- [03:04 Code Structure and Wood Collection in Lumberjack Game](#0304-code-structure-and-wood-collection-in-lumberjack-game)
	- [Code Structure and Wood Collection in Lumberjack Game](#code-structure-and-wood-collection-in-lumberjack-game)
- [05:14 Initializing the Thread in Lumberjack Game](#0514-initializing-the-thread-in-lumberjack-game)
	- [Initializing the Thread in Lumberjack Game](#initializing-the-thread-in-lumberjack-game)
- [05:58 Conclusion and Next Steps](#0558-conclusion-and-next-steps)
	- [Conclusion and Next Steps](#conclusion-and-next-steps)
- [06:44 Understanding Clockwork Triggers](#0644-understanding-clockwork-triggers)
	- [Clockwork Triggers](#clockwork-triggers)
- [07:55 Creating Threads with Clockwork](#0755-creating-threads-with-clockwork)
	- [Creating Threads](#creating-threads)
- [09:26 Additional Uses of Clockwork](#0926-additional-uses-of-clockwork)
	- [Other Use Cases](#other-use-cases)
- [10:05 Game Logic with Anchor Program](#1005-game-logic-with-anchor-program)
	- [Game Logic Implementation](#game-logic-implementation)
- [11:11 Initializing the Game](#1111-initializing-the-game)
	- [Game Initialization](#game-initialization)
- [12:23 Creating PDAs for Game Data](#1223-creating-pdas-for-game-data)
	- [PDA Creation](#pda-creation)
- [13:35](#1335)
	- [Calculating Block Time and Setting Next Energy](#calculating-block-time-and-setting-next-energy)
	- [Possibilities for Game Development](#possibilities-for-game-development)
- [13:56](#1356)
	- [Trying Out the Program](#trying-out-the-program)
- [14:18](#1418)
	- [Recommendations for Exploration](#recommendations-for-exploration)

<!-- /TOC -->

# [Introduction to Clockwork and Lumberjack Game](https://youtu.be/ax0Si3Vkvbo?t=0) 


Section Overview: In this section, the speaker introduces a tool called Clockwork, which allows triggering transactions in the future based on certain triggers. They also mention creating a game called Lumberjack using Clockwork.

## Introduction to Clockwork and Lumberjack Game

- The speaker introduces Clockwork as an open-source tool for triggering transactions in the future.
- They mention that they built a game called Lumberjack around Clockwork.
- The Lumberjack game collects wood every 10 seconds.
- Clockwork creates a thread to trigger transactions on the program.
- Transactions performed by the thread can be observed using the Clockwork tool.

# [01:08](https://youtu.be/ax0Si3Vkvbo?t=68) Understanding Thread Transactions

Section Overview: This section focuses on understanding the transactions performed by the thread created by Clockwork.

## Understanding Thread Transactions

- The thread performs transactions every 10 seconds.
- Each transaction costs slightly more than a normal transaction due to payment to the worker network.
- Users can run their own worker and earn money by performing these transactions.
- Many different programs are already using this worker network.

# [02:16](https://youtu.be/ax0Si3Vkvbo?t=136) Exploring Worker Network Transactions

Section Overview: This section explores various transactions performed by the worker network used in conjunction with Clockwork.

## Exploring Worker Network Transactions

- There are numerous transactions being performed by different programs using the worker network.
- Some of these transactions seem related to games or other activities.
- The speaker opens several of these transactions to see what they do.

# [03:04](https://youtu.be/ax0Si3Vkvbo?t=184) Code Structure and Wood Collection in Lumberjack Game

Section Overview: This section examines the code structure of the Lumberjack game and explains how wood collection works.

## Code Structure and Wood Collection in Lumberjack Game

- The code for the Lumberjack game is written using Anchor.
- The game data struct includes information such as authority, wood count, number of lumberjacks, gold count, teeth upgrades, and updated timestamp.
- Error codes are defined for insufficient wood or gold.
- Balancing factors are defined for wood selling and gold earning calculations.
- Costs for teeth upgrades and buying new lumberjacks are also specified.
- The thread tick time is set to 10 seconds.

# [05:14](https://youtu.be/ax0Si3Vkvbo?t=314) Initializing the Thread in Lumberjack Game

Section Overview: This section focuses on initializing the thread in the Lumberjack game.

## Initializing the Thread in Lumberjack Game

- Default values are set for game data during initialization.
- The game data authority is set to the backpack wallet address.
- The updated add time is set to the current time.
- Instructions are created for the thread to call on the program.

# [05:58](https://youtu.be/ax0Si3Vkvbo?t=358) Conclusion and Next Steps

Section Overview: In this final section, the speaker concludes by summarizing progress made in collecting wood and mentions future steps like converting wood to gold and upgrading lumberjacks.

## Conclusion and Next Steps

- 16 units of wood have been collected so far.
- Wood can be converted into gold by transferring it.
- Gold can be used to upgrade lumberjacks in future steps.
# [06:44](https://youtu.be/ax0Si3Vkvbo?t=404) Understanding Clockwork Triggers

Section Overview: In this section, the speaker explains how Clockwork triggers work and provides examples of their usage.

## Clockwork Triggers

- Clockwork provides various triggers for program execution.
- The crown annotation is used as a trigger in the example.
- Examples of trigger usage include scheduling events in a game or creating time-based rewards.
- Triggers can be customized to specific dates, times, and durations.

# [07:55](https://youtu.be/ax0Si3Vkvbo?t=475) Creating Threads with Clockwork

Section Overview: This section focuses on creating threads using the Clockwork program and discusses the associated costs.

## Creating Threads

- Threads are created using cross-program invocations to the Clockwork program.
- The thread creation includes specifying the payer, system program, thread authority, and signer.
- The payer becomes the owner of the thread and can control its actions (e.g., pausing or stopping).
- However, each transaction incurs a cost in terms of Sol (SOL) cryptocurrency.
- For an idle game scenario, where frequent transactions occur, this cost may not be ideal.

# [09:26](https://youtu.be/ax0Si3Vkvbo?t=566) Additional Uses of Clockwork

Section Overview: This section explores additional use cases for utilizing Clockwork in game development.

## Other Use Cases

- Clockwork can be used to spawn random treasures or events at regular intervals in a game world.
- It can facilitate time-based bonuses or rewards for players.
- For example, every Wednesday for 24 hours, players could receive double the amount of wood in a game.
- It offers flexibility for implementing various dynamic elements within games.

# [10:05](https://youtu.be/ax0Si3Vkvbo?t=605) Game Logic with Anchor Program

Section Overview: This section delves into the game logic implemented using Anchor program functions.

## Game Logic Implementation

- The code demonstrates game logic functions such as trading wood for gold and upgrading player abilities.
- Checks are performed to ensure the player has enough resources before executing actions.
- Upgrading abilities or purchasing additional assets (e.g., Lumberjacks) requires spending in-game currency (gold).
- The code showcases how these interactions can be implemented using Anchor program functions.

# [11:11](https://youtu.be/ax0Si3Vkvbo?t=671) Initializing the Game

Section Overview: This section explains the initialization process of the game and the creation of necessary PDAs.

## Game Initialization

- The game is initialized by creating a new thread using the program's ID and a unique thread ID.
- Various accounts, including payer, system program, Clockwork program, thread address, and authority, are involved in the initialization process.
- These accounts are set up to enable future interactions with the game and control over threads.

# [12:23](https://youtu.be/ax0Si3Vkvbo?t=743) Creating PDAs for Game Data

Section Overview: This section focuses on creating Program Derived Accounts (PDAs) for game data storage.

## PDA Creation

- PDAs are created for storing game data using a combination of strings, public keys, and program IDs.
- The game data PDA is derived from the game data string, public key, and idle game program ID.
- The thread ID is derived from combining the game data string and public key.
- These PDAs serve as storage entities for different aspects of the game.

Note: Timestamps were not available for all sections.
# [13:35](https://youtu.be/ax0Si3Vkvbo?t=815)

Section Overview: This section explains how to calculate the block time and set the next energy in a program. It also mentions the possibility of using this program for various game-related functionalities.

## Calculating Block Time and Setting Next Energy

- To calculate the block time, the last timestamp from the program is taken.
- The on-chain time is used instead of current daytime.
- The last login time or last updated time from the thread is subtracted from the timestamp.
- The next energy is then set based on this calculation.

## Possibilities for Game Development

- The program can be used in strategy games to trigger automatic updates when a building is finished.
- Random monsters can be spawned on the map using this program.
- All clients need to update themselves accordingly.

# [13:56](https://youtu.be/ax0Si3Vkvbo?t=836)

Section Overview: This section encourages trying out the deployed open-source program and highlights its potential for creating various game functionalities.

## Trying Out the Program

- The program is open source, allowing users to try it out themselves.
- There are endless possibilities for what can be built with this program, especially in games.

# [14:18](https://youtu.be/ax0Si3Vkvbo?t=858)

Section Overview: This section emphasizes trying out the program and exploring its capabilities further.

## Recommendations for Exploration

- It is recommended to try out the program and experiment with its features.
- Users can discover new ways to utilize it in their own projects or games.

[Generated with Video Highlight](https://videohighlight.com/video/summary/ax0Si3Vkvbo)