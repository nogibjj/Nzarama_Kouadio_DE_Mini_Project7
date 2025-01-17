Download the latest binary built via CI/CD. The binary is generated and stored after every successful run of the pipeline.
[![CI](https://github.com/nogibjj/Nzarama_Kouadio_DE_Mini_Project7/actions/workflows/CI.yml/badge.svg)](https://github.com/nogibjj/Nzarama_Kouadio_DE_Mini_Project7/actions/workflows/CI.yml)

## Mini Project 7: Rust CLI Project: Database Operations with Simple CRUD

This project demonstrates how to perform basic CRUD (Create, Read, Update, Delete) operations using a Command Line Interface (CLI) built with Rust. The CLI simulates database-like operations, which allows to create tables, insert data, query the contents, and delete tables.

# Project Overview
The CLI supports the following operations:

- **Create**: Create a table with specified columns.

- **Insert**: Insert rows of data into a specified table.

- **Query**: Display the contents of a table.

- **Delete**: Remove a table from the database.

The project uses JSON to store table data, allowing persistence between runs. Data is saved in the db.json file.

# Binary Artifact

A pre-built binary executable is provided via the GitHub Actions CI/CD workflow. It can be downloaded directly from the GitHub Actions artifacts.

- Go to the GitHub Actions tab of this repository.
- Select the latest workflow run.
- Download the `release-binary` artifact.

# Set Up Instructions

You can interact with the project either by running it directly from source code using cargo or by using the provided binary executable. Follow the instructions below for each method.

> 1. Running from Source

- Install Rust on your machine

- Clone the repository: git clone https://github.com/nogibjj/Nzarama_Kouadio_DE_Mini_Project7.git

- Navigate to the project directory: cd sqlite

- Run the following to build and run the project: `cargo build` and `cargo run -- <command>`

> 2. Using the Binary Executable

- To build the binary, navigate to the project root and run `cargo build --release`

- Navigate to target/release: `cd target/release`

- Run the binary: `./sqlite <command> <options>`

# Important File Elements

- `main.rs`: The main Rust file containing the CLI logic and CRUD operations.

- `db.json`: The file where table data is stored.

- `Cargo.toml`: Rust package file with dependencies.

# Explanation of JSON Database

The CLI tool uses a simple JSON file (db.json) to store all table data. Each table consists of a set of columns and rows. The database is saved after each operation to ensure persistence between program executions.

# Run Commands via Source Code

> Create Table

`cargo run -- create <tablename> <column1> <column2> ...`

> Insert Data into Table

`cargo run -- insert <table_name> <value1> <value2> ... <valueN>` 

> Query Table

` cargo run -- query <table_name> `

> Delete Table

`cargo run -- delete <table_name>`

> Example: We create a table called users with columns id, name, and age. Then, insert a row into the users table with the values 1, "Alice", and 30. Then, we displays all rows of the users table. Finally, we delete the table. 

![alt text](sqlite/Images/SourceCode.png)

# Run Commands via the Binary

> Create Table

`./sqlite create <tablename> <column1> <column2> ...`

> Insert Data into Table

`./sqlite insert <tablename> <value1> <value2> ...`

> Query Table

`./sqlite query <tablename>`

> Delete Table

`./sqlite delete <tablename>`

> Example: Reproducing the same example as before

![alt text](sqlite/Images/Binary.png)



