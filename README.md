# sql-unit-test

A POC for SQL files unit test, lint and so on independent of the database engine.

# Hooks

We use git shell hooks to make it run.

All hooks must and are done in shell script, so a unix is mandatory to push.

You will need to run this line on the directory in order to use the hooks directory `.githooks`.

`git config --local core.hooksPath .githooks/`

# Linting

Based on [SQLFluff](https://docs.sqlfluff.com/), a Python tool for SQL Linting independent of anything.

To install, you will need to have `pip`:

`pip install sqlfluff`

## Check

Bad SQL:

`sqlfluff lint sql/bad/lint.sql --dialect ansi`

Good SQL:

`sqlfluff lint sql/good/lint.sql --dialect ansi`

# Conventional commits

On the `.githooks` directory there's several hooks used by the repo to check if you are doing the things ok.

- `commit-msg`: This will check if you are following the conventional commits
- `pre-commit`: Check that there's no bad ascii characters

**Is mandatory set a subject**. This means as an example:

`feat(subject): i did something nasty`
