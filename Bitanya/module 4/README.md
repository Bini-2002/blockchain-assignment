# Bitanya's Blockchain Journey: Module 4 — Advanced Solidity: Inheritance & Governance

Welcome to the fourth module of **Bitanya's** Solidity learning! This module is the capstone of the fundamentals, introducing Object-Oriented Programming (OOP) patterns in Solidity and culminating in a fully-fledged decentralized voting (Governance) contract.

---

## 🌟 What is Covered in Module 4?

This module is split into two major sections:

### 1. Solidity Inheritance
Explore the object-oriented side of Solidity. You will learn to write clean, reusable, and structured code using:
- **Base & Derived Contracts**: Creating hierarchical structures.
- **Constructors in Inheritance**: Passing arguments from child contracts to base contract constructors (e.g., `Warrior is Hero(200)`).
- **Polymorphism**: Using `virtual` in parent contracts and `override` in child contracts to redefine behavior.
- **Calling Parent Functions**: Leveraging the `super` keyword to execute parent contract logic.
- **Multi-Contract Interaction**: Allowing contracts to attack, check, and modify state across other contracts on-chain.
- **Access Control & Lifecycle**: Creating custom patterns like `Ownable` and `Transferable` contracts.

### 2. Decentralized Voting & Governance
Apply all your knowledge to build a robust voting contract (`Voting.sol`). Key mechanics include:
- **Complex Structs**: Storing proposals and vote receipts.
- **Double Mappings**: Preventing double voting using nested lookups (`mapping(uint => mapping(address => Vote))`).
- **Events**: Emitting crucial logs like `ProposalCreated` and `VoteCast`.
- **Modifiers**: Writing custom verification checks like `onlyMember`.
- **Vote Switching**: Restoring/updating vote counts when a user changes their mind.
- **On-chain Execution**: Automatically executing proposal payloads using low-level `.call` once the threshold (10 'Yes' votes) is reached!

---

## 📂 Project Structure

Here is how Bitanya's Module 4 is organized:

```text
module-4/
├── README.md               # You are here!
├── module 4 .png.jpg       # Progress snapshot
│
├── Inheritance/            # Object-Oriented Solidity Practice
│   ├── part-1/             # Collectibles, Ownable, & Transferability
│   ├── part-2/             # Warrior & Mage inheritance
│   ├── part-3/             # Abstract contract Hero with Enemy interactions
│   ├── part-4/             # Overriding attack types (Brawl vs. Spell)
│   ├── part-5/             # Implementing the Ownable modifier pattern
│   └── part-6/             # Constructing Transferable as a child of Ownable
│
└── Voting/                 # Governance & Proposal Execution
    ├── part-1/             # Basic Proposal creation struct
    ├── part-2/             # Adding members and constructor
    ├── part-3/             # Voting restrictions (members only)
    ├── part-4/             # Handling yes/no counts
    ├── part-5/             # Preventing double-voting & updating counts
    └── part-6/             # Emitting events & executing targets via .call()
```

---

## 🛠️ Setup & Compiling

Make sure you're in the right directory:
```bash
cd blockchain-assignment/Bitanya/module-4
```

### Build the contracts:
```bash
forge build
```

### Run all tests for Module 4:
```bash
forge test
```

### Run with deep traces:
```bash
forge test -vvv
```

---

## 💡 Key Highlights

### 🛡️ Inheritance Example
```solidity
// Base Contract
abstract contract Hero {
    uint public health;
    constructor(uint _health) { health = _health; }
    function attack(Enemy enemy) public virtual;
}

// Derived Contract
contract Mage is Hero(50) {
    function attack(Enemy enemy) override public {
        enemy.takeAttack(AttackTypes.Spell);
        super.attack(enemy);
    }
}
```

### 🗳️ Voting Event & Execution
```solidity
if (proposal.yesCount >= 10) {
    proposal.executed = true;
    (bool success, ) = proposal.target.call(proposal.data);
    require(success, "Proposal execution failed");
}
```

---

## 🏆 Graduation Goals for Bitanya
Upon finishing Module 4, Bitanya is fully equipped to:
1. **Design** complex smart contracts using solid OOP architecture.
2. **Implement** access controls (`onlyOwner`, `onlyMember`) securely.
3. **Handle** custom logic overrides and safely bubble up execution using `super`.
4. **Develop** an end-to-end decentralized voting engine from scratch.
5. **Manage** nested state mappings and handle low-level call execution on-chain!

Fantastic job finishing this advanced module, **Bitanya**! You're now ready to build real-world decentralized apps! 🚀🎉
