# CORS


## Introduction

Same-Origin policy is a fundamental security concept allowing sites to prevent malicious scripts from reading data from different servers/domain. 

CORS stands for Cross-Origin Resource Sharing. 

It is a standard for accessing web resources on different domains. It enables browsers to access resouces from other-than-originating domains easily and seamlessly. It becomes quite useful for integrating web services as they may come from multiple (sub) domains to a browser.

---

## Understanding HTTP headers

Following are the http headers you will see when you make a request by typing the URL in the browser address-bar:

```
Accept-Language [en-GB,en-US;q=0.9,en;q=0.8]
Cookie [mysession_cookie_name=8b7d0ca4-2cdb-4d54-bbd0-2f7b2286bddf]
Connection [keep-alive]
Upgrade-Insecure-Requests [1]
Accept [text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8]
User-Agent [Mozilla/5.0 (Macintosh; Intel Mac OS X 10_12_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/62.0.3202.97 Safari/537.36 Vivaldi/1.94.1008.32]
Accept-Encoding [gzip, deflate, br]
```


Now we make the same request using ajax:

```
Connection [keep-alive]
Accept [*/*]
Origin [http://localhost:8000]
User-Agent [Mozilla/5.0 (Macintosh; Intel Mac OS X 10_12_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/62.0.3202.97 Safari/537.36 Vivaldi/1.94.1008.32]
Accept-Language [en-GB,en-US;q=0.9,en;q=0.8]
Pragma [no-cache]
Cache-Control [no-cache]
Referer [http://localhost:8000/]
Accept-Encoding [gzip, deflate, br]
```

Note that an extra http header named “Origin” is sent to the server while making ajax requests.
