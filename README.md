![image](https://cdn.qwertycoin.org/images/press/other/qwc-github-3.png)
#### Master Build Status
[![Build Status](https://travis-ci.org/qwertycoin-org/blockchain-data-collection-agent.svg?branch=master)](https://travis-ci.org/qwertycoin-org/blockchain-data-collection-agent) [![Build status](https://ci.appveyor.com/api/projects/status/github/qwertycoin/blockchain-data-collection-agent?branch=master&svg=true)](https://ci.appveyor.com/project/qwertycoin/blockchain-data-collection-agent/branch/master)

[![NPM](https://nodei.co/npm/qwertycoin-bdca.png?downloads=true&stars=true)](https://nodei.co/npm/qwertycoin-bdca/)

# Qwertycoin fork of TurtlePay™ Blockchain Data Collection Agent (BDCA)

## Prerequisites

* [Qwertycoin](https://github.com/qwertycoin-org/qwertycoin) (development branch)
* MariaDB/MySQL with InnoDB support
* [Node.js](https://nodejs.org/) LTS

## Foreword

We know that this documentation needs cleaned up and made easier to read. We'll compile it as part of the full documentation as the project works forward.

## Setup

1) Clone this repository to wherever you'd like the API to run:

```bash
git clone https://github.com/qwertycoin-org/blockchain-data-collection-agent
```

2) Install the required Node.js modules

```bash
cd blockchain-data-collection-agent && npm install
```

3) Use your favorite text editor to change the values as necessary in `config.json`

**Note:** Make sure you use a limited database user for security reasons

```javascript
{
  "mysql": {
    "host": "localhost",
    "port": 3306,
    "username": "root",
    "password": "password",
    "database": "turtlecoin",
    "connectionLimit": 10
  },
  "node": {
    "host": "localhost",
    "port": 8197
  }
}
```

4) Load the database schema from `schema.sql` into your configured database.

5) Fire up the script

```bash
node index.js
```

6) Optionally, install PM2 or another process manager to keep the service running.

```bash
npm install -g pm2@latest
pm2 startup
pm2 start index.js --name blockchain-data-collection-agent
pm2 save
```

6) Wait to build your database cache (this is likely to take days)

## Donate

```
QWC: QWC1K6XEhCC1WsZzT9RRVpc1MLXXdHVKt2BUGSrsmkkXAvqh52sVnNc1pYmoF2TEXsAvZnyPaZu8MW3S8EWHNfAh7X2xa63P7Y
```
```
BTC: 1DkocMNiqFkbjhCmG4sg9zYQbi4YuguFWw
```
```
ETH: 0xA660Fb28C06542258bd740973c17F2632dff2517
```
```
BCH: qz975ndvcechzywtz59xpkt2hhdzkzt3vvt8762yk9
```
```
XMR: 47gmN4GMQ17Veur5YEpru7eCQc5A65DaWUThZa9z9bP6jNMYXPKAyjDcAW4RzNYbRChEwnKu1H3qt9FPW9CnpwZgNscKawX
```
```
ETN: etnkJXJFqiH9FCt6Gq2HWHPeY92YFsmvKX7qaysvnV11M796Xmovo2nSu6EUCMnniqRqAhKX9AQp31GbG3M2DiVM3qRDSQ5Vwq
```

#### Thanks

Cryptonote Developers, Bytecoin Developers, Monero Developers, Karbo Developers, Qwertycoin Community

###### (c) 2018 TurtlePay™ Development Team
