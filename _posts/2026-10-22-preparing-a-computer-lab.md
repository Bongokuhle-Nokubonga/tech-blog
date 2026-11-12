---
layout: post
title: "Preparing a Computer Lab for a New Semester"
tags: [labs, imaging, hardware]
---

Getting a lab of 50+ PCs ready before students arrive is about doing the same steps
the same way on every machine. This is the process I follow.

## Before you start: walk the lab

Go round with a checklist (on paper or in a spreadsheet) and note:

- missing or damaged keyboards, mice and monitors
- loose or unlabelled network cables
- PCs that won't power on or POST
- asset tag numbers, so the inventory matches what is actually on the desks

Fix the hardware first. There's no point imaging a PC with a failing disk.

## Imaging

1. **Update the master image.** Install the latest Windows updates and the software
   the lecturers asked for, check that licences are activated, then test it on one PC.
2. **Deploy to the whole lab** with your endpoint management or imaging tool.
   Network boot and multicast make this much faster than doing PCs one at a time.
3. **Check the results.** Pick a few machines at random and confirm they joined the
   domain, got the right computer name, and that every required program opens.

## Network checks

- Every PC gets a DHCP address in the correct range
- Students can log in with their domain accounts
- Printers in the lab show up and print a test page
- Internet access and any required network drives work

## Preventative maintenance

While the lab is empty:

- clean dust out of the cases and vents (heat kills hardware)
- tidy and label the cables, so a fault can be traced quickly later
- check projector bulb hours and replace any that are close to the end

## Hand-over

Update the inventory and maintenance log, and tell the lab manager about anything
still waiting on parts. The lab is ready when a student can sit at any PC,
log in, and start working without calling us.
