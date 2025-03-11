//BankAccount
public class BankAccount {
     private String accountNumber;
     private double balance;
 
     public BankAccount(String accountNumber, double initialBalance) {
         this.accountNumber = accountNumber;
         this.balance = initialBalance;
     }
 
     public void deposit(double amount) {
         if (amount > 0) {
             balance += amount;
             System.out.println("Deposited: " + amount);
         } else {
             System.out.println("Invalid deposit amount.");
         }
     }
 
     public void withdraw(double amount) {
         if (amount > 0 && balance >= amount) {
             balance -= amount;
             System.out.println("Withdrawn: " + amount);
         } else if (amount <= 0){
             System.out.println("Invalid withdrawal amount.");
         }
         else{
             System.out.println("Insufficient balance.");
         }
     }
 
     public double getBalance() {
         return balance;
     }
 
     public static void main(String[] args) {
         BankAccount account = new BankAccount("12345", 1000.0);
 
         System.out.println("Initial balance: " + account.getBalance());
 
         account.deposit(500.0);
         System.out.println("Current balance: " + account.getBalance());
 
         account.withdraw(200.0);
         System.out.println("Current balance: " + account.getBalance());
 
         account.withdraw(1500.0);
         System.out.println("Current balance: " + account.getBalance());
 
         account.withdraw(-100);
         System.out.println("Current balance: " + account.getBalance());
 
         account.deposit(-50);
         System.out.println("Current balance: " + account.getBalance());
     }
 }
