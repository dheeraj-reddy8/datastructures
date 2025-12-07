# 🏦 Bank Queue System (C++)

A simple, interactive console application that simulates a real-world bank queue management system. This project demonstrates the usage of the C++ Standard Template Library (STL) `std::queue` along with custom logic for queue manipulation.

## ✨ Features

The application simulates two distinct roles:

### 1. 👤 Customer
- **Queue Me**: Generate a token and join the waiting line.
- **Check Status**: View the current queue status and your specific position (e.g., "5 people ahead of you").

### 2. 👔 Bank Executive
- **Serve Next**: Call the next token number in the queue for service.
- **Delete Token**: Manually remove a specific token (e.g., if a customer leaves).
- **Show Summary**: View the complete list of tokens currently waiting.

## 🛠️ Technical Implementation

The project uses the following C++ concepts:
- **`std::queue`**: For managing the FIFO (First-In, First-Out) serving order.
- **`std::pair`**: To store Token ID and Customer Name together.
- **Custom Removal Logic**: Since `std::queue` does not support random element removal, the `removeToken` function creates a temporary queue to filter out the target token, preserving the order of others.

## 🚀 How to Run

### Prerequisites
You need a C++ compiler (like G++, Clang, or MSVC).

### Compile
```bash
g++ queue.cpp -o bank_queue
```

### Run
```bash
# On Windows
bank_queue.exe

# On Linux/macOS
./bank_queue
```

## 📝 Example Usage

1. **Start the App**: Select your role (Customer or Executive).
2. **Customer**: select "Queue Me" -> Enter Name -> Get Token #1.
3. **Customer**: select "Queue Me" again -> Enter Name -> Get Token #2.
4. **Executive**: Switch role, select "Serve Next" -> "Serving token 1".
5. **Customer**: Check status -> "Token 1 is served".

---
*Created for learning Data Structures & Algorithms with C++.*
