class BankAccount:
  def _init_(self,account_number,account_holder_name,initial_balance = 0.0):
    self.__account_number = account_number
    self.__account_holder_name = account_number
    self.__account_balance = initial_balance 
  def deposit(self,amount):
   if amount > 0:
    self.__account_balance += amount
    print("deposited ₹{}.new balance : ₹{}".format(amount,self.__account_balance))
   else:
    print("invalid deposited amount. please deposit a positive amount.")
  def withdraw(self,amount):
    if amount > 0 and amount <=  self.__account_balance: 
      self.__account_balance -= amount
      print("withdraw ₹{}. new balance: ₹{}".format(amount,self.__account_balance))
    else:
     print("invalid withdrawal amount or insufficient balance.")
  def display_balance(self):
    print("account balance for {} (account #{}".format(self._account_holder_name, self.account_number, self._account_balance))
account = BankAccount(account_number = "123456789",account_holder_name = "Hair prabu",initial_balance = 5000.0)
account.display_balance()
account.deposit(500.0)
account.withdraw(200.0)
account.withdraw(2000.0)
account.display_balance()
