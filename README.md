# ATM-Simultaneous-System
The ATM Simultaneous System is a multi-threaded Python application that simulates real-world ATM behavior where multiple users can access their accounts and perform transactions at the same time. 
It addresses concurrency issues like race conditions and ensures data integrity when several customers withdraw, deposit, or check balances concurrently. 
The system mimics how actual bank servers handle thousands of ATM requests without data corruption or incorrect balances.
This system supports core ATM operations: balance inquiry, cash withdrawal, cash deposit, PIN change, and mini statement generation. The main highlight is simultaneous access — 2 or more users can log in from different instances and perform transactions concurrently.
Thread safety is implemented using threading.Lock to prevent conflicts when updating account balances.
It also includes user authentication with 3-attempt PIN validation, transaction logging with timestamps, and automatic account locking after failed attempts. All data is stored in files or SQLite/MySQL to maintain persistence across sessions.
Built with Python 3.x, the project uses the threading module to handle concurrent users and Lock/RLock for thread synchronization. getpass ensures PINs are hidden during input, while datetime records transaction times.
Data is managed using SQLite via the sqlite3 module or text/JSON files for lightweight setups. Exception handling covers invalid inputs, insufficient balance, and database errors. 
