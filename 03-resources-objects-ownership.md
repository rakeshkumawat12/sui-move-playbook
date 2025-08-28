# Sui3 – Resources, Objects, Ownership, Modules & Token

## Objects Demo
```
module move_playground::objects_demo {

    use sui::object::UID;

    public struct MyObject has key {
        id: UID,    
        value: u64, 
    }
}
```

## Ownership Demo
```
module move_playground::ownership_demo {
    use sui::transfer;

    struct MyObject has key {
        id: UID,
        value: u64,
    }

    public fun send_object(obj: MyObject, recipient: address) {
        transfer::transfer(obj, recipient);
    }
}
```

## Module Demo
```
module move_playground::hello_move {
    public struct Message has copy, drop {
        value: vector<u8>,
    }

    public fun say_hello(): vector<u8> {
        b"Hello, Move!"
    }
}
```

## Visibility Demo
```
module move_playground::visibility_demo {
    use std::debug;

    // private function
    fun hidden_logic() {
        debug::print(&b"Only this module can use me!");
    }

    // public function
    public fun helper() {
        debug::print(&b"Other modules can call me!");
    }

    // entry function
    entry fun run_from_transaction() {
        debug::print(&b"Users can call me via a transaction!");
    }
}
```

## My Token Module
```
module move_playground::my_token {

    // Define a token struct
    struct Token has key {
        id: UID,
        balance: u64,
    }

    // entry function to create a new token
    entry fun mint(recipient: address, amount: u64) {
        let token = Token {
            id: object::new(),
            balance: amount,
        };
        transfer::transfer(token, recipient);
    }

    // public function to read balance
    public fun get_balance(token: &Token): u64 {
        token.balance
    }
}
```