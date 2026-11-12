---
layout: post
title: "\"No Internet\": My Step-by-Step Network Troubleshooting Checklist"
tags: [networking, troubleshooting]
---

"The internet is down" is the ticket I see most often. It can mean almost anything:
a loose cable, a bad DHCP lease, a DNS problem or a dead switch. Guessing wastes time,
so I work from the bottom of the network up, following the OSI model, Layer 1 first.

## 1. Is it one PC or many?

This one question saves the most time.

- **One PC**: the problem is almost always that machine, its cable or its wall port.
- **A whole lab or floor**: look at the switch, uplink, DHCP server or firewall.

## 2. Physical layer: lights and cables

- Is the cable plugged in at **both** ends (PC and wall port)?
- Is the link light on the network card lit? No light means no physical link.
- Try a known-good cable and a different wall port.
- For a whole lab, check that the access switch is powered and its uplink port is lit.

## 3. Does the PC have a valid IP address?

```cmd
ipconfig /all
```

| What you see | What it usually means |
|---|---|
| `169.254.x.x` | No reply from DHCP (APIPA address). Check cabling, VLAN or the DHCP scope |
| Correct range but no gateway | Wrong static config or a bad DHCP option |
| Looks normal | Move on to step 4 |

To ask DHCP for a fresh lease:

```cmd
ipconfig /release
ipconfig /renew
```

## 4. Can I reach the gateway, and then beyond it?

```cmd
ping <default-gateway>
ping 8.8.8.8
```

- Gateway fails: it's a local problem (VLAN, switch port, firewall on the PC).
- Gateway works but `8.8.8.8` fails: the problem is upstream (router, ISP, firewall).
- Both work: the network is fine, so it's probably DNS.

## 5. Is it DNS?

```cmd
nslookup google.com
ipconfig /flushdns
```

If pinging an IP address works but pinging a name doesn't, it's DNS. Check which DNS
servers the PC is using in `ipconfig /all`.

## 6. Write it down

When it's fixed, I note the cause, the fix and how long it took in the ticket.
The next time the same lab goes down, whoever picks up the ticket starts at the answer
instead of at step 1.

> **Tip:** Change one thing at a time and test after each change. If you change three
> things at once, you won't know which one fixed it.
