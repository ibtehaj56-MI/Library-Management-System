# Library-Management-System
A console-based Library Management System built in C++ using linked lists and file handling.
This system allows efficient management of books, users, and transactions with persistent storage.

Features

Add and manage books
Register users
Borrow and return books
Search books (Title / Author / ISBN)
View system statistics
Sort books (Title / Author)
Persistent storage using text files
Transaction logging with timestamps

System Workflow

User Input → Menu Selection → Function Execution → Data Update → File Storage

Step-by-Step Flow:

User selects an option from the menu
System processes request:
Add Book/User → Stored in Linked List
Borrow/Return → Update availability
Search → Traverse list
Transaction is recorded (if applicable)
Data is saved to .txt files
Updated results displayed to user

System Architecture

Data Structures Used

Singly Linked Lists
Books List
Users List
Transactions List

Architecture Diagram

                +----------------------+
                |      USER (CLI)      |
                +----------+-----------+
                           |
                           v
                +----------------------+
                |   MENU CONTROLLER    |
                +----------+-----------+
                           |
        -----------------------------------------
        |                |                      |
        v                v                      v
+---------------+  +---------------+   +------------------+
|   BOOK LIST   |  |   USER LIST   |   | TRANSACTION LIST |
| (Linked List) |  | (Linked List) |   | (Linked List)    |
+-------+-------+  +-------+-------+   +--------+---------+
        |                |                     |
        ---------------------------------------
                           |
                           v
                +----------------------+
                |    FILE STORAGE      |
                | (books.txt, etc.)    |
                +----------------------+


⚙️ Tech Stack
Component	Technology
Language	C++
Data Structures	Linked Lists
Storage	File Handling (fstream)
Time Handling	<ctime>
IDE (optional)	VS Code / CodeBlocks

📂 File Structure
📁 Library-Management-System
│
├── main.cpp
├── books.txt
├── users.txt
├── transactions.txt
└── README.md

Functional Modules

Book Management
Add books
Track availability
Sort by title/author

User Management
Add user details
Maintain user records

Transaction Management
Borrow books
Return books
Log timestamped transactions

📊 System Operations
Borrow Book
Check availability
Mark as borrowed
Log transaction
Return Book
Validate book
Mark available
Log return

🔍 Search Functionality

Supports:
Title-based search
Author-based search
ISBN-based search

📈 Statistics Dashboard
Displays:
Total Books
Available Books
Borrowed Books
Total Users
Total Transactions

💾 Data Persistence
All data is stored in text files:
File Name	Purpose
books.txt	Book records
users.txt	User records
transactions.txt	Borrow/Return logs

🧩 System Flowchart
        START
          |
          v
     Display Menu
          |
          v
   User Selects Option
          |
          v
   ------------------------
   |   Process Request    |
   ------------------------
          |
          v
   Update Linked Lists
          |
          v
   Save to File System
          |
          v
   Display Output
          |
          v
        END / LOOP

🛠️ How to Run
1. Clone Repository
git clone https://github.com/your-username/library-management-system.git
cd library-management-system

3. Compile
g++ main.cpp -o library

5. Run
./library
🧪 Example Usage
1. Add Book
2. Add User
3. Borrow Book
...
Enter choice: 1

Enter Book Title: DSA
Enter Author Name: CLRS
Enter ISBN Number: 12345


⚠️ Limitations
No GUI (CLI-based)
No file loading on startup (data not reloaded into memory)
No validation for duplicate entries
Simple linear search (O(n))

🚀 Future Improvements
🔄 Load data from files at startup
🖥️ GUI (Qt / Web Interface)
🗃️ Database integration (MySQL / SQLite)
🔐 Authentication system
⚡ Faster search (Binary Search / Hashing)

📱 API integration
🤝 Contributing
Feel free to fork this repo and improve the system!
