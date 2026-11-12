---
layout: post
title: "How I Studied for CompTIA Network+ (N10-009)"
tags: [certifications, networking, study]
---

Network+ covers a lot: the OSI model, subnetting, routing, wireless, security and
troubleshooting. These are the habits that helped me most while studying.

## Learn the exam objectives first

CompTIA publishes an objectives list for every exam. I printed it and used it as my
checklist. If a topic wasn't on the list, I didn't spend much time on it.

## Practise subnetting until it's automatic

Subnetting comes up in many questions, directly and indirectly. Practise until you can
work out the network address, broadcast address and usable host range for any
`/24` to `/30` network in under a minute.

| CIDR | Subnet mask | Usable hosts |
|---|---|---|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

## Build it in Cisco Packet Tracer

Reading about VLANs and DHCP is one thing. Configuring them and watching a PC get an
address is when it sticks. The free Cisco Networking Academy courses come with
Packet Tracer labs that line up well with the exam topics.

## Connect it to real work

Working in IT support helped a lot. When I fixed a PC with a `169.254.x.x` address,
I connected it to what I had studied about DHCP and APIPA. Questions about real faults
are much easier when you've actually seen them.

## Use practice exams to find gaps, not to memorise

After each practice test I went through **every** question I got wrong and wrote down
*why* the right answer was right. My weak areas were obvious after two or three tests,
so I spent my last weeks on those.

## What's next

I'm building on Network+ with Cisco's cybersecurity courses. I'll write about that here too.
