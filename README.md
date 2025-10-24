 # Library Management System (OOP)

 A simple, object-oriented Library Management System in Python. It models books, members, and common library operations such as add/search/update/delete, borrow, and return. The project is small and self-contained for learning OOP concepts.

 ## Features
 - **Books**: add, update, delete, search by keyword (title/author), track total and available copies
 - **Members**: add, update, delete, track borrowed books
 - **Borrow/Return**: enforce limits (max 3 per member), ensure availability, update counts

 ## Files
 - **operations.py**: Core classes `Book`, `Member`, `Library` and all business logic
 - **demo.py**: Quick demo that exercises typical flows
 - **test.py**: Lightweight assertions covering key behaviors

 ## Requirements
 - Python 3.8+

 ## Quick Start
 1. Run the demo:
    ```bash
    python demo.py
    ```
 2. Run the basic tests:
    ```bash
    python test.py
    ```

 ## Usage (Library API)
 ```python
 from operations import Library

 lib = Library()

 # Books
 lib.add_book("001", "Python 101", "John Doe", "Fiction", 2)
 lib.search_books("Python")          # [(isbn, title, author), ...]
 lib.update_book("001", title="New Title")
 lib.delete_book("001")

 # Members
 lib.add_member(1, "Alice", "alice@example.com")
 lib.update_member(1, email="alice@new.com")
 lib.delete_member(1)

 # Borrow/Return
 lib.borrow_book(1, "001")           # Enforces availability and 3-book limit
 lib.return_book(1, "001")
 ```

 ## Notes
 - Valid genres: `Fiction`, `Non-Fiction`, `Sci-Fi`
 - Borrow limit: 3 books per member

