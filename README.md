# How to run your own node

## Step 1. Download programs
Download programs nodeos, cleos, keosd and so on at github https://github.com/supereos/eos. And add those programs to path.

## Step 2. Download genesis.json of SuperEOS
We already provide genesis.json, or you can download it from https://github.com/supereos/eos.

## Step 3. Run your own node
We already provide three scripts in directory node. The script genesis_start.sh for your first run, the script start.sh for your later run after your first run, the script hard_start.sh when you need to replay.

Notes:
- This node can only synchronize blocks from other SuperEOS nodes. It can't produce block.
- You need to reset the --p2p-peer-address in those scripts for the right SuperEOS mainnet nodes.

Of course, you can run the node with your own way. You can reference https://developers.eos.io/eosio-nodeos/docs right now because SuperEOS is forked from EOS.

## Appendix 1. Resource Requirement
You need install Ubuntu 16.04 first, because the programs nodeos, cleos, keosd was build in Ubuntu 16.04 right now.

## Appendix 2. About option --chain-state-db-size-mb
You may need increase size of option --chain-state-db-size-mb when blocks increase.

## Appendix 3. About plugin eosio::history_plugin
When you need query history transactions or actions, you may need use plugin eosio::history_plugin, and setting options such as --filter-on=*. The option --filter-on=* will need a lot of memory, right now it need 32 GB or even more.
