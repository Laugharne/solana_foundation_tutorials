# [Managing large accounts on Solana](https://youtu.be/zs_yU0IuJxc) 

<!-- TOC -->

- [Managing large accounts on Solana](#managing-large-accounts-on-solana)
	- [Memory Limitations on Solana](#memory-limitations-on-solana)
- [00:25 Saving Stack Space and Creating Larger Accounts](#0025-saving-stack-space-and-creating-larger-accounts)
	- [Saving Stack Space](#saving-stack-space)
	- [Creating Larger Accounts](#creating-larger-accounts)
- [01:11 Stack Size Limit Test](#0111-stack-size-limit-test)
	- [Test Description](#test-description)
- [02:02 Zero Copy Serialization Challenge](#0202-zero-copy-serialization-challenge)
	- [Zero Copy Serialization Challenge](#zero-copy-serialization-challenge)
- [03:19 Running Tests and Analyzing Errors](#0319-running-tests-and-analyzing-errors)
	- [Running Tests](#running-tests)
	- [Analyzing Errors](#analyzing-errors)
- [04:06 Saving Stack Space with Boxing Technique](#0406-saving-stack-space-with-boxing-technique)
	- [Boxing Technique](#boxing-technique)
- [05:22 Creating Accounts Larger Than 10 Kilobytes](#0522-creating-accounts-larger-than-10-kilobytes)
	- [Increasing Account Size](#increasing-account-size)
- [06:39 Dynamic Account Size with Variable Data](#0639-dynamic-account-size-with-variable-data)
	- [Dynamic Account Size](#dynamic-account-size)
- [07:26 Increasing Account Data Size](#0726-increasing-account-data-size)
	- [Increasing Account Data Size](#increasing-account-data-size)
- [07:49 Sending Strings to Account](#0749-sending-strings-to-account)
	- [Sending Strings to Account](#sending-strings-to-account)
- [08:19 Backend Program Explanation](#0819-backend-program-explanation)
	- [Backend Program Explanation](#backend-program-explanation)
- [08:40 Running Tests and Memory Allocation Failure](#0840-running-tests-and-memory-allocation-failure)
	- [Running Tests and Memory Allocation Failure](#running-tests-and-memory-allocation-failure)
- [09:07 Re-alloc Instruction and Account Size](#0907-re-alloc-instruction-and-account-size)
	- [Re-alloc Instruction and Account Size](#re-alloc-instruction-and-account-size)
- [09:34 Zero Copy Accounts and Memory Limitations](#0934-zero-copy-accounts-and-memory-limitations)
	- [Zero Copy Accounts and Memory Limitations](#zero-copy-accounts-and-memory-limitations)
- [10:31 Creating Zero Copy Accounts](#1031-creating-zero-copy-accounts)
	- [Creating Zero Copy Accounts](#creating-zero-copy-accounts)
- [10:54 Setting Data Size for Zero Copy Account](#1054-setting-data-size-for-zero-copy-account)
	- [Setting Data Size for Zero Copy Account](#setting-data-size-for-zero-copy-account)
- [11:39 Account Loader and Partial Data Loading](#1139-account-loader-and-partial-data-loading)
	- [Account Loader and Partial Data Loading](#account-loader-and-partial-data-loading)
- [12:38 Saving Data in Zero Copy Account](#1238-saving-data-in-zero-copy-account)
	- [Saving Data in Zero Copy Account](#saving-data-in-zero-copy-account)
- [13:31 Interacting with Memory Directly](#1331-interacting-with-memory-directly)
	- [Interacting with Memory Directly](#interacting-with-memory-directly)
- [14:44](#1444)
	- [Reading Data Again in Zero Copy t=884s](#reading-data-again-in-zero-copy-t884s)
- [15:04](#1504)
	- [Test Execution and Conclusion t=904s](#test-execution-and-conclusion-t904s)

<!-- /TOC -->




Section Overview: In this section, the speaker discusses the memory limitations on Solana and introduces the stack size limit, heap size limit, and PDA account limit.

## Memory Limitations on Solana

- Stack size limit is 4 kilobytes.
- Heap size limit is 32 kilobytes.
- PDA (Program Derived Account) account limit is 10 kilobytes.

# [00:25](https://youtu.be/zs_yU0IuJxc?t=25) Saving Stack Space and Creating Larger Accounts

Section Overview: The speaker explains how to save stack space, create accounts larger than 10 kilobytes, and achieve zero-copy serialization.

## Saving Stack Space

- By boxing an account in a derived account struct and storing it on the heap, you can save stack space.
- Boxing an account creates a pointer of 16 bytes that points to the account stored on the heap.

## Creating Larger Accounts

- By default, PDA accounts created in Solana have a size limit of 10 kilobytes.
- To create larger accounts, a custom instruction called "increase account size" can be used to allocate more memory to the account.
- The cost of an account depends on its size. The command `Solana rent` can be used to determine the cost of an account.

# [01:11](https://youtu.be/zs_yU0IuJxc?t=71) Stack Size Limit Test

Section Overview: The speaker demonstrates a test for exceeding the stack size limit using big structs in an Anchor program.

## Test Description

- The test creates a new key pair and finds a PDA using specific parameters.
- An error occurs during initialization due to exceeding the stack size with large structs in the account.

# [02:02](https://youtu.be/zs_yU0IuJxc?t=122) Zero Copy Serialization Challenge

Section Overview: The speaker explains the challenge of zero-copy serialization and demonstrates how Anchor checks for stack size limits during program build.

## Zero Copy Serialization Challenge

- The speaker introduces a big struct containing an array of nine options of another struct.
- The total size of the big struct exceeds the stack size limit, causing an error during program build.
- Anchor performs a check before building to ensure that the stack size limit is not exceeded.

# [03:19](https://youtu.be/zs_yU0IuJxc?t=199) Running Tests and Analyzing Errors

Section Overview: The speaker demonstrates running tests, analyzing errors, and using a local validator for further investigation.

## Running Tests

- The command `anchor test` automatically builds and deploys the program, making it easier to run tests.
- Transaction signatures are displayed after running tests.

## Analyzing Errors

- By copying the transaction signature into an explorer pointing to a local validator, detailed error information can be obtained.
- An "excess violation stack frame" error is shown in this case.

# [04:06](https://youtu.be/zs_yU0IuJxc?t=246) Saving Stack Space with Boxing Technique

Section Overview: The speaker shares a technique to save stack space by boxing accounts using derived account structs.

## Boxing Technique

- By boxing an account in a derived account struct, only 72 bytes exceed the stack size limit instead of larger amounts when using big structs directly.
- This technique is useful for accounts larger than 16 bytes.

# [05:22](https://youtu.be/zs_yU0IuJxc?t=322) Creating Accounts Larger Than 10 Kilobytes

Section Overview: The speaker explains how to create accounts larger than 10 kilobytes by increasing their size through custom instructions.

## Increasing Account Size

- By default, PDA accounts created in Solana have a size limit of 10 kilobytes due to system program constraints.
- To create larger accounts, a custom instruction called "increase account size" can be used to allocate more memory to the account.

# [06:39](https://youtu.be/zs_yU0IuJxc?t=399) Dynamic Account Size with Variable Data

Section Overview: The speaker demonstrates how to dynamically increase the size of an account using a variable data field in a struct.

## Dynamic Account Size

- By using a variable data field in a struct and converting it from `u16` to `usize`, the account size can be increased dynamically.
- This allows for flexible allocation of memory based on the value stored in the variable data field.
# [07:26](https://youtu.be/zs_yU0IuJxc?t=446) Increasing Account Data Size

Section Overview: In this section, the speaker explains how to increase the size of account data by calling program methods multiple times.

## Increasing Account Data Size

- The speaker demonstrates how to increase the size of account data by calling program methods.
- By setting the account data to a larger value, such as 20,480 bytes, the account size can be doubled.
- This process can be repeated multiple times to further increase the account size.

# [07:49](https://youtu.be/zs_yU0IuJxc?t=469) Sending Strings to Account

Section Overview: The speaker discusses sending strings to an account and saving them in the account data field.

## Sending Strings to Account

- A loop is used to send strings (920 A's) to the account and save them in the account data field.
- This process is repeated 14 times, resulting in more than 10 kilobytes of data stored in the account.

# [08:19](https://youtu.be/zs_yU0IuJxc?t=499) Backend Program Explanation

Section Overview: The speaker provides an overview of what happens in the backend program when interacting with accounts and saving string data.

## Backend Program Explanation

- The backend program takes context and accounts as input.
- It retrieves the data holder from the accounts and pushes a passed-in string into it.
- Anchor automatically serializes and saves the updated account.

# [08:40](https://youtu.be/zs_yU0IuJxc?t=520) Running Tests and Memory Allocation Failure

Section Overview: The speaker runs tests using Anchor and encounters memory allocation failure.

## Running Tests and Memory Allocation Failure

- The command "anchor run" is used without zero copy, but it fails.
- To run all scripts, "anchor test" is used. However, running individual tests separately does not work properly.
- Memory allocation failure occurs due to exceeding memory limits when loading more data than 35 kilobytes.

# [09:07](https://youtu.be/zs_yU0IuJxc?t=547) Re-alloc Instruction and Account Size

Section Overview: The speaker examines the re-alloc instruction and the resulting increase in account size.

## Re-alloc Instruction and Account Size

- The re-alloc instruction is copied and pasted into the Explorer.
- A PDA (Program Derived Address) with a balance of 14 SOL is created, increasing the account size to 20 gigabytes.
- However, zero copy is not yet implemented.

# [09:34](https://youtu.be/zs_yU0IuJxc?t=574) Zero Copy Accounts and Memory Limitations

Section Overview: The speaker introduces zero copy accounts as a solution to memory limitations.

## Zero Copy Accounts and Memory Limitations

- To overcome memory limitations, zero copy accounts are needed.
- Zero copy accounts store data in memory on the validator instead of on the heap.
- By using certain slices of the account, up to 10 megabytes of data can be interacted with directly.
  
# [10:31](https://youtu.be/zs_yU0IuJxc?t=631) Creating Zero Copy Accounts

Section Overview: The speaker explains how to create zero copy accounts by adding attributes and setting rep types.

## Creating Zero Copy Accounts

- To create a zero copy account, add the attribute "account zero copy" and set a rep type (e.g., packed).
- Different rep types determine how data will be structured in the account.
- It is important to use this feature only when necessary due to potential serialization issues with options and enums.

# [10:54](https://youtu.be/zs_yU0IuJxc?t=654) Setting Data Size for Zero Copy Account

Section Overview: The speaker sets the data size for a zero copy account by adjusting byte values.

## Setting Data Size for Zero Copy Account

- A long string is set to 40,000 bytes using the u8 data type.
- The size is adjusted by subtracting eight bytes, which accounts for the byte discriminator set by Anchor during account initialization.

# [11:39](https://youtu.be/zs_yU0IuJxc?t=699) Account Loader and Partial Data Loading

Section Overview: The speaker explains the use of account loaders and partial data loading in zero copy accounts.

## Account Loader and Partial Data Loading

- The account type is changed to an account loader instead of a regular account.
- With an account loader, only a pointer to the account is obtained instead of loading the entire account.
- To save data in this type of account, a certain slice of the loaded data is taken and modified directly.

# [12:38](https://youtu.be/zs_yU0IuJxc?t=758) Saving Data in Zero Copy Account

Section Overview: The speaker demonstrates how to save data in a zero copy account without loading the entire account.

## Saving Data in Zero Copy Account

- A string is sent to the zero copy account along with an index value.
- Instead of loading the whole account, only a slice of the data is taken starting from the index position.
- The size of each string sent is adjusted to 912 bytes due to space limitations within transactions.

# [13:31](https://youtu.be/zs_yU0IuJxc?t=811) Interacting with Memory Directly

Section Overview: The speaker highlights how direct interaction with memory allows working with large amounts of data.

## Interacting with Memory Directly

- By interacting directly with memory, up to 10 megabytes of data can be handled without loading the entire account.
- Attempting to load and print a 40,000-byte zero copy account would fail due to exceeding heap size limitations.
# [14:44](https://youtu.be/zs_yU0IuJxc?t=884)

Section Overview: The speaker discusses the complexities of reading data again in zero copy and the benefits of having 10 megabytes accounts.

## Reading Data Again in Zero Copy [14:44](https://youtu.be/zs_yU0IuJxc?t=884s)

- When reading data again in zero copy, you need to pass in the index from where you want to read the screen.
- Zero copy makes it more complicated as you need to figure out what you actually want to do.
- Having 10 megabytes accounts can be helpful in this process.

# [15:04](https://youtu.be/zs_yU0IuJxc?t=904)

Section Overview: The speaker concludes the discussion on memory on Solana and zero copy, inviting questions from the audience.

## Test Execution and Conclusion [15:04](https://youtu.be/zs_yU0IuJxc?t=904s)

- The speaker quickly looks at how the test looks like when it runs.
- The data is chuffed into a foreign system.
- Questions about memory on Solana and zero copy are welcomed for future discussions.

[Generated with Video Highlight](https://videohighlight.com/video/summary/zs_yU0IuJxc)
