# CryptoBlockChain
A direction in BlockChain

>This is the simplest implementation of blockchain.
>This blockchain has a Crypto-Currency use-case. 
>This has many features and runs on an http server mechanism
>Some features are explained below

#### Commands to run on http Server
Use the following commands on Linux to run the Block Chain
```sh
$ python3 Source.py 
$ python3 Source.py -p 5000
$ python3 Source.py -p 5001
```

### Commands to run on http server
If you are on localhost server use the following commands
  - http://localhost:5000/chain   --- To view your BlockChain
  - http://localhost:5000/mine    --- To mine new Coins
  - http://localhost:5000/        --- To check server is running
  - http://localhost:5000/nodes/register        --- To register a new node to P2P network
  - http://localhost:5000/nodes/resolve        --- To check for the longest chain and resolve your node's chain
  
- To send a transaction use Curl like the following example

```sh
$ curl -X POST -H "Content-Type: application/json" -d '{
 "sender": "d4ee26eee15148ee92c6cd394edd974e",
 "recipient": "someone-other-address",
 "amount": 5
}' "http://localhost:5000/transactions/new"
```

- To register a new node to your peer - to - peer network refer following example
```sh
$ curl -X POST -H "Content-Type: application/json" -d '{
"nodes" : ["http://127.0.0.1:5001"]
}' "http://127.0.0.1:5000/nodes/register"
```

## Dependencies
You must have the flask library and requests library installed 
Install them as following via pip
```sh
 pip install Flask==0.12.2 requests==2.18.4 
 ```
 
 Under MIT License.
 Immense gratitude to Hackernoon and Daniel.
  
 Leave a star and check out more amazing codes by Ankush Sharma

Leave a message at ankushors789@gmail.com
