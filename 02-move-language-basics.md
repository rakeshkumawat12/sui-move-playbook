```
module move_playground::data_types {
    public fun demo() {
        let is_active: bool = true;         // Boolean
        let small_number: u8 = 200;         // u8 integer
        let big_number: u64 = 1000000;      // u64 integer
        let account: address = @0x1;        // Account address
        let numbers: vector<u8> = vector[1, 2, 3, 4, 5]; // Vector
    }
}
```