# Coppercoin 3.0 core 

this project is now under open support 1/1/2022 nerdlabs.dev
#
Coppercoin is a peer-to-peer Internet currency that enables instant, near-zero cost payments to anyone in the world. 
Coppercoin is an open source, global payment network that is fully decentralized without any central authorities.
#
Coppercoin is a "WAS" hybrid scrypt PoW+PoS based cryptocurrency
Block Reward 200 Cu (HAS ENDED)
PoS Percentage  3% per year on staked coins
Last PoW Block 800.000
POS activated at Block 775.000 *
#
Total coin supply 160.000.000 *
#
Coinbase maturity 20 blocks
Target spacing 64 seconds
Target timespan 1 block
Transaction confirmations 4 blocks
#
Web Site https://coppercoin.nerdlabs.dev
#
Block Explorer https://cublocks.nerdlabs.dev
#
Mining Pool (NONE)
#
Github https://github.com/nerdlabs-dev/Coppercoin-Cu
#
Discord https://discord.gg/e9zPJfy
#
* not accurate 

## Notes for the modern builds

Block files: the blockchain is stored in a "chain" folder inside the data
directory, in files of about 25 MB (chain/blk0001.dat, chain/blk0002.dat, ...).
On first start, block files from older versions are moved into it
automatically; no resync is needed. To go back to an older version, move the
blk*.dat files from chain/ back into the data directory first.

Wallet: these builds use Berkeley DB 5.3 on both Linux and Windows. Back up
wallet.dat before opening it with them: once a 5.3 build has written to a
wallet, older builds made with Berkeley DB 4.8 can no longer open it.

Sync: blocks are downloaded from one sync peer at a time, 500 per request
(-blockbatchsize). If no new block arrives for 60 seconds the request is sent
again, and after two stalls in a row another peer is used.

Peers: Settings > Peers and Settings > Network Traffic (also tabs in the
Debug window) show every connected peer with its version, height, ping and
traffic, and a live traffic graph. RPC: getpeerinfo, getnettotals, ping,
addnode, getaddednodeinfo.
