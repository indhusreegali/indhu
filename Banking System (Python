class BankAccount:
    def __init__(self, account_holder, balance=0):
        """Initialize a bank account with an account holder's name and optional initial balance."""
        self.account_holder = account_holder
        self.balance = balance

    def deposit(self, amount):
        """Deposit a certain amount into the bank account."""
        if amount > 0:
            self.balance += amount
            print(f"Deposited {amount}. New balance: {self.balance}")
        else:
            print("Deposit amount must be positive.")

    def withdraw(self, amount):
        """Withdraw a certain amount from the bank account."""
        if amount > 0 and amount <= self.balance:
            self.balance -= amount
            print(f"Withdrew {amount}. New balance: {self.balance}")
        elif amount > self.balance:
            print("Insufficient funds.")
        else:
            print("Withdrawal amount must be positive.")

    def transfer(self, target_account, amount):
        """Transfer money to another bank account."""
        if amount > 0 and amount <= self.balance:
            self.balance -= amount
            target_account.balance += amount
            print(f"Transferred {amount} to {target_account.account_holder}.")
        else:
            print("Insufficient funds or invalid amount.")

    def get_balance(self):
        """Return the current balance of the account."""
        return self.balance

    def __str__(self):
        """Return a string representation of the bank account."""
        return f"Account holder: {self.account_holder}, Balance: {self.balance}"


# Example of usage
if __name__ == "__main__":
    # Create two bank accounts
    account1 = BankAccount("Alice", 1000)
    account2 = BankAccount("Bob", 500)

    # Print initial account details
    print(account1)
    print(account2)

    # Deposit money into Alice's account
    account1.deposit(500)

    # Withdraw money from Bob's account
    account2.withdraw(200)

    # Transfer money from Alice to Bob
    account1.transfer(account2, 300)

    # Print final account details
    print(account1)
    print(account2)
