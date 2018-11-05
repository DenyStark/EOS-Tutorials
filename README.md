# EOS-Tutorials
EOS Dictionary

### Docker container

**Start eosio**
```
$ docker start eosio
```

**Stop eosio**
```
$ docker stop eosio
```

**Config ports**
```
$ alias cleos='docker exec -it eosio /opt/eosio/bin/cleos --url http://127.0.0.1:7777 --wallet-url http://127.0.0.1:5555'
```

### Wallet

**Create**
```
$ cleos wallet create --to-console

Creating wallet: default
Save password to use in the future to unlock this wallet.
Without password imported keys will not be retrievable.
"PW5JMrwdBV1xZEEse4....................CkV1HHJ4sk3S6K2"
```

**Open**
```
$ cleos wallet open

Opened: default
```

**List** (```*``` - unlocked wallet)
```
$ cleos wallet list

Wallets:
[
  "default *"
]
```

**Unlock**
```
$cleos wallet unlock

password: Unlocked: default
```
