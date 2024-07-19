# Banking Application

## Video Demo
[]

## Description
The Banking Application is a Python-based system designed to simulate basic banking operations through a menu-driven interface. Users can create accounts, log in securely, view their balance, deposit and withdraw funds, transfer money between accounts, view transaction history, update account information (name and PIN), and delete their account if needed.

## Project Overview
The project is structured into several files, each fulfilling distinct roles:

### project.py
This file serves as the core of the application, containing all primary functions responsible for executing banking operations. It manages user interactions, validates inputs, and updates data stored persistently using JSON files.

#### Key Functions:
- `create_account(accounts)`: Creates a new account with validation and an initial deposit.
- `login(accounts)`: Logs in to an existing account.
- `view_balance(accounts, account_number)`: Views the balance of an account.
- `deposit(accounts, account_number)`: Deposits money into an account.
- `withdraw(accounts, account_number)`: Withdraws money from an account.
- `transfer(accounts, account_number)`: Transfers money between accounts.
- `view_transaction_history(accounts, account_number)`: Views the transaction history of an account.
- `update_information(accounts, account_number)`: Updates account holder's information (name and PIN).
- `delete_account(accounts, account_number)`: Deletes an account.

### test_project.py
The unit testing suite designed to rigorously test the functionalities defined in `project.py`. It utilizes the `unittest` framework alongside `unittest.mock` for simulating user inputs and ensuring expected outcomes across various scenarios.

### data/accounts.json
This JSON file is employed to store account-related data such as account numbers, account holder names, PINs, current balances, and transaction histories. It facilitates seamless data retrieval and updating between sessions, ensuring continuity and accuracy in managing user accounts.

### requirements.txt
This text file has the libraries I used for the running of my application. No need to install these via `pip` as they are already part of Python's standard library.

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/just-sufyaan/banking-application.git
    ```
2. Navigate to the project directory:
    ```sh
    cd banking-application
    ```
3. (Optional) Create and activate a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```
4. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage
1. Run the application:
    ```sh
    python project.py
    ```
2. Follow the on-screen instructions to create an account, log in, and perform various banking operations.

## Running Tests
To run the unit tests, execute the following command:
```sh
python -m unittest test_project.py
```

## Design Choices and Features

### User Interface
This application uses a command-line interface (CLI) approach to ensure simplicity and accessibility for users of all technical levels. The menu-driven navigation simplifies user interactions, guiding them through each banking operation step-by-step.

### Data Management
The `accounts.json` file securely stores and manages account data, guaranteeing data confidentiality and integrity. The fast serialization and deserialization of data made possible by the usage of JSON allows for dependable and rapid access to user data.

## Future Enhancements and Roadmap
In future iterations, the Banking Application can be further enhanced with additional features and improvements, such as:

- **Graphical User Interface (GUI)**: Developing a graphical user interface (GUI) using libraries like Tkinter or PyQt to offer a more visually appealing and user-friendly experience.
- **Transaction Categorization**: Adding features for categorizing transactions (e.g., expenses, income) and generating detailed financial reports for users' convenience.

## Conclusion
The Banking Application is a reliable tool for securely and effectively handling basic banking procedures. It prioritizes operational accessibility and data security while trying to offer users a smooth experience. Utilizing the built in libraries of Python, the program provides all the necessary functionality for daily banking needs.
