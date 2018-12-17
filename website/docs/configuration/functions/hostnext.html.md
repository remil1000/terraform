---
layout: "functions"
page_title: "hostnext function"
sidebar_current: "docs-funcs-ipnet-cidrhost"
description: |-
  Takes a host IP address in CIDR notation and return the `hostcidr` +
  `nextnum` IP address.
---

# `hostnext` Function

`hostnext` takes a host IP address in CIDR notation (like `10.0.10.10/16`) and
return the `hostcidr` + `nextnum` IP address

```hcl
hostnext(hostcidr, nextnum)
```

`prefix` the host address, must be given in CIDR notation, as defined in
[RFC 4632 section 3.1](https://tools.ietf.org/html/rfc4632#section-3.1).

`hostnum` is a whole number

## Examples

```
> hostnext("10.0.10.10/16", 8) 
  returns: "10.0.10.18"

> hostnext("2607:f298:6051:516c::/64", 31)
  returns: "2607:f298:6051:516c::1f"
```
