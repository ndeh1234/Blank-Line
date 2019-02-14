# Blank-Line
@@ -36,29 +36,39 @@ def create_menu():

def add_book():
    new_book = ui.get_book_info()
    print("\n") # adding blank line after list of books
    store.add_book(new_book)
    print("\n") # adding blank line after list of books
    # TODO show an error message if a book is already in the store, don't add book


def show_read_books():
    read_books = store.get_books_by_read_value(True)
    print("\n") # adding blank line after list of books
    ui.show_books(read_books)
    print("\n") # adding blank line after list of books


def show_unread_books():
    unread_books = store.get_books_by_read_value(False)
    print("\n") # adding blank line after list of books
    ui.show_books(unread_books)
    print("\n") # adding blank line after list of books


def show_all_books():
    books = store.get_all_books()
    print("\n") # adding blank line after list of books
    ui.show_books(books)
    print("\n") # adding blank line after list of books


def search_book():
    search_term = ui.ask_question('Enter search term, will match partial authors or titles.')
    matches = store.book_search(search_term)
    print("\n") # adding blank line after list of books
    ui.show_books(matches)
    print("\n") # adding blank line after list of books


def change_read():
