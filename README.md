rpi-pico-builder
==========

Build environment for Raspberry Pi Pico C/C++ SDK

## Usage

1. Clone [pico-sdk](https://github.com/raspberrypi/pico-sdk)
2. Clone [pico-examples](https://github.com/raspberrypi/pico-examples), or [set up](https://github.com/raspberrypi/pico-sdk#quick-start-your-own-project) your own project
3. ```sh
   docker run --rm -it \
    -v /path/to/your/pico-sdk:/pico-sdk \
    -v /path/to/your/pico-examples:/project \
    xingrz/rpi-pico-builder:latest \
    bash -c 'mkdir -p build && cd build && cmake .. && make blink'
   ```
4. Copy `build/blink/blink.uf2` into the RPI-RP2 drive
