
[![Release](https://img.shields.io/github/release/ctubio/Krypto-trading-bot.svg)](https://github.com/ctubio/Krypto-trading-bot/releases)
[![Platform](https://img.shields.io/badge/platform-unix--like-111111.svg)](https://www.gnu.org/)
[![g0t0 Counter](https://tinyurl.com/g0t0search)](https://tinyurl.com/g0t0docs)
[![Code Size](https://img.shields.io/github/languages/code-size/ctubio/Krypto-trading-bot.svg)](https://github.com/ctubio/Krypto-trading-bot)
[![Software License](https://img.shields.io/badge/license-ISC-551a8b.svg)](https://raw.githubusercontent.com/ctubio/Krypto-trading-bot/master/LICENSE)
[![Software License](https://img.shields.io/badge/license-MIT-551a8b.svg)](https://raw.githubusercontent.com/ctubio/Krypto-trading-bot/master/COPYING)

[`K`](https://github.com/ctubio/Krypto-trading-bot) is a family of (very customizable) very low latency [market making](https://github.com/ctubio/Krypto-trading-bot/blob/master/doc/MANUAL.md#what-is-market-making) trading bots with a fully featured [web interface](https://github.com/ctubio/Krypto-trading-bot#web-ui).<br />It can place or cancel orders on [compatible exchanges](https://github.com/ctubio/Krypto-trading-bot#compatible-exchanges) in less than a few milliseconds per order on a decent machine.

If you don't want to configure or hardcode your own trading strategies in your own machine,<br />
you can fund liquidity pools of automated market makers at [tinyman.org](https://tinyman.org/) (or at any other defi out there),<br />just remember:
- <b><ins>never write on any defi website your private keys</ins></b> (you have to sign transactions, not to share your wallet keys)
- <b><ins>never tell anyone on any chat your private keys</ins></b> (if you have questions, use a public forum and reject impostors)

### <img src="https://github.githubassets.com/images/icons/emoji/unicode/1f4be.png" height="64" width="64"  align="middle" /> Latest version at https://github.com/ctubio/Krypto-trading-bot <img src="https://github.githubassets.com/images/icons/emoji/unicode/1f51e.png" height="64" width="64" align="middle" /> <img src="https://github.githubassets.com/images/icons/emoji/unicode/1f4b8.png" height="64" width="64" align="middle" />

[![Build Status](https://github.com/ctubio/Krypto-trading-bot/workflows/test/badge.svg)](https://github.com/ctubio/Krypto-trading-bot/actions)
[![Coverage Status](https://img.shields.io/coveralls/ctubio/Krypto-trading-bot/master.svg)](https://coveralls.io/r/ctubio/Krypto-trading-bot?branch=master)
[![Quality Status](https://img.shields.io/badge/review-clang--tidy%20+%20pvs-4cc61e.svg)](https://www.codacy.com/gh/ctubio/Krypto-trading-bot/dashboard)
[![Open Issues](https://img.shields.io/github/issues/ctubio/Krypto-trading-bot.svg)](https://github.com/ctubio/Krypto-trading-bot/issues)
[![Last Commit](https://img.shields.io/github/last-commit/ctubio/Krypto-trading-bot.svg)](https://github.com/ctubio/Krypto-trading-bot)
[![Downloads Last Releases](https://img.shields.io/github/downloads/ctubio/Krypto-trading-bot/total.svg?label=downloads%20last%20releases)](https://github.com/ctubio/Krypto-trading-bot)

Our bots run on unix-like systems. Persistence is achieved through a built-in server-less SQLite C++ interface.<br>Data transfers are directly done from your machine to the exchange using the latest CURL and OpenSSL versions.<br>Installation in a dedicated [Debian](https://cdimage.debian.org/cdimage/release/current/), [Raspberry](https://www.raspberrypi.com/software/), [Red Hat](https://developers.redhat.com/products/rhel/download), [CentOS](https://www.centos.org/download/) or macOS instance without Docker is recommended.

The web UI is compatible with most web browsers/resolutions, but Brave or Firefox at 1600px are recommended.<br />Doesn't require configuration of any web server (unless installed behind your own reverse proxy).

<details><summary><b>K-trading-bot</b> <sup>(web UI + CLI)</sup></summary>
to control a fully configurable high frequency trading engine, with all features suggested by the community:<br />

![trading-bot UI Preview](https://user-images.githubusercontent.com/1634027/44740469-d5c7ff00-aafa-11e8-9252-73b9c1283adb.png)
</details>

<details><summary><b>K-+portfolios</b> <sup>(web UI + CLI)</sup></summary>
to show all balances from one exchange, with buttons to create, edit or cancel orders and links to go to markets:<br />

![+portfolios UI Preview](https://github.com/user-attachments/assets/e0e3ce7d-3388-45a9-a559-4ba239a9e880)
</details>

<details><summary><b>K-hello-world</b> <sup>(CLI)</sup></summary>
to print the current value of a given currency to stdout:<br />

<pre>
 _________________________________________
/ Hello, WORLD!                           \
|                                         |
\ pssst.. 1.00000000 BTC = 56683.49 EUR.  /
 -----------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
</pre>
</details>

<details><summary><b>K-scaling-bot, K-stable--bot</b> <sup>(CLI)</sup></summary>
to easy mod and start developing a new custom bot.
</details>

### Compatible Exchanges

All currency pairs are supported (use `--list` argument to see all currently tradable pairs on a given exchange).

<table><tbody><tr><td></td><td align="center"><b>under maintenance</b></td><td colspan="2" align="center" nowrap><b>under development or abandoned</b></td></tr><tr><td align="center"><b>Spot Trading</b></td><td nowrap><a href="https://www.coinbase.com/en-es/advanced-trade">Coinbase</a> <sub>(<a href="https://help.coinbase.com/en/coinbase/trading-and-funding/advanced-trade/advanced-trade-fees">fees</a>)</sub><br> &#10239; <i>REST + 2 WebSockets</i><br><br><a href="https://www.binance.com/">Binance</a> <sub>(<a href="https://www.binance.com/en/fee/schedule">fees</a>)</sub><br><a href="https://www.binance.us/">Binance.US</a> <sub>(<a href="https://www.binance.us/fees">fees</a>)</sub><br> &#10239; <i>REST + 1 WebSocket</i><br><br><a href="https://www.bitmex.com/">BitMEX</a> <sub>(<a href="https://www.bitmex.com/wallet/fees/derivatives">fees</a>)</sub><br> &#10239; <i>REST + 1 WebSocket</i></td><td nowrap><a href="https://www.kraken.com/">Kraken</a> <sub>(<a href="https://www.kraken.com/features/fee-schedule">fees</a>)</sub><br> &#10239; <i>REST + 2 WebSockets</i><br><br><a href="https://www.kucoin.com/">KuCoin</a> <sub>(<a href="https://www.kucoin.com/vip/level">fees</a>)</sub><br> &#10239; <i>REST + 1 WebSocket</i><br><br><a href="https://www.bitfinex.com/">Bitfinex</a> <sub>(<a href="https://www.bitfinex.com/fees">fees</a>)</sub><br><a href="https://www.ethfinex.com/">Ethfinex</a> <sub>(<a href="https://www.ethfinex.com/fees">fees</a>)</sub><br> &#10239; <i>REST + 1 WebSocket</i></td><td nowrap><a href="https://www.gate.io/">Gate.io</a> <sub>(<a href="https://www.gate.io/fee">fees</a>)</sub><br> &#10239; <i>REST + 1 WebSocket</i><br><br><a href="https://hitbtc.com/">HitBTC</a> <sub>(<a href="https://hitbtc.com/fee-tier">fees</a>)</sub><br><a href="https://bequant.io/">Bequant</a> <sub>(<a href="https://bequant.io/fees-and-limits">fees</a>)</sub><br> &#10239; <i>REST + 2 WebSockets</i><br><br><a href="https://www.poloniex.com/">Poloniex</a> <sub>(<a href="https://poloniex.com/fees/">fees</a>)</sub><br> &#10239; <i>REST + 1 WebSocket</i></td></tr><tr><td align="center"><b>Margin Trading</b></td><td nowrap><i>none</i></td><td colspan="2" nowrap><i>none</i></td></tr></tbody></table>

If you ask me, [<img height="20px" src="https://github.com/user-attachments/assets/e84f2708-d29a-423d-a702-42c87a8ffe5b">](https://advanced.coinbase.com/join/KAME9XG) is the best and most secure by far, so here is my [referral link](https://advanced.coinbase.com/join/KAME9XG) for both of us to enjoy.

In case you are looking for referral links to other exchanges, feel free to post a [new issue](https://github.com/ctubio/Krypto-trading-bot/issues/new?title=Referral%20link%20for%20%5Bexchange%5D) asking to other active users.

## README
- Documentation
  - [README](#readme)
  - [MANUAL](https://github.com/ctubio/Krypto-trading-bot/blob/master/doc/MANUAL.md)
- Installation
  - [Docker Installation](#docker-installation)
  - [Windows Installation](#windows-installation)
  - [Manual GIT Installation](#manual-git-installation)
  - [Manual ZIP Installation](#manual-zip-installation)
  - [Configuration After Manual Installation](#configuration-after-manual-installation)
  - [Upgrade to the latest commit](#upgrade-to-the-latest-commit)
  - [Multiple instances party time](#multiple-instances-party-time)
- Information
  - [Compatible Exchanges](#compatible-exchanges)
  - [Application Usage](#application-usage)
  - [Web UI](#web-ui)
  - [Databases](#databases)
  - [Charts](#charts)
  - [Cloud Hosting](#cloud-hosting)
- Development
  - [Build notes](#build-notes)
  - [Changelogs](#changelog)
- Humans and Milk Mammals
  - [Unlock](#unlock)
  - [Donations](#donations)
  - [General Discussion](#general-discussion)
  - [Very Special Thanks](#very-special-thanks-to)
  - [Help](#help)
  - [Issues](#issues)

### Docker Installation

See [etc/Dockerfile](https://github.com/ctubio/Krypto-trading-bot/tree/master/etc#dockerfile) file.

### Windows Installation

Before starting with a manual installation, ensure your target machine has Windows 7 or greater and [MSYS2](https://www.msys2.org/) installed.

Use MSYS2 Terminal to install `make` (with command `pacman -S make`), then proceed as usual with the installation.

### Manual GIT Installation

0. Ensure you agree to install collaborative non-free software (see [Unlock](#unlock) section).

1. Ensure your target machine has `git` and `make` installed.

2. Download it wherever you want (feel free to customize the suggested folder name K) and execute the installer:
```
 $ git clone ssh://git@github.com/ctubio/Krypto-trading-bot K
 $ cd K
 $ make install
```

3. Open and edit the config file `K.sh` in your favorite text editor:
```
 $ vim K.sh
```

To upgrade anytime see [Upgrade to the latest commit](#upgrade-to-the-latest-commit) section.

### Manual ZIP Installation

0. Ensure you agree to install collaborative non-free software (see [Unlock](#unlock) section).

1. Ensure your target machine has `curl` and `make` installed.

2. Download it wherever you want (feel free to customize the suggested folder name K) and execute the installer:
```
 $ mkdir K
 $ cd K
 $ curl -O krypto.ninja/Makefile
 $ make install
```

3. Open and edit the config file `K.sh` in your favorite text editor:
```
 $ vim K.sh
```

To upgrade anytime to the latest release just run `make reinstall`.

### Configuration After Manual Installation

See [etc/K.sh.dist](https://github.com/ctubio/Krypto-trading-bot/blob/master/etc/K.sh.dist) file or better your own copy of `K.sh` file located in the top level path.

It just contains a few variables with examples. The very end of the file contains the code that starts the bot.

Once your config file is ready, you can execute it to start the bot:
```
 $ ./K.sh
```

Alternatively use `make start` to run `K.sh` in the background using [screen](https://kb.iu.edu/d/acuy) (to see the output, attach the screen with `make screen` [or run all at once with `make start screen`]).

Feel free to run `make stop` or `make restart` anytime, and don't forget to [read the fucking manual](https://github.com/ctubio/Krypto-trading-bot/blob/master/doc/MANUAL.md).

Troubleshooting:

 * If there is no wallet data on a given exchange, double-check the currency symbols with `--list` argument.

 Optional:

 * See at least once `./K.sh --help` to trade or `make help` to develop.

 * Use your own HTTP Basic Authentication credentials with `--user` and `--pass` arguments.

 * Use your own SSL certificate with `--ssl-crt` and `--ssl-key` arguments.<br>Otherwise, the insecure built-in certificate is fully featured, but you may need to authorise it in your browser.<br>If you want to generate your own certificate see [SSL for internal usage](https://www.akadia.com/services/ssh_test_certificate.html).<br>In case you really want to use plain HTTP, use `--without-ssl` argument.

### Upgrade to the latest commit

If you upgrade while having any instance running in the background, you will need to manually restart it using `make restart` or `make restartall` to start using the latest version.

#### Upgrade under Manual ZIP Installation:

Please run `make reinstall` to download the upgraded source and executable files.

#### Upgrade under Manual GIT Installation:

Feel free anytime to check if there are new upgrades with `make diff`.

Once you decide that it is time to upgrade, execute `make upgrade` (or directly `make reinstall` to skip the validation of new commits).

If you only use `git` to pull the latest source files from the remote branch, you will still need to upgrade or recompile your executable files.

To not upgrade but instead recompile your own modified source files, use `make lib K` or just `make` (see [Build notes](#build-notes)).

### Multiple instances party time

Please note, an "instance" is in fact a `*.sh` config file; using a single machine with a single installation, you can run as many instances as `*.sh` files you have (limited by the available free RAM).

You can list the current running instances with `make list`.

If you haven't defined a config file, `make start`, `make screen`, `make stop` and `make restart` will use the default config file `K.sh`.

To run multiple instances using a collection of config files:

1. Create a new config file with `cp etc/K.sh.dist X.sh && chmod +x X.sh` (use `X.sh` or any name but keep `.sh` extension).

2. Edit the new config file `vim X.sh`

3. Run the new instance with `./X.sh` or to run in the background, use `K=X.sh make start`. To attach to the new instance's screen, use `K=X.sh make screen`. To stop the new instance, use `K=X.sh make stop` and to restart it, use `K=X.sh make restart`. The environment variable `K` specifies the filename of the config file that you want to use.

4. Open in the web browser the different pages of the ports of the different running instances, or display the UI of all instances together in a single page using the MATRYOSHKA link in the footer (that can be predefined using the optional argument `--matryoshka=URL`).

After multiple config files are setup, to control them all together instead of one by one, the commands `make startall`, `make stopall` and `make restartall` are also available, just remember that config files with a filename starting with underscore symbol "_" will be skipped.

### Application Usage

1. Open your web browser to connect to port `3000` (or your configured port number) of the machine running K. Using `localhost` or one of the public or private IPs of your machine (if you're running on Docker, use the IP address returned by `boot2docker ip`).

2. Read up on how to use K and market making in the [manual](https://github.com/ctubio/Krypto-trading-bot/blob/master/doc/MANUAL.md).

3. Use the web UI to change the quoting parameters. Click the big "BTC/USD" button to start making markets. Click it again to stop. When the button is green, the bot is actively placing orders.

### Web UI

Once `K` is up and running, visit port `3000` (or your configured port number) to access the UI (i.e. [https://localhost:3000](https://localhost:3000)). There are inputs for quoting parameters, grids to display market orders, market trades, your trades, your order history, your positions, and a big button with the currency pair you are trading. When you're ready, click that button green to begin sending out quotes. The UI uses angularjs hydrated with websockets observed with reactivexjs.

### Databases

Each currency pair of each exchange will use a different sqlite database file with [WAL mode](https://www.sqlite.org/wal.html) enabled.

All database files are located at `/var/lib/K/db/K-*.db*`, outside the download folder to survive wild `rm -rf path/to/K` or reinstalls.

You can copy any group of `*.db*` files to another machine when migrating or as a backup.

If a database does not exist, the application will create it on boot; otherwise, it will use the existing one.

To explore each database you can use https://github.com/sqlitebrowser/sqlitebrowser or a similar tool.

To set a different database filename or to set an [in-memory database](https://sqlite.org/inmemorydb.html), use `--database=FILE` argument (see `--help`).

Even if using an in-memory database, the quoting parameters are always loaded from and saved into the file database.

### Charts

The metrics are not saved anywhere, it is just UI data collected with a visibility retention of `n` hours (where `n` is the value of `profit` quoting parameter), to display over time:

 * Market Fair Value with High and Low Prices
 * Trades Complete
 * Target Position for BTC currency (TBP)
 * Target Position for Fiat currency
 * STDEV and EWMA values for Quote Protection and APR
 * Amount available in wallet for buy
 * Amount held in open trades for buy
 * Amount available in wallet for sell
 * Amount held in open trades for sell
 * Total amount available and held at both sides in BTC currency
 * Total amount available and held at both sides in Fiat currency

### Cloud Hosting

If you ask me, [<img height="20px" src="https://user-images.githubusercontent.com/1634027/29756933-3e64c62e-8ba8-11e7-916a-3b0ae1481a52.png">](https://www.dreamhost.com/r.cgi?475987/cloud/) is a very nice web hosting company (awesome support team, awesome servers). Feel free to use this referral link to get a discount subtracted from my referral earnings (i'm a user since 2008).

### Build notes

Make sure your build machine has [node](https://nodejs.org/en/download/package-manager/) installed, also ensure `make lib` provides all dependencies without errors.

To rebuild the application, see `make help` and choose a target (just `make` may be what you are looking for).

Test units are executed before the application exits, only if the application was compiled with `KUNITS=1 make`.

Otherwise, just `make` without the environment var `KUNITS` produces an application that simply exits on exit.

A quick test runner therefore is `./K.sh --version` or the alias `make test` or all at once with `KUNITS=1 make K test`.

To pipe the output to stdout, execute the application in the foreground with `--naked` argument.

For more information consider to follow the *white rabbit*, but its dangerous to go alone, take this:

c sandbox: [wandbox.org](https://wandbox.org)

js sandbox: [jsfiddle.net](https://jsfiddle.net)

ws sandbox: [app.gosandy.io](https://app.gosandy.io/)

<details><summary><a id="changelog"><b>Release v0.7.x Changelog</b></a></summary>

Updated Coinbase integration to Advanced Trade API.

</details>

<details><summary><b>Release v0.6.x Changelog</b></summary>

Added Hello World bot, Portfolios bot, Scaling bot and Stable bot.

Added Binance, Kraken, KuCoin, Gate.io and BitMEX API.

</details>

<details><summary><b>Release v0.5.x Changelog</b></summary>

Updated exchange integrations as simple libcurl wrappers.

</details>

<details><summary><b>Release v0.4.x Changelog</b></summary>

Added main KryptoNinja class derived from all other classes and ready to be extended.

Added C++ OOP everywhere.

Added test units.

Added --interface=IP argument to bind outgoing traffic to a specific network interface.

Added Ethfinex ~~and FCoin~~ API.

Added build-in document root to stop reading files from disk.

Added build chain for win32.

~~Updated OKEx websocket to binary data.~~

Added build chain for OSX v10.13.
</details>

<details><summary><b>Release v0.3.x Changelog</b></summary>

Updated HitBTC API v2.

Added ZIP installation steps for non-git-lovers.

Added HamelinRat quoting mode and Trend safety thanks to b-seite and serzhiio contributions.

Added command-line arguments.

Updated quoting engine and gateways without nodejs.

Added Makefile to replace npm scripts.

~~Added PNG files as configuration files.~~

Added built-in C++ WWW Server to replace expressjs and socketio.

Added built-in SQLite C++ interface to replace external mongodb server.

Added Poloniex API.
</details>

<details><summary><b>Release v0.2.x Changelog</b></summary>

Updated application name to K because of Kira.

Added nodejs7, typescript2, angular4 and reactivexjs.

Added cleanup of bandwidth, source code, dependencies and installation steps.

Added many quoting parameters thanks to Camille92 genius suggestions.

Added support for multiple instances/config files with nested matryoshka UI.

Added npm scripts, david-dm, travis-ci, coveralls and codacy.

Added historical charts to replace grafana.

Added C++ math functions.

Updated OKCoin API (since https://www.okcoin.com/t-354.html).

Updated Bitfinex API v2.

Added Coinbase FIX API.

~~Added Korbit API.~~

Added new quoting styles PingPong, Boomerang, AK-47.

Added cleanup of database records, memory usage and log recording.

Added audio notices, realtime wallet display, and grafana integration.

Added https, dark theme and new UI elements.

Added a bit of love to Kira.
</details>

<details><summary><b>Release v0.1.0 Changelog</b></summary>

see the upstream project [michaelgrosner/tribeca](https://github.com/michaelgrosner/tribeca).
</details>

### Unlock

The bot is unlocked for collaborators and contributors (feel free to make acceptable Pull Requests for already opened issues or for anything you consider useful, and let me know the BTC Payment Address for the bot that you wish to unlock in the description of the PR, and I will credit it for you).

While locked, the orderbook will be in realtime 121 seconds, and later it will be updated only once every 121 seconds.

Anonymous users can also unlock any API Key by paying 0.00121000 BTC to the address displayed on exit.

Once unlocked you may use different bots or currency pairs or reinstall on a different machine with the same unlocked API Key. However, if you want to use more than one exchange, you will need to pay again to unlock the API Key for each exchange.

Otherwise if you choose to not support further development by ctubio, just keep running some old commit and do not upgrade (any commit prior to v0.3.0 was completely unlocked).

Please don't open issues asking how much % less the bot generates with `--free-version`; it is relative to your trading strategy, the market conditions, and the bot's performance.

### Donations

nope, this project doesn't have maintenance costs. but you can donate to your favorite developer today!<br>(or tomorrow!)

or see the upstream project [michaelgrosner/tribeca](https://github.com/michaelgrosner/tribeca).

or donate your time with programming or financial suggestions in the IRC channel [#krypto.ninja](https://kiwiirc.com/client/irc.libera.chat:6697/?theme=cli#krypto.ninja) at irc.libera.chat on port 6697 (SSL), or 6667 (plain); or feel free to make any question, but questions technically are not donations.

### General Discussion

[IRC](https://kiwiirc.com/client/irc.libera.chat:6697/?theme=cli#krypto.ninja) is awesome!

But if you dislike it.. consider to join the [discord server](https://discord.gg/jAX7GEzcWD). Or you can DM [ctubio on reddit](https://www.reddit.com/user/ctubio) privately.

Otherwise, here on GitHub, just create a [new discussion](https://github.com/ctubio/Krypto-trading-bot/discussions) permanently readable by everybody.

### Very Special Thanks to:

- https://github.com/michaelgrosner/tribeca (https://github.com/michaelgrosner)
- https://curl.haxx.se (https://github.com/bagder)
- https://github.com/michaelgrosner/tribeca (https://github.com/michaelgrosner)
- https://github.com/uNetworking (https://github.com/alexhultman)
- https://github.com/michaelgrosner/tribeca (https://github.com/michaelgrosner)
- https://nlohmann.github.io/json (https://github.com/nlohmann)
- https://github.com/michaelgrosner/tribeca (https://github.com/michaelgrosner)
- http://invisible-island.net
- https://github.com/michaelgrosner/tribeca (https://github.com/michaelgrosner)
- https://www.sqlite.org
- https://github.com/michaelgrosner/tribeca (https://github.com/michaelgrosner)
- but Most Special Thanks goes to [your mother](https://youtu.be/YDafHsyyTNk).

### Help

If you need installation or usage support, please create a [new discussion](https://github.com/ctubio/Krypto-trading-bot/discussions/new).

### Issues

To request new features open a [new issue](https://github.com/ctubio/Krypto-trading-bot/issues/new?title=Feature%20request) and explain your improvement as you consider.

To report errors open a [new issue](https://github.com/ctubio/Krypto-trading-bot/issues/new?title=Error%20report) only after collecting all possible relevant log messages.

Pull Requests are welcome, but adhere to the Contributor License Agreement:
- Your biological and technological distinctiveness will be added to our own. Resistance is futile.

### like yesterday, since 0day and ∞

![bcn](https://user-images.githubusercontent.com/1634027/29495722-1d924018-85c5-11e7-8d61-d83f5716ae9e.jpg)

#### every new day we sing:

<p>If love is so nice, tell me why are you so sad?<br>If love is so nice, tell me, oh tell me why are you hurt so bad?<br>One Love! get ready!</p>
<p>Now feel this drumbeat as it beats within,<br>playin' a riddim, resisting against the system:</p>

 - https://youtu.be/g--fsK6aLf8
 - https://youtu.be/BncXzyjdREc
 - https://youtu.be/uEqxj58g6To
 - https://youtu.be/SS9DJX8gTKk
 - https://youtu.be/vu6WXLQT5r8
 - https://youtu.be/e8ULyjcSukM
 - https://youtu.be/Rom4qWtEkMA
 - https://youtu.be/InNk4Z-BGc8
 - https://youtu.be/xPg_e_3cK-E
 - https://youtu.be/KKpcQIfIAi8
 - https://youtu.be/pZAmer0EmMQ
 - https://youtu.be/50aXt1ctmUU
 - https://youtu.be/vofff0Ei3kk
 - https://youtu.be/4Ois3zB7SJ4
 - https://youtu.be/_wGDcWD1E1A
 - https://youtu.be/VOgFZfRVaww
 - https://youtu.be/1iZdJNH3Z1o
 - https://youtu.be/_e5hvHL2WTg
 - https://youtu.be/jQhtEYfax5c
 - add your song here (please open a [new issue](https://github.com/ctubio/Krypto-trading-bot/issues/new?title=Today,%20I%20sing) to share your link)
<p align="center"><img src="https://user-images.githubusercontent.com/1634027/32134633-642bb47a-bbf1-11e7-809c-f2d4d57678e0.jpg" />
<br /><br />
We have already enough policemen,<br />if you like adventures choose to be a <a href="https://youtu.be/pT_GM35fM7I">brave firefighter</a>.
<br /><br /><br /><br /><br />
<img src="https://user-images.githubusercontent.com/1634027/32695988-22681724-c76b-11e7-8557-7f2b15b2686b.jpg" />
<br /><br /><br /><br />Violence <a href="https://www.cnvc.org/about/purpose-of-nvc">should not</a> be the answer to those who<br />are <a href="https://novact.org/en/">asking for</a> freedom.<br /><br /><br /><br /><br />
<img src="https://user-images.githubusercontent.com/1634027/29746351-7478d556-8ad7-11e7-8b27-445eefa8f960.jpg" />
<br /><br /><br /><br /><br />
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fctubio%2FKrypto-trading-bot%2FREADME.md&count_bg=%2379C83D&title_bg=%23555555&icon=known.svg&icon_color=%2306FF18&title=page+views&edge_flat=false"/></a></p>
