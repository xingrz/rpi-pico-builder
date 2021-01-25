rpi-pico-builder
==========

![][docker-build] ![][docker-pulls] ![][docker-image-size]

Build environment for Raspberry Pi Pico (RP2040) C/C++ SDK

```sh
docker pull xingrz/rpi-pico-builder:latest
```

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

[docker-build]: https://shields.io/docker/cloud/build/xingrz/rpi-pico-builder?style=flat-square
[docker-pulls]: https://shields.io/docker/pulls/xingrz/rpi-pico-builder?style=flat-square
[docker-image-size]: https://shields.io/docker/image-size/xingrz/rpi-pico-builder?style=flat-square
