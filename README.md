# Book Shelf API idea

#### Why Bookshelf API?

I have so many books in my book shelf and lose track of the books that I have. At the moment, to find out if I have a book in my book shelf I have to manually search for each book in my shelf which worst case takes linear time. With this API, I can make a GET request and find out if I currently have the book instantly!

#### Downside

I have to manually add each book to the SQL table which may be time consuming. However, once I have every book in my bookshelf, I can add, remove, and look up for each book that I have.

### SQL Diagram
<img width="652" alt="Screen_Shot_2022-10-23_at_5 41 53_PM" src="https://user-images.githubusercontent.com/24259728/197421663-ecf2fc49-15e4-4a61-96db-4b0ff8a18722.png">

| Api              | Description     | Request Body | Response Body     | SQL Command | 
| :--------        | :------- | :-------- | :------- | :--------------- |
| `GET /api/bookshelf/` | Get books in bookshelf | None | Array of Book Names in shelf | `SELECT * FROM Books;`|
| `GET /api/bookshelf/{id}` | Get book details by id | None | Book details | `SELECT * FROM Books WHERE Id = {id};` |
| `POST /api/bookshelf/` | Add new book | Book Details | None     | `INSERT INTO Books "..." VALUES "...."` |
| `PUT /api/bookshelf/{id}` | Update existing book | Book Details | None     | `UPDATE Books`, `SET "..." = "..."`, `WHERE Id = {id};`|
| `DELETE /api/bookshelf/{id}` | Delete existing book | Book Details | None     | `DELETE Books` , `WHERE Id = {id}`|
