# pio-teensy4-with-zephyr

# Uploading

While this project compiles normally, due to lack of teensy-cli/gui support in platform-nxplc, one has to do uploading manually.

After building, use `C:\Users\<user>\packages\tool-teensy\teensy-gui.exe` to upload the `.pio\build\teensy40\firmware.hex` file and reboot the MCU.

If `tool-teensy` does not exist, have PlatformIO download it by creating a dummy regular Teensy 4.0 projects using `pio init -b teensy40 && pio run -t upload` or VSCode -> New Project -> Teensy 4.0 + Arduino -> Uopload.

# UART

Although the [board docs](https://github.com/zephyrproject-rtos/zephyr/blob/main/boards/arm/teensy4/doc/index.rst#debugging) state that the UART at 
arduino pins 1 (TX) and 0 (RX) at 115200 can be used, this did not work on my hardware for me (no output). Still, the on-board LED is blinking, so 
the firmware is running..
