# Hexagonal architecture or ports and adapters 

Hexagonal architecture is introduced by Alistair Cockburn and written on his blog in 2005.
It represents business logic. It does not care about your framework development, your technology stack and your language code. It helps you define decoupled code structure, isolated with external components and easy-to-run tests.


## Installation Guide

### Cloning a repository 

* On GitHub.com, navigate to the main page of the repository. [https://github.com/arezooq/hex_messanger]

* Above the list of files, click <>Code.

* Copy the URL for the repository.

To clone the repository using an SSH key, including a certificate issued by your organization's SSH certificate authority, click SSH, then click .

  1. Open Terminal.

  2. Change the current working directory to the location where you want the cloned directory.

  3. Type git clone, and then paste the URL you copied earlier.

    git clone git@github.com:arezooq/hex_messanger.git

  4. Press Enter to create your local clone.

    git clone git@github.com:arezooq/hex_messanger.git

     Cloning into 'hex_messanger'...
     remote: Enumerating objects: 4522, done.
     remote: Counting objects: 100% (4522/4522), done.
     remote: Compressing objects: 100% (3371/3371), done.
     remote: Total 4522 (delta 959), reused 4522 (delta 959), pack-reused 0
     Receiving objects: 100% (4522/4522), 22.08 MiB | 2.38 MiB/s, done.
     Resolving deltas: 100% (959/959), done.


### Install
* Create file go.mod:
 
   go mod init github.com/username/hex-messanger

*  Run go mod tidy to install all dependencies

### Usage

* Create database in pgAdmin 4, database

* Run go run cmd/main.go to start the application with postgres database or Run go run cmd/main.go --db=mongo with mongo database

* Connect on port localhost:5000/

### API Endpoints User

| HTTP Verbs | Endpoints | Action |
| --- | --- | --- |
| POST | /register | Register new user |
| POST | /login | Login user by email |
| GET | /users | Get all users added to the database |
| GET | /user/:id | Get single user by id|
| PUT | /user/:id | To edit the details of a single user |
| DELETE | /user/:id | To delete a single user |

### API Endpoints Message

| HTTP Verbs | Endpoints | Action |
| --- | --- | --- |
| POST | /messages | Create messages |
| GET | /messages | Get all Messages added to the database |
| GET | /message/:id | Get single message by id|
| PUT | /message/:id | To edit the details of a single message that created by specified user |
| DELETE | /message/:id | To delete a single message that created by specified user |

### Technologies Used

* [Go](https://go.dev/doc/) The Go programming language is an open source project to make programmers more productive.

* [Postgres](https://www.postgresql.org/) PostgreSQL, also known as Postgres, is a free and open-source relational database management system emphasizing extensibility and SQL compliance.

* [gorm](https://gorm.io/index.html) The fantastic ORM library for Golang.

* [mongo](https://www.mongodb.com/docs/drivers/go/current/) Welcome to the documentation site for the official MongoDB Go Driver. 

### Dependencies

* [JWT](https://pkg.go.dev/github.com/golang-jwt/jwt/v5#section-readme) JSON Web Tokens.

* [bcrypt](https://pkg.go.dev/golang.org/x/crypto/bcrypt) Package bcrypt implements Provos and Mazières's bcrypt adaptive hashing algorithm.

* [pq](https://pkg.go.dev/github.com/lib/pq) Package pq is a pure Go Postgres driver for the database/sql package.

### Authors

* [Arezoo Ghorbanzade](https://github.com/arezooq)