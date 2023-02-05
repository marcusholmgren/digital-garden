# Digital Garden

[![Rust](https://github.com/marcusholmgren/digital-garden/actions/workflows/rust.yml/badge.svg)](https://github.com/marcusholmgren/digital-garden/actions/workflows/rust.yml)

A CLI tool for the creation and maintenance of Digital Gardens.

## Run and test

Given that you have Rust installed locally. Navigate into the cloned folder and issue the following commands for running application and tests.

Run the application
```
cargo run
```

Run the application with argument to write new post
```
cargo run -- write
```

Run the application and use Visual Studio Code as your default editor

```
EDITOR="code -w" cargo run -- write
```

Set garden path and run with VS Code
```
GARDEN_PATH=~/.garden && EDITOR="code -w" cargo run -- write
```

### Runs the test suite
Test suite require execute permission on `tests/fake-editor.sh`

```
chmod +x ./tests/fake-editor.sh
```

```
cargo test
```


## Commands

```shell
GARDEN_PATH=~/github/my-digital-garden garden write
garden -p ~/github/my-digital-garden write
garden --garden_path ~/github/my-digital-garden write
```

## Write

Open a new file to write in our digital garden.
Since we don't necessarily know what we want to title what we're writing,
we'll leave the title as option and ask the user for it later if they don't provide it up-front. 

```shell
garden write
garden write -t "Some Title"
```

## cargo-dist

Use cargo-release to create release pipeline. See article [release engineering is exhausting so here's cargo-dist](https://blog.axo.dev)

```shell
# cut a release
cargo release 0.1.0
```

## Credits

[Chris Biscardi](https://egghead.io/instructors/chris-biscardi) for creating the [Creating a Digital Garden CLI with Rust](https://egghead.io/courses/creating-a-digital-garden-cli-with-rust-34b8) course.
