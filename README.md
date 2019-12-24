# NRF52 Toolchain

This is a toolchain for compilation of code for Nordic NRF52 microcontroller.

To build docker image for cross-compilation, use `docker build -t nrf52-toolchain:v0 .`

To use this image afterwards, use `docker run -it nrf52-toolchain:v0 /bin/bash`. All tools related to NRF52 development are stored in `/tools` folder. 

In order to assure that minimal basic toolchain works, in the running image perform the following actions:
`cd /tools/nRF5SDK160098a08e2/examples/peripheral/blinky/pca10056/blank/armgcc/ && make`. Build process should pass without errors.

## TODO:

- add cmake support
- add project structure capable of referring to the paths in the docker image, but keeping all sources under this folder
- add flashing script (likely will be used with Raspberry Pi computer)

