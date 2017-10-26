# Bytecoin-Wallet-Fix
Mac OS fix for blockchain loading error and syncing errors

I experienced problems with downloading and using the official Bytecoin wallet downloaded from: https://bytecoin.org/downloads. I saw many people were having the same problem and figured out how to fix it. This is also a fix if your wallet is taking days to sync with the blockchain, it only took me 10 minutes to download blockchain and another 20-30 for it to import locally through the wallet (better than 3 days).  The issue was the files are in a hidden folder so it was hard to find the blockchain files to delete.

MAC OS X:
1. Go to the offical site for downloading the Bytecoin block chain https://blockchain.bytecoin.org and download the blocks.bin and blockindexes.bin files
2. While the download is going, follow steps 3-5
3. Open Finder
4. Press Cmd+Shift+G or select from menu Go -> Go to Folder and type ~/.bytecoin and press Enter
5. Delete blocks.bin and blockindexes.bin if they are present, leave this folder open for step 6
6. Once the files have been downloaded, open the downloads folder and move the downloaded blocks.bin and blockindexes.bin to directory ~/.bytecoin folder that you left open.
7. If you still have problems and can't get it to work after doing all that, see section below the donations for MAC OS X. 

Voila, problem solved. Start the app again and you'll see the blockchain importing.

Please pass this on since this seems to be a common problem that the developers aren't addressing in forums.

PLEASE DONATE!!!

BCN:

BTC: 1LuWhENdBEMhsEosCwbtvUpEJJpAWQ3dZX

ZEC: t1fcyS75C94zSJ2LmLsNPKe2R6pASaDkevi

LTC: LU3X572D3Zu3adespXBq4CAH3CbDpT89V5

ETH: 0xc03cfd2c036ba8d462b7ecf0529ed8090172d6cc

ETC: 0x35291c336cd22a6876830b4c7769a2815430b02b

TZC: Ttk84BWjYGmpKDAAmcPRcmJjhxY6RJq8eG

MAC OS X still having issues:
1. Moving past this step can remove your wallet, I would suggest moving all wallet files from ~/.bytecoin before moving forward. I didn't have money in my wallet since it wasn't established so this wasn't an issue.
2. Move the blocks.bin and blockindexes.bin files out of the ~/.bytecoin directory.  I put them back in downloads. Remove the Bytecoin wallet app, empty the trash bin. Eject all Bytecoin wallets images loaded, I did this through finder under devices.
3. Open up the mac terminal. Search for terminal in spotlight or go to Application - Utilities -Terminal
4. Warning Step 5 will delete the entire hidden folder so you can do a fresh reinstall. EVERYTHING WILL BE GONE FROM THIS FOLDER
5. sudo rm -r ~/.bytecoin
6. Now go back to your downloads and open up the BytecoinWallet-1.1.9.3.dmg file or redownload the offical wallet from the website https://bytecoin.org/downloads
7. Install and copy the wallet to your applications.  Open your applications then it should start syncing.
8. Close the Bytecoin wallet app by quitting the app, not just closing the wallet you have to quit
9. Press Cmd+Shift+G or select from menu Go -> Go to Folder and type ~/.bytecoin and press Enter
10. Delete blocks.bin and blockindexes.bin if they are present, leave this folder open for step 11
11. Move the downloaded blocks.bin and blockindexes.bin to directory ~/.bytecoin folder that you left open.
12. Relaunch the app and you should see it importing with the blockchain faster, then if you had not moved the blocks.bin and blockindexes.bin into the ~/.bytecoin directory

LINUX:
1. Follow step 1 of MAC OS X instructions
2. cd ~/.bytecoin
3. rm blocks.bin blockindexes.bin
4. Once files have downloaded, cp /Downloads/blocks.bin ~/.bytecoin;  cp /Downloads/blockindexes.bin ~/.bytecoin; You may need to specify your home directory before /Downloads, but these should be the linux fixes for the same problem (if it exists).
