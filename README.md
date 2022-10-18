# STM32F4 Configuration: I2S Audio In / Out
My high resolution audio I/O configuration with STM32F4 Discovery board and Pmod I2S2 (24-bit, 96 KHz).

It uses a ping pong buffer audio stream, taking advantage of DMA in circular mode to continuously a “receive” buffer completely independent of the CPU. So the other half of the buffer is free to be processed, before being sent to the I2S peripheral data register through the transmit buffer.

More information about ping pong buffer on STM32 available [here](https://audiodsplab.wordpress.com/ping-pong-buffer-audio-stream/).

<p align=center>
  <picture>
    <img src="./Assets/doublebuffer.png" height="200"/>
  </picture>
</p>

## Hardware used

| Shop | Description |
| --- | --- |
| [STM32F411E-DISCO Evalboard](https://www.mouser.it/ProductDetail/511-STM32F411E-DISCO) | STM32F4 microcontroller (Cortex M4 MCU, 32-bit), Discovery kit |
| [Digilent Pmod I2S2](https://www.mouser.it/ProductDetail/424-410-379) | Stereo 24-bit A/D and D/A converters for I2S audio input and output |
