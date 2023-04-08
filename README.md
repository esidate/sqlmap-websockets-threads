# SQLmap Websocket Threads

Tool to proxy sqlmap requests to a websocket server, with support for multiple threads.

## Usage

```sh
pip install websocket-client rich

# usage: proxy.py [-h] -u URL -p PAYLOAD [-o PORT] [-t THREADS] [--json]
# proxy.py: error: the following arguments are required: -u/--url, -p/--payload

python proxy.py -u ws://server:9001 -p '{"id": "%param%"}' --json -o 9090 -t 10
sqlmap -u "http://localhost:9090/?param1=1" --batch --level 5 --risk 3 --thread 10 --dbs
```

## Credits

This tool is based on the work of [BKreisel/sqlmap-websocket-proxy](https://github.com/BKreisel/sqlmap-websocket-proxy)
