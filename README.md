# Proof Of Authority Blockchain
## Developed by Aaron Galloway as part of the UNCC Fintech Bootcamp

A proof of authority blockchain was using puppeth and geth. MyCrypto was used to execute transactions as well as connect to the custom nodes.

## Important Information:
- There are two nodes in this network: rattler1 and rattler2 (information is below)
- This is a Proof Of Authority Blockchain
- Network ID is 1887

## Starting The Blockchain:
1. In a command terminal enter the following information to initiate rattler1: geth --datadir rattler1 --mine --minerthreads 1
2. In another command terminal enter the following information to initiate rattler2: geth --datadir rattler2 --port 30304 --rpc --bootnodes "enode://7cb678cd924c8af253238029d2eb9af0da193dcbe7511fa14f0b1dce3570582d83d585e5a133cac60b20e19e9206da3601e82c0d457ba4f10d9c4cbaefaa8c6d@127.0.0.1:30303" --ipcdisable

## Connecting To MyCrypto:
1. Create a new network by going to the custom network option
2. Enter network name, network ID, and access port (usually 8545)

## Connecting wallets / Making Transaction
1. In MyCrypto use the "Keystore" Option
2. Import the Keystore File for rattler1: rattler1\keystore\UTC--2021-02-16T02-00-55.809600000Z--2f9d9d99cbbc8f23e46b5df58cf570dfbef2ef98
3. Unlock using the password for rattler1: bigrattler
4. Paste the public address of rattler2 in the receiver area: 0xBF9e4105890AEE161501176f5A95CAD280392CC8
5. Send crypto and check the transaction was confirmed

### Points of note:
- As constucted the accounts will not send as the pre-fund option was accidentally omitted
- The screenshot used was of a previous network created in class where everything was funded properly to show knowledge of how to complete a transaction.

**Account Information For rattlernet**

rattler1 password: bigrattler
rattler1 public address: 0x2F9d9d99Cbbc8F23e46B5Df58Cf570DfBef2ef98
rattler1 path of secret key: rattler1\keystore\UTC--2021-02-16T02-00-55.809600000Z--2f9d9d99cbbc8f23e46b5df58cf570dfbef2ef98
rattler1 mining enode: enode://7cb678cd924c8af253238029d2eb9af0da193dcbe7511fa14f0b1dce3570582d83d585e5a133cac60b20e19e9206da3601e82c0d457ba4f10d9c4cbaefaa8c6d@127.0.0.1:30303
Start rattler1: geth --datadir rattler1 --mine --minerthreads 1

rattler2 password: bigrattler1
rattler2 public address: 0xBF9e4105890AEE161501176f5A95CAD280392CC8
rattler2 path of secret key: rattler2\keystore\UTC--2021-02-16T02-03-14.466393100Z--bf9e4105890aee161501176f5a95cad280392cc8
Start rattler2: geth --datadir rattler2 --port 30304 --rpc --bootnodes "enode://7cb678cd924c8af253238029d2eb9af0da193dcbe7511fa14f0b1dce3570582d83d585e5a133cac60b20e19e9206da3601e82c0d457ba4f10d9c4cbaefaa8c6d@127.0.0.1:30303" --ipcdisable