# Move Language Basics – Code Examples

## Ownership Model
```
module move_playground::ownership {
    public fun example() {
        let a: u64 = 10;
        let b: u64 = a;   // ownership moves to b

        // a can’t be used here anymore
    }
}
```

## Data Types
```
module move_playground::data_types {
    public fun demo() {
        let is_active: bool = true;         // Boolean
        let small_number: u8 = 200;         // u8 integer
        let big_number: u64 = 1000000;      // u64 integer
        let account: address = @0x1;        // Account std lib address
        let numbers: vector<u8> = vector[1, 2, 3, 4, 5]; // Vector
    }
}
```

## Mutability
```
module move_playground::mutability_demo {
    public fun demo() {
        let x: u64 = 10;        // Immutable
        let mut y: u64 = 20;    // Mutable

        // x = x + 5;           // This would throw an error
        y = y + 5;              // Allowed since y is mutable
    }
}
```