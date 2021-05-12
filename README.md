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

Runs the test suite
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


## Credits

[Chris Biscardi](https://egghead.io/instructors/chris-biscardi) for creating the [Creating a Digital Garden CLI with Rust](https://egghead.io/courses/creating-a-digital-garden-cli-with-rust-34b8) course.
