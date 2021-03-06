# ReFlashIG
![alt text](https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/reflash.PNG)
Instagram Password Cracker

### Donate
  - Bitcoin: 1DGyJxWY4AWCbjMQptc3fSkdnf4e71BCX9
  - Ethereum: 0x019e2AC0ffEFD6eC62b464487d2434bc57C6F9ae

### Features
* Imports and uses proxies(keeps you off of Instagram's blacklist)
* Imports passwords
* Sorts and cleans proxies and passwords
* Provides after-action reports
* Notifies on "Suspicious Login Attempt Flags"
* Apply custom timeout values
* Multi-Threaded cracking
* Run with switches or open menu

### Requirements(for use on the Linux operating system)
* Python 2.7
* Basic knowledge of the Linux command line
* Connection to the internet

### Setup

Download: `wget "https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/ReFlashIG.py" -O ReFlashIG.py`  

Copy your password list into the same directory as `ReFlashIG.py`  
If you already have your own list of proxies, make sure that is also in the same directory
##### Optional(if you don't already have your own proxies)
Download: `wget "https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/get_proxies.py" -O get_proxies.py`  
Download: `wget "https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/test_proxies.py" -O test_proxies.py`

### Usage

##### Setting up a proxy list
**1.** Run: `python get_proxies.py output.txt 10`  
 * This will save a list of 200 proxies to `output.txt`  
 ![alt text](https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/screen_get.JPG)

**2.** Run: `python test_proxies.py -x output.txt -o proxies.txt -t 5`
 * This will take the list of proxies from `output.txt` and save the proxies that beat a timeout of 5 seconds to `proxies.txt`
 * Check your list of proxies. If you want more, repeat steps **1** and **2**
 ![alt text](https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/screen_test_1.JPG)  
 ![alt text](https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/screen_test_2.JPG)
 
 
##### Running ReFlashIG.py using swtich options
```

╔════════ ReFlashIG ════════╗
║ ╦═╗┌─┐╔═╗┬  ┌─┐┌─┐┬ ┬╦╔═╗ ║
║ ╠╦╝├┤ ╠╣ │  ├─┤└─┐├─┤║║ ╦ ║
║ ╩╚═└─┘╚  ┴─┘┴ ┴└─┘┴ ┴╩╚═╝ ║
╚═══════════════════════════╝

 Developed By: @the.red.team2

Usage: ReFlashIG.py [-i] [-m] [-v] [-c <thread count>] -u <username> -p <password file> -x <proxy file> -t <timeout>

Options:
  -h, --help        show this help message and exit
  -u USERNAME       Instagram username to target
  -p PASSWORD_FILE  File containing list of passwords
  -x PROXY          File containing list of proxies
  -t TIMEOUT        Instagram connection timeout
  -c THREAD_COUNT   Thread count
  -v                Verbose output
  -m                Open interactive menu
  -i                Information page
```
  
Example: `python ReFlash.py -u the.red.team2 -p passwords.txt -x proxies.txt -t 5 -v`  
![alt text](https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/screen_run_1.JPG)  
![alt text](https://raw.githubusercontent.com/the-red-team/ReFlashIG/master/screen_run_2.JPG)


##### Running ReFlashIG.py using the walk-through method

Run: `python ReFlash.py -m`
 * This will walk you through a step-by-step process to run a password cracking session.


