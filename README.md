# Luminati HTTP/HTTPS Proxy manager

A forward HTTP/HTTPS proxy on your side, to accelerate/compress/rotate/distribute/manage/monitor/report/log/debug traffic to your proxies around the world.

This tool requires a [Luminati](https://luminati.io/?cam=github-proxy) account.

## Features
- Highly scalable
- Connection pool for faster response time
- Easy setup for multiple configurations using a simple web interface
- Statistics
- Automatically rotate IP every X requests
- Load balancing using multiple Super Proxies
- SSL sniffing (using a self-signed certificate)
- SOCKSv5 proxy

## Installation

### Windows
- Install [Git](https://git-scm.com/download/win)
- Install [Node.js](https://nodejs.org/en/download/)
- Install Luminati Proxy from Window's command prompt:
```sh
npm install -g luminati-io/luminati-proxy
```

### Linux/MacOS
- Install Node.js (preferably using [nave](https://github.com/isaacs/nave))
- Install Luminati Proxy from the terminal prompt:
```sh
$ sudo npm install -g luminati-io/luminati-proxy
```

### Upgrade
- Use npm to upgrade
```sh
$ sudo npm install -g luminati-io/luminati-proxy
```
NOTE: In versions 0.1.x port 23000 was used by default. In version 0.2.0 this was changed to port 24000.

## Usage
```sh
$ luminati --help
Usage: luminati [options] config1 config2 ...

Options:
  --log              Log level (NONE|ERROR|WARNING|INFO|DEBUG)
                                                            [default: "WARNING"]
  --customer         Customer
  --password         Password
  --proxy            Super proxy ip or country
  --proxy_count      Minimum number of super proxies to use         [default: 1]
  --secure_proxy     Use SSL when accessing super proxy
  --zone             Zone                                       [default: "gen"]
  --country          Country
  --state            State
  --city             City
  --asn              ASN
  --dns              DNS resolving (local|remote)
  --pool_size        Pool size                                      [default: 3]
  --ssl              Enable SSL sniffing
  --max_requests     Requests per session                          [default: 50]
  --session_timeout  Session establish timeout                   [default: 5000]
  --direct_include   Include pattern for direct requests
  --direct_exclude   Exclude pattern for direct requests
  --www              Local web port                             [default: 22999]
  --socks            SOCKS5 port (local:remote)
  --history          Log history                                       [boolean]
  --database         Database path              [default: "~/.luminati.sqlite3"]
  --resolve          Reverse DNS lookup file
  --config           Config file containing proxy definitions
                                                   [default: "~/.luminati.json"]
  --iface            Interface or ip to listen on (lo, eth0, lxcbr0, br0, eth1,
                     veth01, veth02, veth03, veth04, veth0d, veth13, veth18,
                     veth1a, veth20, veth1b, veth26)
  -h, --help         Show help                                         [boolean]
  --version          Show version number                               [boolean]
  -p, --port         Listening port                             [default: 24000]
```
