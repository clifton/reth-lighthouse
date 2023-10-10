# reth-lighthouse

moved to reth after dealing with a lot of unreliable behavior from both geth and erigon. these compose files are modified from [those available in the reth repo](https://github.com/paradigmxyz/reth/tree/main/etc) with some changes made in order to run a validator + mev-boost.

### running

1. run `./generate-jwt.sh` to generate a jwt key used for consensus <-> execution communication
2. `cp .env.example .env` and make any edits to MEV relays or the suggested fee recipient
3. `mkdir -p ~/.reth/mainnet ~/.reth/sepolia ~/.reth/logs ~/.reth/prom ~/.reth/grafana ~/.reth/beacon`
4. `docker compose up -d`
5. if running a validator, point it at port 5052 of this host

### grafana

provided on port 3000. default creds are admin/admin

![image](https://github.com/clifton/reth-lighthouse/assets/14217/81e35458-5238-4934-92e5-4e6ef6b1a4e4)
