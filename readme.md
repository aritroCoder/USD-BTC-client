
# Simple USD/BTC Client

This is Rust based CLI client that collects real time price of BTC in USD from the binance websocket API and saves it in a file.


## Run Locally

Clone the project

```bash
  git clone https://github.com/aritroCoder/USD-BTC-client
```

Go to the project directory

```bash
  cd USD-BTC-client
```

Run using cargo (make sure Rust is installed)

```bash
cargo run -- --mode=cache --times=10
```

## Command flags

- `--help, -h`: Show help in CLI
- `--mode, -m`: (required) Set the mode. Avalable modes are `cache`, and `read`.
- `--times, -t`: Set the number of times data is read from websocket. Default is zero.


## Modes
- `cache`: Cache mode is used to connect to websocket and collect USD/BTC data from it, and then computes and shows the average of them. The number of times data is collected is decided by the `times` flag(defaults to zero). After collection, the data is cached into a txt file.
- `read`: This mode reads the cached prices from the socket saved into the txt file and shows them into the terminal.