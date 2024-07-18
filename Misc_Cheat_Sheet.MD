# Ffuf - Cheat Sheet

## General Commands

```sh
echo STRING | Base64 

```
*Description:* Base64 encode

```sh
echo ENCODED_B64 | base64 -d 
```
*Description:* Base64 decode

```sh
echo hackthebox | xxd -p
```
*Description:* Hex encode

```sh
echo hackthebox | xxd -p -r
```
*Description:* Hex decode

```sh
echo STRING | tr 'A-Za-z' 'N-ZA-Mn-za-m' 
```
*Description:* ROT13 encode

```sh
echo STRING | tr 'A-Za-z' 'N-ZA-Mn-za-m' 
```
*Description:* ROT13 encode

```sh
echo ENCODED_ROT13 | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
*Description:* ROT13 decode

### Useful Websites

[JsConsole](https://jsconsole.com/)
*Description:* JavaScript Console

[Js Prettier](https://prettier.io/playground/)
*Description:* JavaScript Deobfuscator/Beautifyer

[Js Beautifier](https://beautifier.io/)
[Js Beautifier](http://www.jsnice.org/)
*Description:* JavaScript Beautifier


