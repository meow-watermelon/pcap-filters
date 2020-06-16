## capture ipv4 DNS failed responses + all queries

```
ip and port 53 and (udp[11] & 0xf != 0 or udp[10] & 0x80 = 0)
```

`udp[11] & 0xf != 0`: RCODE is not equal to 0

`udp[10] & 0x80 = 0`: QR field is 0(DNS Query)
