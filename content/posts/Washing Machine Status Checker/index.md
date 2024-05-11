---
title: "Washing Machine Status Checker"
date: 2024-3-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["Arduino Uno", "CAN", "Communication Protocols"]
categories: ["index"]
author: "Mohamed Alzoubi"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: true
description: "This box can be used to verify that an OBDII device can both send and recieve CAN data frames."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: true
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "cover.png" # image path/url
    alt: "Wiring" # alt text
    caption: "CAN Communication Troubleshooter" # display caption under cover
    relative: false # when using page bundles set this to true
    # hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/Mohamed1628/Washing-Machine-Status"
    Text: "Suggest Changes" # edit text
    appendFilePath: false # to append file path to Edit link
---

This program lets the user know:
- When a cycle finished
- When a cycle **will** finish
- When the door was opened

It does this using a microphone sensor to listen for the dinging noise at the end of a cycle as well as a humidity sensor to measure when the humidity spikes indicating that steam/vapor is coming out of a freshly opened washing machine. This of course is very simple 

---
## Materials
- Arduino Uno R3
- MCP2515 CAN Bus Module
- OBDII Female Port
- Power Supplies
- Jumper Wires

## Wiring
4 LEDs (Red, Green, Blue, Yellow) to represent 4 packet types (ICMP, TCP, UDP, and Other). Any GPIO pins can be used, in this case, GPIO 2, 5, 21, and 23 were used (NodeMCU ESP-12E). The 220 Ω Resistors are optional.

![wiring](images/wiring.png)

![pinout](images/pinout.png)
This is the pinout for the Arduino Uno R3 board. If you would like to use a different Uno board, make sure to check your own pinout online.

---

## Software
- Arduino IDE

### Source Code
See all code and setup instructions in my GitHub repository:
https://github.com/Mohamed1628/Washing-Machine-Status

---