---
title: "CAN Communication Troubleshooter"
date: 2024-03-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["Arduino Uno", "CAN Communication", "Communication Protocols"]
categories: ["Projects"]
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
    image: "" # image path/url
    alt: "" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    # hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/Mohamed1628/CAN-Troubleshooter"
    Text: "Suggest Changes" # edit text
    appendFilePath: false # to append file path to Edit link
---

This program lets the user know if a device can properly send and recieve CAN data frames.

It does this using a CAN bus module that allows the Arduino Uno to communicate with the device over the CAN High/Low pins of the OBD port.

---

## Materials
- Arduino Uno R3
- MCP2515 CAN Bus Module
- OBDII Female Port
- Power Supplies
- Jumper Wires

## Wiring
![wiring](images/wiring.png)

Also note that, when not being programmed, the Uno is powered with an external 9V 3A power supply. Also, depending on the device you are testing, it will also need to be powered to sense that it is currently connected to something (our box). You will need an extra power supply for this. Or if you have a larger power supply you can use a simple voltage divider circuit. For example, if you have a device that normally requires 12V, then you can use one 20V power supply. The 20V would split to be 9V for the Arduino and 12V for the device. In my experience, if the device was not being powered and I sent it some frames, I would get no response back from the device. So try powering your device as well.

![example](images/example.png)
Here is an example of what I am talking about. 2 Power Supplies (or just one with a voltage divider).

![pinout](images/pinout.png)
This is the pinout for the Arduino Uno R3 board. If you would like to use a different Uno board, make sure to check your own pinout online.

---

## Software
You only need the Arduino IDE for this project.

### Source Code
See all code and setup instructions in my GitHub repository:
https://github.com/Mohamed1628/CAN-Troubleshooter

### Included Libraries
- mcp_can by coryjfowler (1.5.1 as of March 2024)
- SPI by Arduino
---