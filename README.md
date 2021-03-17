# Marketplace Docker

## Configuration

### Submodules

```
git submodule update --init --recursive --remote
```

### Database

1. Copy .env.sample file to .env and specify POSTGRES_USER and POSTGRES_PASSWORD

### Marketplace Backend (Escrow and REST API)

1. Specify admin seed in .env file in ADMIN_SEED field. This is the seed phrase for the account that admins Matcher contract and controls Escrow.

ADMIN_SEED=//Alice

2. Set the escrow address that matches to the privake key above:

MarketplaceUniqueAddress=5GrwvaEF5zXb26Fz9rcQpDWS57CtERHpNehXCPcNoHGKutQY

3. Set the address of Matcher contract and Unique wss endpoint

MatcherContractAddress=5H7XmZ2e3urCwYNLScQryN51xDvqjvUeLG6ffDDEz6NmyTbZ
UniqueEndpoint=ws://localhost:9944/

4. Set escrow address as an admin in the Matcher contract


### Mint Backend

1. Create collection (collection). 
    - Set collection admin (admin's seed phrase will be saved in .env file)
    - Set schema version, on-chain and off-chain schema (see create collection script in mint backend)

2. Set MINT_ADMIN_SEED in .env file to contain the collection admin seed

3. Set the MINT_COLLECTION_ID in .env file: Id of this collection


### UI



### Telegram Faucet Bot

1. Set FAUCETBOTTOKEN bot's token in .env file
2. Set faucet admin seed in FAUCET_BOT_ADMIN in .env file
3. Charge faucet address with adequate amount of tokens



## License Information

Copyright 2021, Unique Network, Usetech Professional

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.