# Code

Clone code from eosio github
```
$ git clone https://github.com/EOSIO/eosio.contracts --branch v1.4.0 --single-branch
```

### Decsription

**Create token-contract** (only contract owner)
```
$ cleos push action eosio.token create '[ "eosio", "1000000000.0000 SYS"]' -p eosio.token@active
```

**Issue tokens** (only token-contract owner)
```
$ cleos push action eosio.token issue '[ "alice", "100.0000 SYS", "memo" ]' -p eosio@active
```

**Transfer tokens**
```
$ cleos push action eosio.token transfer '[ "alice", "bob", "25.0000 SYS", "m" ]' -p alice@active
```

**Check balance**
```
$ cleos get currency balance eosio.token bob SYS
```
