---
title: "Washing Machine Status Checker"
date: 2023-11-28T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["ESP8266", "IoT", "Cloud"]
categories: ["Projects"]
author: "Mohamed Alzoubi"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: true
description: "This program uses an ESP8266 to report on the status of a washing machine using a microphone and humidity sensor."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: true
disableHLJS: false
hideSummary: false
searchHidden: false
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
    URL: "https://github.com/Mohamed1628/Washing-Machine-Status"
    Text: "Suggest Changes" # edit text
    appendFilePath: false # to append file path to Edit link
---
![esp32](images/esp32.png)

This program lets the user know:
- When a cycle finished
- When a cycle **will** finish
- When the door was opened
It does this using a microphone sensor to listen for the dinging noise at the end of a cycle as well as a humidity sensor to measure when the humidity spikes indicating that steam/vapor is coming out of a freshly opened washing machine. This of course is very simple 
---
## Materials
- ESP8266 NodeMCU ESP-12E 1.0
- Electret Microphone Amplifier MAX4466 Module
- DHT11 Temperature-Humidity Sensor Module
- Jumper Wires

## Wiring
4 LEDs (Red, Green, Blue, Yellow) to represent 4 packet types (ICMP, TCP, UDP, and Other). Any GPIO pins can be used, in this case, GPIO 2, 5, 21, and 23 were used (NodeMCU ESP-12E). The 220 Ω Resistors are optional.
![wiring](images/wiring.png)
![pinout](images/pinout.png)
This is the pinout for the ESP8266 NodeMCU ESP-12E board. If you would like to use a different ESP8266 board, make sure to check your own pinout online.
---

## Software
- Arduino Cloud
- Arduino Create Agent

### Source Code
See all code and setup instructions in my GitHub repository:
https://github.com/Mohamed1628/Washing-Machine-Status

### YouTube Demonstration + Explanation
{{< youtube "Php4FqPXtiM" >}}

---