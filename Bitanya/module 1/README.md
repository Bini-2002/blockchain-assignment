
# Bitanya's Blockchain Journey: Module 1 — Solidity Fundamentals

Welcome to **Bitanya's** space for Module 1! This section is dedicated to exploring the core concepts of Solidity. Here, you'll find practice exercises focusing on primitive data types, functions (like `pure`, `view`, and state-modifying ones), and constructors.

---

## What's Inside?

This module is organized into two main categories to help you build a strong foundation:

1. **Data Types Exploration**: Understanding how Solidity handles variables.
2. **Function Mechanics**: Learning how to write and interact with smart contract functions.

Each topic includes hands-on smart contracts (`Contract.sol`) alongside their respective tests (`Contract.t.sol`) written using Foundry.

---

## Directory Layout

```text
module-1/
├── README.md                  # You are here!
├── module1 progress image.png # Bitanya's progress snapshot
│
├── data-types/
│   ├── booleans/              # Working with true and false
│   ├── Enum/                  # Creating custom types
│   ├── Signed-Integers/       # Math with negative numbers
│   ├── String-Literals/       # Text storage
│   └── Unsigned-Integers/     # Math with positive numbers
│
└── Solidity-Functions/
    ├── Arguments/             # Passing data to constructors
    ├── Console-Log/           # Debugging with pure functions
    ├── Double-Overload/       # Functions with the same name
    ├── Increments/            # Modifying blockchain state
    ├── Pure-Double/           # Simple calculations
    └── View-Addition/         # Reading from the blockchain state
```

---

## Getting Started for Bitanya

To run these exercises locally, make sure you have the right tools:

### Requirements
- **Git** to clone the code.
- **[Foundry](https://book.getfoundry.sh/)** to compile and test the contracts.
- A terminal of your choice.

### Quick Setup

1. **Get the code**:
   ```bash
   git clone <repo-url>
   cd blockchain-assignment/Bitanya/module-1
   ```

2. **Initialize Foundry** (if needed):
   ```bash
   forge init --no-commit --force
   ```

3. **Install Dependencies**:
   ```bash
   forge install foundry-rs/forge-std --no-commit
   ```

---

## How Bitanya Can Run the Tests

Use the following commands inside any exercise folder that acts as a Foundry project:

- Compile the code:
  ```bash
  forge build
  ```
- Run the test suite:
  ```bash
  forge test
  ```
- See detailed execution traces:
  ```bash
  forge test -vvv
  ```

---

## Exercise Details

### Part 1: Data Types

| Topic | Location | Description |
|-------|----------|-------------|
| **Booleans** | `data-types/booleans/` | Setting up `true` and `false` values. |
| **Enums** | `data-types/Enum/` | Defining a `Foods` enum to manage options. |
| **Signed Integers** | `data-types/Signed-Integers/` | Dealing with `int8` and converting types. |
| **Strings** | `data-types/String-Literals/` | Saving text data on the blockchain. |
| **Unsigned Integers**| `data-types/Unsigned-Integers/` | Using `uint256` for positive numbers. |

### Part 2: Functions

| Topic | Location | Description |
|-------|----------|-------------|
| **Constructor Args**| `Solidity-Functions/Arguments/` | Storing a `uint256` upon contract deployment. |
| **Console Log** | `Solidity-Functions/Console-Log/` | A `pure` function that returns a fixed number. |
| **Overloading** | `Solidity-Functions/Double-Overload/` | Two versions of the `double` function. |
| **Increments** | `Solidity-Functions/Increments/` | A function that increases a state variable. |
| **Pure Functions** | `Solidity-Functions/Pure-Double/` | Safely multiplying inputs without state access. |
| **View Functions** | `Solidity-Functions/View-Addition/` | Reading a state variable to perform addition. |

---

## Bitanya's Goals Achieved

By finishing this module, Bitanya has learned how to:
- Properly structure a Solidity file with `SPDX` and `pragma`.
- Use the correct primitive data types based on the situation.
- Define and utilize `enum` for readable code.
- Safely cast between different integer sizes.
- Distinguish and apply `pure`, `view`, and standard functions.
- Work with function overloading.
- Test contracts effectively using Foundry.

Awesome job, **Bitanya**! Keep up the great work! 🎉
