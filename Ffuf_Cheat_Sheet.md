
# Ffuf - Cheat Sheet

## Ffuf Commands

### General Commands

```sh
ffuf -h
```
*Description:* ffuf help

### Directory Fuzzing

```sh
ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/FUZZ
```
*Description:* Directory Fuzzing

### Extension Fuzzing

```sh
ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/indexFUZZ
```
*Description:* Extension Fuzzing

### Page Fuzzing

```sh
ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/blog/FUZZ.php
```
*Description:* Page Fuzzing

### Recursive Fuzzing

```sh
ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/FUZZ -recursion -recursion-depth 1 -e .php -v
```
*Description:* Recursive Fuzzing

### Sub-domain Fuzzing

```sh
ffuf -w wordlist.txt:FUZZ -u https://FUZZ.hackthebox.eu/
```
*Description:* Sub-domain Fuzzing

### VHost Fuzzing

```sh
ffuf -w wordlist.txt:FUZZ -u http://academy.htb:PORT/ -H 'Host: FUZZ.academy.htb' -fs xxx
```
*Description:* VHost Fuzzing

### Parameter Fuzzing - GET

```sh
ffuf -w wordlist.txt:FUZZ -u http://admin.academy.htb:PORT/admin/admin.php?FUZZ=key -fs xxx
```
*Description:* Parameter Fuzzing - GET

### Parameter Fuzzing - POST

```sh
ffuf -w wordlist.txt:FUZZ -u http://admin.academy.htb:PORT/admin/admin.php -X POST -d 'FUZZ=key' -H 'Content-Type: application/x-www-form-urlencoded' -fs xxx
```
*Description:* Parameter Fuzzing - POST

### Value Fuzzing

```sh
ffuf -w ids.txt:FUZZ -u http://admin.academy.htb:PORT/admin/admin.php -X POST -d 'id=FUZZ' -H 'Content-Type: application/x-www-form-urlencoded' -fs xxx
```
*Description:* Value Fuzzing

## Wordlists

### Directory/Page Wordlist

```sh
/opt/useful/SecLists/Discovery/Web-Content/directory-list-2.3-small.txt
```
*Description:* Directory/Page Wordlist

### Extensions Wordlist

```sh
/opt/useful/SecLists/Discovery/Web-Content/web-extensions.txt
```
*Description:* Extensions Wordlist

### Domain Wordlist

```sh
/opt/useful/SecLists/Discovery/DNS/subdomains-top1million-5000.txt
```
*Description:* Domain Wordlist

### Parameters Wordlist

```sh
/opt/useful/SecLists/Discovery/Web-Content/burp-parameter-names.txt
```
*Description:* Parameters Wordlist

## Misc

### Add DNS Entry

```sh
sudo sh -c 'echo "SERVER_IP academy.htb" >> /etc/hosts'
```
*Description:* Add DNS entry

### Create Sequence Wordlist

```sh
for i in $(seq 1 1000); do echo $i >> ids.txt; done
```
*Description:* Create Sequence Wordlist

### Curl with POST

```sh
curl http://admin.academy.htb:PORT/admin/admin.php -X POST -d 'id=key' -H 'Content-Type: application/x-www-form-urlencoded'
```
*Description:* Curl with POST
