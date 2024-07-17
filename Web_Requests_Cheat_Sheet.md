
# Web Requests Module - Cheat Sheet

## cURL Commands

### General Commands

```sh
curl -h
```
*Description:* cURL help menu

```sh
curl inlanefreight.com
```
*Description:* Basic GET request

```sh
curl -s -O inlanefreight.com/index.html
```
*Description:* Download file

```sh
curl -k https://inlanefreight.com
```
*Description:* Skip HTTPS (SSL) certificate validation

```sh
curl inlanefreight.com -v
```
*Description:* Print full HTTP request/response details

```sh
curl -I https://www.inlanefreight.com
```
*Description:* Send HEAD request (only prints response headers)

```sh
curl -i https://www.inlanefreight.com
```
*Description:* Print response headers and response body

```sh
curl https://www.inlanefreight.com -A 'Mozilla/5.0'
```
*Description:* Set User-Agent header

```sh
curl -u admin:admin http://<SERVER_IP>:<PORT>/
```
*Description:* Set HTTP basic authorization credentials

```sh
curl http://admin:admin@<SERVER_IP>:<PORT>/
```
*Description:* Pass HTTP basic authorization credentials in the URL

### Set Request Header

```sh
curl -H 'Authorization: Basic YWRtaW46YWRtaW4=' http://<SERVER_IP>:<PORT>/
```
*Description:* Set request header

### Pass GET Parameters

```sh
curl 'http://<SERVER_IP>:<PORT>/search.php?search=le'
```
*Description:* Pass GET parameters

### Send POST Request with POST Data

```sh
curl -X POST -d 'username=admin&password=admin' http://<SERVER_IP>:<PORT>/
```
*Description:* Send POST request with POST data

### Set Request Cookies

```sh
curl -b 'PHPSESSID=c1nsa6op7vtk7kdis7bcnbadf1' http://<SERVER_IP>:<PORT>/
```
*Description:* Set request cookies

### Send POST Request with JSON Data

```sh
curl -X POST -d '{"search":"london"}' -H 'Content-Type: application/json' http://<SERVER_IP>:<PORT>/search.php
```
*Description:* Send POST request with JSON data

## APIs

### Read Entry

```sh
curl http://<SERVER_IP>:<PORT>/api.php/city/london
```
*Description:* Read entry

### Read All Entries

```sh
curl -s http://<SERVER_IP>:<PORT>/api.php/city/ | jq
```
*Description:* Read all entries

### Create (Add) Entry

```sh
curl -X POST http://<SERVER_IP>:<PORT>/api.php/city/ -d '{"city_name":"HTB_City", "country_name":"HTB"}' -H 'Content-Type: application/json'
```
*Description:* Create (add) entry

### Update (Modify) Entry

```sh
curl -X PUT http://<SERVER_IP>:<PORT>/api.php/city/london -d '{"city_name":"New_HTB_City", "country_name":"HTB"}' -H 'Content-Type: application/json'
```
*Description:* Update (modify) entry

### Delete Entry

```sh
curl -X DELETE http://<SERVER_IP>:<PORT>/api.php/city/New_HTB_City
```
*Description:* Delete entry

## Browser DevTools

### Shortcuts

```sh
[CTRL+SHIFT+I] or [F12]
```
*Description:* Show devtools

```sh
[CTRL+SHIFT+E]
```
*Description:* Show Network tab

```sh
[CTRL+SHIFT+K]
```
*Description:* Show Console tab
