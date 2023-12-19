# PizzaHut Smart Contract 

## Overview

The PizzaHut smart contract is a simple Solidity contract that allows customers to place pizza orders with a specified quantity of pizzas. The contract is designed to be used by a pizza restaurant, where the shopkeeper is responsible for managing and canceling orders.

## Smart Contract Details

### Contract Structure

- **PizzaHut**: The main contract representing the pizza restaurant.
  - **Variables**:
    - `shopkeeper`: The address of the restaurant owner.
    - `num_pizza`: A mapping from customer addresses to the number of pizzas they have ordered.

  - **Events**:
    - `OrderPlaced`: Triggered when a customer places a pizza order, indicating the customer's address and the number of pizzas ordered.
    - `OrderCancelled`: Triggered when the restaurant cancels an order, indicating the restaurant owner's address.

  - **Modifiers**:
    - `Restaurent`: A modifier that restricts certain functions to be called only by the restaurant owner.

  - **Functions**:
    - `constructor`: Initializes the contract and sets the shopkeeper as the address deploying the contract.
    - `placeOrder`: Allows customers to place pizza orders with a specified quantity. Requires a minimum order of two pizzas.
    - `cancelOrder`: Allows the restaurant owner to cancel an order. Can only be called by the restaurant owner and only if the order contains more than 50 pizzas.

### Usage

1. **Deploy the Contract**: Deploy the PizzaHut contract to the Ethereum blockchain.

2. **Place an Order**:
   - Customers can call the `placeOrder` function to order pizzas. The order must contain a minimum of two pizzas.

3. **Cancel an Order**:
   - The restaurant owner can call the `cancelOrder` function to cancel an order. The order can only be canceled if it contains more than 50 pizzas.

## Development and Testing

The contract is developed in Solidity version 0.8.0. Developers can use tools like Remix or Truffle for development, testing, and deployment.


### Testing

1. Test placing orders with different quantities.
2. Test canceling orders with varying quantities, ensuring that only the restaurant owner can cancel orders and only if the order contains more than 50 pizzas.

## License

This smart contract is licensed under the MIT License. See the `LICENSE` file for details.

## Author

Shashank S R

shashanksr762@gmail.com
