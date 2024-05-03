---
title: "ESP32 Wi-Fi Packets"
date: 2024-05-02T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["ESP32", "Networking", "Communication Protocols"]
author: "Mohamed Alzoubi"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: true
description: "This program can be used to see TCP, UDP, ICMP, and other incoming packets to an ESP32 board that is connected to a WiFi network."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
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
    image: "images/esp32.png" # image path/url
    alt: "ESP32" # alt text
    caption: "ESP32 with 4 LEDs: TCP (Green) | UDP (Blue) | ICMP (Red) | OTHER (Yellow)" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/Mohamed1628/ESP32-WiFi-Packets"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

This program can be used to see TCP, UDP, ICMP, and other incoming packets to an ESP32 board that is connected to a WiFi network. A different color LED is also turned on when different protocol packets are received (red for ICMP, green for TCP, blue for UDP, and yellow for others). It also outputs the source IP address of each packet. This program uses Visual Studio Code and two extensions: ESP-IDF (Espressif IoT Development Framework) and PlatformIO.

## Materials
- ESP32 DevKit V1
- 4 LEDs
- Breadboard
- 220 Ω Resistors (optional)
- Jumper Wire(s)

## Wiring
4 LEDs (Red, Green, Blue, Yellow) to represent 4 packet types (ICMP, TCP, UDP, and Other). Any GPIO pins can be used, in this case, GPIO 2, 5, 21, and 23 were used. The 220 Ω Resistors are optional.

![wiring](images/wiring.png)

---

## Software
- Virtual Studio Code
- ESP-IDF
- PlatformIO

---