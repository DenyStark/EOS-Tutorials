# Code

```
#include <eosiolib/eosio.hpp>
#include <eosiolib/print.hpp>

using namespace eosio;

class hello : public contract
{
  public:
    using contract::contract;

    [[eosio::action]] void hi(name user) {
        require_auth(user);
        print("Hello, ", name{user});
    }
};
EOSIO_DISPATCH(hello, (hi))
```

### Description

Include **eosio libs** and **namespace**
```
#include <eosiolib/eosio.hpp>
#include <eosiolib/print.hpp>
```

Mark function as **contract action**
```
[[eosio::action]] void hi(name user) {
``` 

Check is the ```user``` **the author** of this contract
```
require_auth(user);
```

Add **action dispatch**
```
EOSIO_DISPATCH(hello, (hi))
```
