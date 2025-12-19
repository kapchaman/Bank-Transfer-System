import java.util.ArrayList;
import java.util.List;

public class Bank {

    private List<Account> accounts = new ArrayList<>();

    // optional extra (implemented)
    public Account openAccount(Customer customer, double initialBalance) {
        Account account = new Account(customer, initialBalance);
        accounts.add(account);
        return account;
    }

    // mandatory method
    public boolean transfer(Account from, Account to, double amount) {
        if (amount <= 0) {
            System.out.println("Transfer amount must be positive.");
            return false;
        }

        if (from.getBalance() < amount) {
            System.out.println("Transfer failed: insufficient funds.");
            return false;
        }

        Transaction tx = new Transaction(from, to, amount);

        from.apply(tx);
        to.apply(tx);

        System.out.println("Transfer successful: " + tx);
        return true;
    }
}
