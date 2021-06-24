# ESPAsyncTCP

## Async TCP Library for ESP8266 N.B. THIS IS A BUGFIX VERSION OF THE ORIGINAL

---

## If you are able, please [Support me on Patreon](https://patreon.com/esparto) and/or subscribe to my [Youtube channel (instructional videos)](https://www.youtube.com/channel/UCYi-Ko76_3p9hBUtleZRY6g)

---

# Bugs fixed from the original:

1. Compilation error when setting `ASYNC_TCP_SSL_ENABLED 1` in [async_config](src/async_config.h)
2. Failure to correctly ACK "overlapped" requests, leading to a) un-ACKed messages which "pile-up" in the output buffers, usually leading to a timeout error in any caller as it waits (in vain) for the output buffer to clear, which it never will if any message is sent before the previous is ACKed

## Libraries which require this version

The author's other libraries which will either fail to compile or will misbehave badly and crash if using the unpatched original are:

1. [ESPAsyncWebserver](https://github.com/philbowles/ESPAsyncWebserver) This is a pre-requisite for the following two libraries, and also is a patched and cut-down version of the original which again had/still has numerous serious flaws
2. [PangolinMQTT](https://github.com/philbowles/PangolinMQTT)
3. [H4Plugins](https://github.com/philbowles/h4plugins)

---

# Installation

Please see [H4 Installer](https://github.com/philbowles/h4installer)
# Issues

## If you want a *quick* resolution, please follow these rules:

1. As with all H4 and H4Plugins libraries, please make sure you have read *all* the relevant documentation relating to the issue and watched any videos on the [Youtube channel (instructional videos)](https://www.youtube.com/channel/UCYi-Ko76_3p9hBUtleZRY6g). Please also subscribe to the channel for notifications of news and updates.

2. If you still think there is a problem, then join the [Facebook H4  Support / Discussion](https://www.facebook.com/groups/444344099599131/) group and report the issue briefly there. This is because I visit the group every day, whereas I do not have time to visit 11 github repos every day. Furthermore, it alerts other users to potential problems and allows an initial assessment. 

3. If there is a genuine issue then you will be referred to [Raising H4/H4Plugins issues](https://github.com/philbowles/h4plugins/blob/master/docs/issues.md) after which you are advised to create a full github issue report.

4. Failing to make an initial report in the [Facebook H4  Support / Discussion](https://www.facebook.com/groups/444344099599131/) group and simply starting with a github issue, or failing to include all of the information required in [Raising H4/H4Plugins issues](https://github.com/philbowles/h4plugins/blob/master/docs/issues.md) is likely to result in a ***long*** delay before it gets picked up.

---

(c) 2021 Phil Bowles h4plugins@gmail.com

* [Support me on Patreon](https://patreon.com/esparto)
* [Youtube channel (instructional videos)](https://www.youtube.com/channel/UCYi-Ko76_3p9hBUtleZRY6g)
* [Facebook H4  Support / Discussion](https://www.facebook.com/groups/444344099599131/)
* [Facebook General ESP8266 / ESP32](https://www.facebook.com/groups/2125820374390340/)
* [Facebook ESP8266 Programming Questions](https://www.facebook.com/groups/esp8266questions/)
* [Facebook ESP Developers (moderator)](https://www.facebook.com/groups/ESP8266/)
