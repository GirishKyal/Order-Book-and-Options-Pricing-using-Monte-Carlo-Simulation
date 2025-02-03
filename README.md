# Order-Book-and-Options-Pricing-using-Monte-Carlo-Simulation

## Overview
This project implements two fundamental components used in financial trading systems:

1. **Order Book System:** A simulation of a market order book supporting various order types, order matching, and execution.
2. **Options Pricing Model (Monte Carlo Simulation):** A C++ implementation of a Monte Carlo-based pricing model for European call and put options.

This project demonstrates high-performance computing, financial modeling, and algorithmic trading concepts, making it highly relevant for fintech, trading, and quantitative finance roles.

---

## Features
### **Order Book System**
- Supports multiple order types:
  - **Market Orders** (execute immediately at best available price)
  - **Limit Orders** (execute at a specific price or better)
  - **Stop Orders** (triggered once a price level is hit)
  - **Good-Till-Canceled (GTC) Orders** (stay active until executed or manually canceled)
  - **Fill-Or-Kill (FOK) Orders** (must be executed immediately or canceled)
- Order matching and execution based on price-time priority.
- Cancelling orders by ID.
- Real-time order book updates.
- Well-structured C++ implementation using OOP principles.

### **Options Pricing (Monte Carlo Simulation)**
- Uses Monte Carlo simulations to estimate the fair price of **European Call and Put options**.
- Incorporates **risk-free rate, volatility, and strike price** in pricing calculations.
- Implements the **Black-Scholes stochastic process** for asset price evolution.
- Uses high-performance numerical methods for large-scale simulations.

---

## Technologies Used
- **C++ (OOP, STL, Multithreading)** for performance-optimized trading and pricing algorithms.
- **Monte Carlo Simulation** for financial modeling.
- **Algorithmic Trading Concepts** for order matching and execution logic.

---

## Installation & Setup
### **Prerequisites**
- C++ Compiler (g++, clang, MSVC, etc.)
- C++ Standard Library (STL)

### **Compilation**
```bash
# Compile order book system
 g++ -o order_book ob.cpp

# Compile options pricing system
 g++ -o option_pricing mtco_option_pricing.cpp -O2 -std=c++11
```

### **Running the Programs**
```bash
# Run the order book system
 ./order_book

# Run the options pricing model
 ./option_pricing
```

---

## Code Structure
### **Order Book (ob.cpp)**
- `OrderBook` Class: Manages the order book and executes orders.
- `Order` Class: Represents an individual buy/sell order.
- `matchOrders()`: Matches orders based on price-time priority.
- `executeOrder()`: Executes trades when matching orders are found.
- `printOrders()`: Displays the order book state before and after execution.

### **Options Pricing (mtco_option_pricing.cpp)**
- `monteCarloOptionPricing()`: Uses Monte Carlo simulations to estimate option prices.
- `generateGaussianNoise()`: Generates normally distributed random values.
- `callOptionPayoff()` / `putOptionPayoff()`: Computes option payoffs.
- `main()`: Defines option parameters and runs simulations.

---

## Example Output
### **Order Book Execution Sample**
```
Order Book before matching:
Order ID: 1, Type: Market, Side: Buy, Price: 0, Quantity: 10
Order ID: 2, Type: Limit, Side: Sell, Price: 101.00, Quantity: 20
...

Matched Order ID: 1 with Order ID: 3 at Price: 99.00 quantity: 10
...
Order Book after matching:
Order ID: 2, Type: Limit, Side: Sell, Price: 101.00, Quantity: 10
...
```

### **Options Pricing Sample Output**
```
European Call Option Price: 10.47
European Put Option Price: 5.32
```

## Visualizations 
![order_book_before](https://github.com/user-attachments/assets/14c88d68-43f6-4e01-8d3a-2cf56f7c2d3a)
![order_book_after](https://github.com/user-attachments/assets/305418a9-67ef-46af-906e-0cb06d956ad2)
![mc_simulation](https://github.com/user-attachments/assets/60c45feb-ed80-4778-ac1c-d43e71323623)


---

## Future Enhancements
- Add **multithreading** for performance optimization in the order book system.
- Implement **historical volatility estimation** for improved pricing accuracy.
- Extend **Monte Carlo simulation** to include **American options pricing**.
- Introduce **real-time market data integration** for a more dynamic order book.

---

## Why This Project Matters
This project provides hands-on experience in:
✅ **Trading Algorithms** → Order book mechanics and execution strategies.
✅ **Financial Modeling** → Monte Carlo methods for derivatives pricing.
✅ **High-Performance C++ Development** → Efficient memory and execution management.
✅ **Interview Readiness** → Demonstrates key fintech skills for companies like Goldman Sachs, JPMorgan, and Morgan Stanley.

---

## Contributors
- **Girish Kyal** ([GitHub Profile](https://github.com/GirishKyal))

---

### **If you find this project useful, give it a ⭐ on GitHub!** 🚀

