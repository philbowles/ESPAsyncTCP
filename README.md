# ESPAsyncTCP

## N.B. THIS IS A BUGFIX VERSION OF THE ORIGINAL

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

## Find me daily in these FB groups

* [Pangolin Support](https://www.facebook.com/groups/pangolinmqtt/)
* [ESP8266 & ESP32 Microcontrollers](https://www.facebook.com/groups/2125820374390340/)
* [ESP Developers](https://www.facebook.com/groups/ESP8266/)
* [H4/Plugins support](https://www.facebook.com/groups/h4plugins)

I am always grateful for any $upport on [Patreon](https://www.patreon.com/esparto) :)

(C) 2021 Phil Bowles