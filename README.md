# lists
IP whitelist & blacklist operated by Mailbrix.mx

Lists are updated hourly and individual records are expired after 1 day of __inactivity__.


## whitelist

The whitelist is intended to be fed to greylisting agents in order to reduce latency,
do not assume the IP addresses in that list to be "safe" from spam:
some are safe, others are just less likely.

Applying the whitelist should reduce drastically the greylisting of legitimate hosts,
it is built from three means:

- the resolution of SPF records at major mail services providers NOT providing ESP services
- lists of legitimate senders gathered from various mailing-lists as well as trusted domains
- domain and/or IP reputation

**you can't pay your way to the whitelist, be good and you might hit the list naturally**



## blacklist

The blacklist is intended to be fed to your firewall or MTA in order to IP-block a sender.

The lists are currently generated through various means, it consists mainly of IP addresses that:

- hit mailbrix.mx operated spam traps
- send Unsolicitated Commercial Email (UCE) to adresses subscribed to specific lists
- brute-force addresses
- have a very bad domain and/or IP reputation
- were reported by a list of trusted sources

**you can't pay your way out of the blacklist, be good and you will not enter it**


## How to use

You can fetch the latest whitelist and blacklist from this repository and feed it directly in your MTA, firewall or antispam solution.
