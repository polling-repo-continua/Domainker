# Domainker (Beta)
My personal bugbounty tool

# How to use
I developed this tool to be easily managed and upgraded so i created it as small plugin systems connected together

## Plugins and usage
```
lib\modules\crlf.py  : [--crlf] Check if host is vulnerable to CRLF
lib\modules\aws.py   : [--aws] Check if target is hosted on amazon (Use -x to run Auto-Takeover)
lib\modules\cname.py : [--dns] Return host cname
lib\modules\url.py   : [--url] Returs host response code
```

## Basic usage
 ```
 $ python domainker.py -d mydomains_list.txt [.. Plugins]
 $ python domainker.py -d mydomains_list.txt --url
 $ python domainker.py -d mydomains_list.txt --dns
 $ python domainker.py -d mydomains_list.txt --aws
 $ python domainker.py -d mydomains_list.txt --crlf
 ```
You could also use multiple plugins at the same time
```
$ python domainker.py -d mydomains_list.txt --url --dns --aws ...
```
## Options
```
$ python domainker --help
```
- Create output file [--output/-o file_name]
- Threads count [--threads/-t number]
- Takeover aws [--aws-takeover/-x]
- Thread timeout [--thread-timeout/-T seconds]
- Request timeout [--request-timeout/-rt seconds]


# Format 
I want add different formats at the future but currenlty this tool only support this format for the domains file
```
https://sub.domain.com  
http://sub.domain.com  
sub.domain.com  
.sub.domain.com
```
Which generated by:
- amass  
- aquatone (hosts.txt)  
- subfinder  
- sublist3r  
... and many other subdomain finders  
