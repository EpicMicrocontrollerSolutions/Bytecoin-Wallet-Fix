# Bytecoin-Wallet-Fix
Mac OS fix for blockchain loading error and syncing errors

I experienced problems with downloading and using the official Bytecoin wallet downloaded from: https://bytecoin.org/downloads. I saw many people were having the same problem and figured out how to fix it. This is also a fix if your wallet is taking days to sync with the blockchain, it only took me 10 minutes to download blockchain and another 10 for it to import locally through the wallet.  The issue was the files are in a hidden folder so it was hard to find the blockchain files to delete.


MAC OS X:
1. Go to the offical site for downloading the Bytecoin block chain https://blockchain.bytecoin.org and download the blocks.bin and blockindexes.bin files
2. While the download is going, follow steps 3-5
3. Open Finder
4. Press Cmd+Shift+G or select from menu Go -> Go to Folder and type ~/.bytecoin and press Enter
5. Delete blocks.bin and blockindexes.bin if they are present, leave this folder open for step 6
6. Once the files have been downloaded, open the downloads folder and move the downloaded blocks.bin and blockindexes.bin to directory ~/.bytecoin folder that you left open.

Voila, problem solved. Start the app again and you'll see the blockchain importing

Please pass this on since this seems to be a common problem that the developers aren't addressing in forums.

DONATE!!!
BCN:
BTC: 1LuWhENdBEMhsEosCwbtvUpEJJpAWQ3dZX
ZEC: t1fcyS75C94zSJ2LmLsNPKe2R6pASaDkevi
LTC: LU3X572D3Zu3adespXBq4CAH3CbDpT89V5
ETH: 0xc03cfd2c036ba8d462b7ecf0529ed8090172d6cc
ETC: 0x35291c336cd22a6876830b4c7769a2815430b02b
