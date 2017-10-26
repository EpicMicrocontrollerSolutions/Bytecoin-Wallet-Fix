# Bytecoin-Wallet-Fix
Mac OS fix for blockchain loading error and syncing errors

I experienced problems with downloading and using the official Bytecoin wallet downloaded from: https://bytecoin.org/downloads. I saw many people were having the same problem and sought to figure out how to fix it. PLEASE DONATE. This is also a fix if your wallet is taking days to sync with the blockchain, it only took me 10 minutes to download blockchain and another 20-45 minutes for it to import locally through the wallet (better than 3 days).  The issue was the files are in a hidden folder so it was hard to find the blockchain files to delete.

Follow these steps exactly, if you haven't already sent BCN to your wallet address prior to it syncing; i.e., you just couldn't wait for it to sync now you're scare your money is gone.

MAC OS X, no BCN in or sent to the wallet:
1. Moving past this step will remove your wallet. If you already sent money to your wallet address, I would suggest moving all wallet files from ~/.bytecoin before moving forward. I didn't send BCN to my wallet since it wasn't synced (I’m smart). See instructions below the donation section for suggestions and steps if you had or sent BCN already.
2. Delete the Bytecoin wallet application and .dmg install files. Empty trash. Eject all Bytecoin wallet images. Seriously nothing can be on your computer associated the previous version of the Bytecoin wallet.  You're doing a fresh install through the process.
3. Open up the terminal. You can find terminal by searching for terminal in spotlight or go to Application - Utilities -Terminal.
4. Warning Step 5 will delete the entire hidden folder so you can do a fresh reinstall. EVERYTHING WILL BE GONE FROM THIS FOLDER INCLUDING YOUR WALLET FILE, which is why I say see below if you have money in your wallet.
5. Type "sudo rm -r ~/.bytecoin" in the terminal with no quotes.
6. Download the official wallet from the website https://bytecoin.org/downloads.
7. Go to the official site for downloading the Bytecoin block chain https://blockchain.bytecoin.org and download the blocks.bin and blockindexes.bin files.
8. Open the BytecoinWallet-1.1.9.3.dmg file and after install move to your application.
9. Now this is important, open the app and then immediately close it. The reason for this is the ~/.bytecoin folder wasn't re-created after installing the app, I had to launch the app for the hidden folder to create. But don't let the blockchain start syncing, seriously immediately close it I had to do this like 3 times. 
10. Press Cmd+Shift+G or select from menu Go -> Go to Folder and type ~/.bytecoin and press Enter
11. Delete blocks.bin and blockindexes.bin, they should have very kb range file sizes, and leave this folder open for step 12. You just removed the unsynced blockchain files.
12. Move the copies of blocks.bin and blockindexes.bin that you downloaded to the directory ~/.bytecoin folder that you left open in step 11. You just added the synced blockchain files.
13. Eject the disk image of the Bytecoin wallet.
14. Launch the Bytecoin wallet from the applications folder.  The blockchain will import in increments off 1000, at least for me, then there is some syncing once the app launches.

Voila, problem solved. Start the app again and you'll see the blockchain importing. It still takes awhile to sync, but this was the only way to get my wallet working.

Please pass this on since this seems to be a common problem that the developers aren't addressing in forums.

PLEASE DONATE!!!

BCN:21ya3g3yEpMAButNVy89RT6Q2dufbYwK4P1XwXXepani6GT2fKVcnEbLcTnrv5ZuDqj1STegSiCkyjemtHJPH2jh5dRaC1s (since it finally works)

BTC: 1LuWhENdBEMhsEosCwbtvUpEJJpAWQ3dZX

ZEC: t1fcyS75C94zSJ2LmLsNPKe2R6pASaDkevi

LTC: LU3X572D3Zu3adespXBq4CAH3CbDpT89V5

ETH: 0xc03cfd2c036ba8d462b7ecf0529ed8090172d6cc

ETC: 0x35291c336cd22a6876830b4c7769a2815430b02b


MAC OS X, already sent BCN to wallet:
I can't gaurentee this works, but it really makes sense after having figured out how to get the official wallet working!

1. So in the instructions above before doing anything, I would Press Cmd+Shift+G or select from menu Go -> Go to Folder and type ~/.bytecoin and press Enter
2. drag all files that have the word wallet in them to a safe and secure location, this way when you go through the instructions and remove the ~/.bytecoin folder you do no remove your wallet.  
3. Start with step 1 in the steps above the donation section. Since you already have BCN, donating shouldn't be a problem for you donate after you get this working.
3. After completing the steps above, when launching the Bytewallet there is an option to open a wallet or import a key.  Just direct the open/import to the location of your wallet files you transfered early.

LINUX:
1. Follow step 1 of MAC OS X instructions
2. cd ~/.bytecoin
3. rm blocks.bin blockindexes.bin
4. Once files have downloaded, cp /Downloads/blocks.bin ~/.bytecoin;  cp /Downloads/blockindexes.bin ~/.bytecoin; You may need to specify your home directory before /Downloads, but these should be the linux fixes for the same problem (if it exists).
