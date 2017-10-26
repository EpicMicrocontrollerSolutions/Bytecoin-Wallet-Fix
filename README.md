# Bytecoin-Wallet-Fix
Mac OS fix for blockchain loading error and syncing errors

I experienced problems with downloading and using the official Bytecoin wallet downloaded from: https://bytecoin.org/downloads. I saw many people were having the same problem and sought to figure out how to fix it. PLEASE DONATE. This is also a fix if your wallet is taking days to sync with the blockchain, it only took me 10 minutes to download the complete blockchain and another 20-45 minutes for it to import locally through the wallet (better than 3 days).  The issue was the files are in a hidden folder so it was hard to find the blockchain files to delete.

Follow these steps exactly,this was the only way I could get it to work. If you haven't already sent BCN to your wallet address prior to it syncing. See after the donation section below for how to save your wallet.

MAC OS X, no BCN in or sent to the wallet:
1. Delete the Bytecoin wallet application and .dmg install files. Empty trash. Eject all Bytecoin wallet images. Seriously nothing can be on your computer associated the previous version of the Bytecoin wallet.  You're doing a fresh install through these steps.
2. Open up the terminal. You can find terminal by searching for terminal in spotlight or go to Application - Utilities -Terminal.
3. Moving past this step will remove your wallet. See instructions below the donation section for suggestions and steps if you already sent BCN to your wallet address.
4. Warning Step 5 will delete the entire hidden folder so you can do a fresh reinstall. EVERYTHING WILL BE GONE FROM THIS FOLDER INCLUDING YOUR WALLET , which is why I state see below if you have money in your wallet.
5. Type "sudo rm -r ~/.bytecoin" in the terminal with no quotes.
6. Download the official wallet from the website https://bytecoin.org/downloads.
7. Go to the official site for downloading the Bytecoin blockchain https://blockchain.bytecoin.org and download the blocks.bin and blockindexes.bin files.
8. Open the BytecoinWallet-1.1.9.3.dmg file and after install move the Bytecoin wallet to your Application folder. DO NOT LAUNCH THE APPLICATION YET.

9. In the terminal, type "cd ~/.bytecoin" with no quotes, and you should get a "No such file or directory" error.  If for some reason you don't get this error, proceed to step 10, but it seems opening Bytecoin wallet app for the first time creates the ~/.bytecoin folder. I didn't have the folder (see step 9 continued).

9 (continued). If you did get the "No such file or directory" error this is important, open the app and then immediately close it. It appears, for me at least, that launching the Bytecoin wallet app creates the ~/.bytecoin folder. But don't let the blockchain start syncing, immediately close the wallet. If it Bytecoin wallet starts syncing for more than a few seconds you'll get the blockchain error when it is finished. I closed my wallet right after opening, even before I recieved the warning that the app was from an outside developer and asking if I would allow the app to recieve data.

10. Press Cmd+Shift+G or select from menu Go -> Go to Folder. Type ~/.bytecoin and press Enter
11. Delete blocks.bin and blockindexes.bin, they should have kb range file sizes, and leave this folder open for step 12. You just removed the unsynced blockchain files.
12. Move the copies of blocks.bin and blockindexes.bin that you downloaded in step 7, to the directory ~/.bytecoin folder that you left open in step 11. You just added the synced blockchain files.
13. Eject the disk image of the Bytecoin wallet.
14. Launch the Bytecoin wallet from the applications folder.  The blockchain will import in increments off 1000, at least for me, then there is some syncing once the app launches.

Voila, problem solved.  It still takes awhile to sync (1 hour), but this was the only way to get my wallet working.

Please pass this on since this seems to be a common problem that the developers aren't addressing in forums.

PLEASE DONATE!!!

BCN:27oDMvGM2jJM1vMy26trGCD4FApMf4rxhfFaEXEuqN7J3BzB51q6LhnFr6MNqj3PGR4PGXzCGYQw7UemxRoRxCC97r6VTZt (since it finally works)

BTC: 1LuWhENdBEMhsEosCwbtvUpEJJpAWQ3dZX

ZEC: t1fcyS75C94zSJ2LmLsNPKe2R6pASaDkevi

LTC: LU3X572D3Zu3adespXBq4CAH3CbDpT89V5

ETH: 0xc03cfd2c036ba8d462b7ecf0529ed8090172d6cc

ETC: 0x35291c336cd22a6876830b4c7769a2815430b02b


MAC OS X, already sent BCN to wallet:
I can't gaurentee this works, but it makes sense after having figured out how to get the official wallet working and playing around in the wallet app.

1. So in the instructions above before doing anything, I would suggest moving all wallet files from ~/.bytecoin before moving forward. Press Cmd+Shift+G or select from menu Go -> Go to Folder and type ~/.bytecoin and press Enter
2. Drag all files that have the word wallet in them to a safe and secure location, this way when you go through the instructions and remove the ~/.bytecoin folder you do no remove your previous wallet.  
3. After moving your wallet files from ~/.bytecoin, start with step 1 in the section above the donation section. Since you already have BCN, donating shouldn't be a problem for you after you get this working.
3. After completing the steps above, when launching the Bytewallet there is an option to open a wallet or import a key.  Just direct the open/import to the location of your wallet files you transfered early.

LINUX:
This should probably work, let me know if not. Linux instructions would be similar to Mac.
1. Follow step 1 of MAC OS X instructions
2. cd ~/.bytecoin
3. rm blocks.bin blockindexes.bin
4. Once files have downloaded, cp /Downloads/blocks.bin ~/.bytecoin;  cp /Downloads/blockindexes.bin ~/.bytecoin; You may need to specify your home directory before /Downloads, but these should be the linux fixes for the same problem (if it exists).
