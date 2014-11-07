# XSTerminate

## The Original Bitcointalk Delete Bot

XSTerminate is a bot that can crawl new messages in your thread
and delete posts from unwelcome members.

XSTerminate is a python program with only two dependencies:
pyyaml and BeautifulSoup.

XSTerminate can run as a daemon in ``*nix`` systems or as a console
program in both Windows (NT+) and ``*nix`` systems. In ``*nix`` it
can be killed with SIGINT (ctrl-C in the console) or SIGTERM
in Windows. In such cases, it will terminate gracefully and save
cookie information.


## Donations

* BTC: 1HWu9Ant9CNmuJCG5MXi1z3F8F5Zi1o9sT
* XST: SMFPrpKYQ6yxVesVEwNfQbsPCPveG6srBP
* LTC: LZ7Rkvz5LeisP2GRmvQhUxuewe45h6tDf3
* DOGE: DLdew3KSaL9kL2cLC6Pv7hVzDULtkDcZ6



## Usage

```
xsterminate deletebot.yml
```

The file "deletebot.yml" is a yaml file with several settings.


## Configuration

* user: the bitcointalk username
* password: the bitcointalk password (remove or make null for getpass)
* topic: the bitcointalk topic number found in the topic url
* lusers: the luser blacklist with one luser name per line
* sleep: be nice to bitcointalk by sleeping between thread reloads
* cookiefile: the file wherein cookies are stored
* debug: prints debug output if set to "true";
  omit or set to false if unwanted


The settings "sleep" and "debug" can be changed in the config file
while the bot is live and the bot will adjust its behavior
upon the next reload of the thread messages.


### Example Config File: "deletebot.yml"

```
# user name at BCT
user : deletebot
# remove or make null for getpass; put in a password for auto
password : null
# BCT topic number
topic : 850210
# file with username blacklist, one per line
lusers : lusers.txt

# sleep this many seconds before reloading new messages
# can be modified while bot is live
sleep : 60

# name of the file where cookies are stored
cookiefile : cookies.lwp

# for development, this can be ommitted or set to false
# can be modified while bot is live
debug : true
```



### Example Blacklist File: "lusers.txt"

```
UnwantedUser1
UnwantedUser2
UnwantedUser3
```

