# PineCone BL602 talks SPI too!

📝 _10 Feb 2021_

Here's the source code for BL602 accessing BME280 over SPI: [`sdk_app_spi/demo.c`](https://github.com/lupyuen/bl_iot_sdk/blob/spi/customer_app/sdk_app_spi/sdk_app_spi/demo.c)

In this article we'll study the source code and look into these issues with BL602 SPI...

1.  The pins for __Serial Data In__ and __Serial Data Out__ seem to be flipped, when observed with a Logic Analyser. 

    This contradicts the BL602 Reference Manual.

1.  To talk to BME280, we must configure BL602 for __SPI Polarity 0, Phase 1__.

    Though the Logic Analyser shows that it looks like SPI Phase 0.

1.  BL602's __SPI Chip Select Pin__ doesn't work with BME280's SPI protocol.

    We'll control the SPI Chip Select Pin ourselves.

1.  Setting __Serial Data Out to Pin 0__ will switch on the WiFi LED.

    We'll switch to a different pin for Serial Data Out.

Also we'll learn to __troubleshoot BL602 SPI with a Logic Analyser__.

![PineCone BL602 RISC-V Evaluation Board connected to BME280 SPI Sensor](https://lupyuen.github.io/images/spi-title.jpg)

# What's Next

TODO

-   [Sponsor me a coffee](https://github.com/sponsors/lupyuen)

-   [Check out my articles](https://lupyuen.github.io)

-   [RSS Feed](https://lupyuen.github.io/rss.xml)

_Got a question, comment or suggestion? Create an Issue or submit a Pull Request here..._

[`lupyuen.github.io/src/spi.md`](https://github.com/lupyuen/lupyuen.github.io/blob/master/src/spi.md)