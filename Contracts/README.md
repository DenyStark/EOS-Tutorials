# Create contract
Simple instruction

### 1. Create

Create **.cpp** file
```
$ touch contract.cpp
```

### 2. Code)

Create your contract

### 3. Build

3.1 Build **.wasm** file
```
$ eosio-cpp -o contract.wasm contract.cpp --abigen
```

3.2 Get **public key** from wallet
```
$ cleos wallet keys
```

3.3 Create **account** for contract
```
$ cleos create account eosio contract EOS6s7LD4VvJjNBCx....................gcDzfATyEThCJJXo -p eosio@active
```

3.4 **Compile** (replace CONTRACTS_DIR with the absolute path to your contract's directory)
```
$ cleos set contract hello CONTRACTS_DIR -p contract@active
```

### 4. Run

Run function **func** 
```
$ cleos push action contract func '["bob"]' -p bob@active
$ cleos push action contract func '["alice"]' -p alice@active
```
