# Move – Security, Storage & Testing

## Overview

This is the 4th part of the Sui & Move playlist.

In this part, we cover:
- Security Considerations: Gas optimization, reentrancy prevention, and formal verification.
- Storage in Sui: Object-centric global storage for scalability and parallelism.
- Testing: Writing and running simple Move unit tests. 

## Move Test Module
```
module move_playground::testing {
    #[test]
    fun simple_test() {
        let sum = 2 + 2;
        assert!(sum == 4); // If this fails, the test will throw an error.
    }
}
```

## Run the test with:
```
sui move test
```