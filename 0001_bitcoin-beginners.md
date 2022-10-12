
# Bitcoin beginners guide - How to run bitcoin nodes in Windows (a basic approach)

This guide will teach you how to install a bitcoin node (base layer) using mainnet and testnet with two different bitcoin.conf files and data folders.
The mainnet node will run in pruned mode and use only 1.2GB for storing blocks. The old blocks will be deleted.
It was done for Windows, but the concept will work both in Linux and Mac.


1. Download the bitcoin node software and install the software but don't run it.

	https://bitcoincore.org/en/download/


2. Create the data directory:

	. Go to Start -> Run (or press WinKey+R) and run this: 

		%APPDATA%

	. Crate a folder named Bitcoin.

	. Create two folders one named mainnet and the other testnet inside the Bitcoin folder.


3. Create bitcoin.conf for mainnet:

	In the folder %APPDATA%\Bitcoin\mainnet create a bitcoin.conf using a text editor like https://notepad-plus-plus.org/downloads/  it is crucial that the file is a text file.
	Add the following lines to the file.

		# Reduce storage requirements by pruning (deleting) old blocks. This mode is incompatible with -txindex and -rescan. 
		# Warning: Reverting this setting requires re-downloading the entire blockchain. 
		# (default: 0 = disable pruning blocks, >550 = target size in MiB to use for block files)
		prune=1200


4. Create bitcoin.conf for testnet:

	In the folder %APPDATA%\Bitcoin\testnet create a bitcoin.conf using a text editor like https://notepad-plus-plus.org/downloads/  it is crucial that the file is a text file.
	Add the following lines to the file.

		# [network]
		# Network-related settings:
		chain=test


6. After installing the software, you will should have a desktop icon for the application. If don't go to start menu and create it. Then copy and paste that icon, so you have two on desktop. One for each network:


	Edit one icon and rename it to bitcoin mainnet and in properties change the target to this 

		"C:\Program Files (x86)\Bitcoin\bitcoin-qt.exe" -datadir=%APPDATA%\Bitcoin\mainnet -conf=%APPDATA%\Bitcoin\mainnet\bitcoin.conf

		Or if you get an error of target box not valid:

		"C:\Program Files\Bitcoin\bitcoin-qt.exe" -datadir=%APPDATA%\Bitcoin\mainnet -conf=%APPDATA%\Bitcoin\mainnet\bitcoin.conf		


	Edit the other icon and rename it to bitcoin testnet and in properties change the target to this 

		"C:\Program Files (x86)\Bitcoin\bitcoin-qt.exe" -datadir=%APPDATA%\Bitcoin\testnet -conf=%APPDATA%\Bitcoin\testnet\bitcoin.conf

		Or if you get an error of target box not valid:

		"C:\Program Files\Bitcoin\bitcoin-qt.exe" -datadir=%APPDATA%\Bitcoin\testnet -conf=%APPDATA%\Bitcoin\testnet\bitcoin.conf


7. You are good to go!! Get bitcoin testnet in provided faucets.




More:

https://www.lopp.net/

https://developer.bitcoin.org/reference/rpc/

https://github.com/bitcoinbook/bitcoinbook

https://bitcointalk.org/index.php?topic=5237763.0 (testnet faucets)


Tips:

clyde_nakamoto@coinos.io

https://coinos.io/clyde_nakamoto
