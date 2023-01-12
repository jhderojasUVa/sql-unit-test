# sql-unit-test

A POC for SQL files unit test, lint and so on independent of the database engine.

# Hooks

We use git shell hooks to make it run. The hooks are made on python, so you need python installed on your system.

# Linting

Based on [SQLFluff](https://docs.sqlfluff.com/), a Python tool for SQL Linting independent of anything.

To install, you will need to have `pip`:

`pip install sqlfluff`

## Check

Bad SQL:

`sqlfluff lint sql/bad/lint.sql --dialect ansi`

Good SQL:

`sqlfluff lint sql/good/lint.sql --dialect ansi`
