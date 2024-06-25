# fuff_cookbook



## Introduction

FFUF (Fuzz Faster U Fool) is a powerful web fuzzer written in Go. It is designed for fast and flexible web fuzzing tasks such as directory discovery, virtual host discovery (without DNS records), and GET and POST parameter fuzzing. FFUF is known for its speed, ease of use, and extensive customization options.

## Key Features

- **High Performance**: Leverages Go's concurrency model to provide high-speed fuzzing.
- **Flexibility**: Supports multiple fuzzing techniques, including directory discovery, virtual host discovery, and parameter fuzzing.
- **Customization**: Allows extensive customization of fuzzing tasks with various options and switches.
- **User-Friendly**: Provides a simple and intuitive command-line interface.

## Installation

### Prerequisites

- Go (version 1.11 or later)

### Steps

1. Install Go from the [official Go website](https://golang.org/dl/).
2. Set up your Go environment. Ensure `$GOPATH/bin` is in your `$PATH`.
3. Install FFUF using the following command:
    ```sh
    go install github.com/ffuf/ffuf@latest
    ```

## Basic Usage

### Directory Discovery

To perform a directory discovery on a target website, use the following command:
```sh
ffuf -w /path/to/wordlist -u http://target/FUZZ

Virtual Host Discovery

ffuf -w /path/to/wordlist -u http://target -H "Host: FUZZ.target"

GET and POST Parameter Fuzzing

ffuf -w /path/to/wordlist -u "http://target/page?param=FUZZ"

To fuzz POST parameters:

ffuf -w /path/to/wordlist -X POST -d "param1=value1&param2=FUZZ" -u "http://target/page"

Advanced Usage
Multiple Wordlists

ffuf -w /path/to/wordlist1:/path/to/wordlist2 -u http://target/FUZZ

Output Options

ffuf -w /path/to/wordlist -u http://target/FUZZ -o output.json -of json

Filtering and Matching

ffuf -w /path/to/wordlist -u http://target/FUZZ -fc 404 -fw 12 -fl 2





This README provides a comprehensive overview of FFUF, covering its features, installation, usage, advanced options, and contribution guidelines. It's structured to be easily searchable and informative for anyone interested in using or learning about FFUF.







