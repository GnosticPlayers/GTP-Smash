[![license](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/opensecs/GTP-Smash/blob/master/LICENSE)
[![version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/opensecs/GTP-Smash)
[![language](https://img.shields.io/badge/language-Python3-red.svg)](https://www.python.org/download/releases/3.0/)

__DISCLAIMER__: This project should be used for authorized testing and educational purposes only.

# GTP Smash
A DDoS tool that uses unsecured GPRS servers via AMP attacks.


## Pre-Requirements

* Python3
* Shodan API Key
* Shodan ```sudo python3-pip install shodan```
* Scrapy ``sudo python3-pip install scrapy```

## Download

```
git clone https://github.com/GnosticPlayers/GTP-Smash
```

## PoC - Point Of Concept

![alt text](https://i.gyazo.com/0ebba1050055005edeb64e9249b0c075.png "Explaining vulnerabilities with GPRS / GTP")

Date: 07/05/19

This exploit works in one possible way. Unsecured GPRS servers are found via Shodan's IoT Search engine, they are using ASCII embedded binary commands, which are easily controllable through a basic Python3 file. In one instance, I found 650K+ affected servers, which all use the same ASCII encoded binary strings. 
This exploit works in the same way as the Memcrashed DDoS Exploit from 2017-2018. It's working just the same, a part from the fact that all servers and ports are different. It's also worth noting that the total power has been mesured through a live DStat terminal at around 1.52tbps. This is not a Botnet! It's a amplification DDoS exploit...

However, as these servers are mostly all in China and they will be used to support the speeds required for the future technology 5G, I'd like to give a bit more information:
```
3G has a total of 40mbps
4G has a total of 50mbps
```
It's been said that 5G will have 20 x the speed of 4G.
So, let's work out the maths:
```
50 * 20 = 1000 or 1Gbps
1 server has 1gbs. I have amassed a total of 652,000 bots. Each of these has the max capacity of 1Gbps. 
652,000 * 1 = 652000 or 652Tbps!
```
If 5G does end up using all these servers, then you can now see why this is an issue!

On the same note, my friend (who's also helping me with this) has access to my tool, he's using a different port but the same Shodan dork as me. He has 287K+ bots. If we work together or add more functions to the tool to allow different ports to be controlled, then we'll have a total bot number of ```939,000+``` or ```0.939Pbps```

Update: 25/05/19

Recently, 5G in the UK was announced to have a max speed of 10GBPS, which is far better than our 1GPBS. However, this now means that our initial number (939tbps) must now be timed 10!.

This is equal to 1/PBPS or (1.042499 pbps!). This means that nothing can survive / mitigrate against this.

Update: 01/06/19 

As of today, I tested out the tool early in the morning, later on during the day, I've had issues with internet access to the application websites and applications I targetted. Example service that was hit:
* Snapchat (I've had issues all day with this)

Update: 18/07/19

I've finally finished the project. This includes all python sources files, features and additions that I wanted to include. However, I will NOT be uploading it here, as Github will just flock to this and it'll get overused into the ground. If you want access, please email me. <3

Update: 27/04/2021

Just finished adding the anomitiy module. Tested around 400K bots on paypal.com. It seems to be struggling

Update: 05/05/2021

Upon further research into this project, I can now see that with the use of IoT search engines, such as Censys, Zoomeye & Shodan, threat actors or APTs can download & parse millions of GPRS-tunneling-protocol-based IPs & subsequently attack them all, for a selected area, albeit a town or a city, or even a country, and remove all connection to the outside world via 3G/4G/5G networks. In short, anyone can use a botnet or something similar to attack these IPs en-mass, which can shut down communications for a country or a city. 

The United Kingdom, for instance, only has around 700 GPRS servers, which are all suseptable to denial of service attacks.
# Author

Rest In Peace to the original developer, whom has sadly passed away.
This account will now be maintained by an IRL/close friend.

__Email__: dreammarket@riseup.net
__Twitter__: [![twitter](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/GnosticPlayers)
