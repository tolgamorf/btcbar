# changelog

# 2.5.0

* #27 Remove Huobi
* #29 Add CEX.io
* #30 Fix intermittent crash
* #31 Remove Winkdex

# 2.4.0

* #17 Add Kraken ticker
* #26 Add Bittrex ticker
* #24 Remove BTCe ticker
* Fix #21 automatically reload tickers when internet is reconnected

# 2.3.1

* Fix BitFenix ticker (it was throwing 301s back to the btcbar user agent, but it's on a 60 second poll and they don't publish any rate limits...)

# 2.3.0

* Fix #15 text cut off on launch
* Fix #14 setting update frequency to 60 seconds (from 10 seconds)
* Fix #13 Huobi ticker error **Note:** Strict TLS 1.2 checks had to be disabled for the Huobi domain due to their insecure HTTPS certificate. It was only using HTTP until this release, so this is unfortunate but is not a regression.
* Use the new Huobi and OKCoin USD tickers rather than CNY price **Note:** Apologies to anyone this inconveniences. Also, this change will reset your default ticker.
* Tickers are now sorted alphabetically

TODO:

* Implement multiple currency pair support on tickers in the near future to support switching between currencies.
* Make ticker loading and default ticker handling more robust so they can be swapped out or plugged in easier.
* Implement self-updates from within the app
* Figure out an appropriate OSS license

# 2.2.1

* Fix bug where icon disappears on error

# 2.2.0

* Adds BitFinexUSD, WinkDexUSD, HuobiCNY and OKCoinCNY
* New status bar icon with Yosemite (dark theme) support

# 2.1.4

* Removes MtGox

# 2.1.3

* Fixes issue where the local currency code was displayed instead of the USD symbol
* Improves error handling: if there is an error, the icon will fade and a descriptive error will be displayed in the tooltip when hovering over btcbar rather than taking up space in your menu bar

# 2.1.2

* Uses new HTTPS MtGox API to fix "json error"
* Better organization for repo and XCode project
* Standardizes use of commas in tickers

# 2.1.1

* Enables live prices in menu
* Fixes a minor bug in the ticker switching code

# 2.1.0

* New BTCe/USD ticker
* Manually refreshes when a ticker is clicked
* Decreases disk io/cpu time/power usage
* Greatly increases modularity (tickers now have a protocol, menu is dynamically generated)

# 2.0.0

* Adds Bitstamp and Coinbase, and a little better backend abstraction so it will be easier to add future tickers.

TODO:

* Live updating prices for each menu item in the dropdown
* More robust abstraction of tickers/dynamic menu

# 1.0.0

* The first release, which uses MtGox's USD ticker API.
