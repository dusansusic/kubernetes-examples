

# Examples:

## busybox
* Create busybox pod:

``dusansusic@syslog:/home/dusansusic/kubes# kubectl create -f busybox.yaml``

* Execute command using recently created pod:

``dusansusic@syslog:/home/dusansusic/kubes# kubectl exec busybox ping 8.8.8.8``

```
PING 8.8.8.8 (8.8.8.8): 56 data bytes
64 bytes from 8.8.8.8: seq=0 ttl=50 time=1.655 ms
64 bytes from 8.8.8.8: seq=1 ttl=50 time=1.494 ms
64 bytes from 8.8.8.8: seq=2 ttl=50 time=1.655 ms
```

``dusansusic@syslog:/home/dusansusic/kubes# kubectl exec busybox nslookup google.com 8.8.8.8``

```
Server:    8.8.8.8
Address 1: 8.8.8.8 google-public-dns-a.google.com

Name:      google.com
Address 1: 2a00:1450:400b:801::200e dub08s01-in-x0e.1e100.net
Address 2: 216.58.198.78 dub08s02-in-f14.1e100.net```
