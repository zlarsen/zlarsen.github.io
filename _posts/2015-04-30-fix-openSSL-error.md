---
layout: post
title: Fix openSSL Error
desc: Fixes OpenSSL::SSL::SSLError: SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed Error.
keywords: Zach Larsen, Zachariah Larsen, zlarsen, zlarsenz, freelance developer ruby, freelance developer, OpenSSL, Ruby, Ruby On Rails, SSLERROR, SSL_connect error
---

While developing lately in Ruby on Rails I ran into a dastardly error `OpenSSL::SSL::SSLError: SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed` Which made me go, What the Heck?! After a lot of googling, I found the best way to fix this problem, if on a mac, is to run just two simple commands.

```
curl -s http://curl.haxx.se/ca/cacert.pem > ~/.cacert.pem
echo 'export SSL_CERT_FILE="$HOME/.cacert.pem"' >> ~/.bash_profile
```

I seriously spent a LOT of time looking into this error, and hope this can help some one else fix their error a little faster than I was able to! Feel free to comment suggestions below!

{% include twitter_plug.html %}
