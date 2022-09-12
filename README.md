## ESP32-c3 Scaffold

This is a simple repo that uses the [esp-hal](https://github.com/esp-rs/esp-hal) and provides a minimal rust project setup for the ESP32-C3 RISC-V platform. Ideally you can clone this and immediately be able to upload blinky to your ESP32-C3 board. 

The scaffold uses the [espflash](https://github.com/esp-rs/espflash) utility to upload the code to the board over USB. This can be installed easily using the `cargo install espflash` command.

You will also need to install the `riscv32imc-unknown-none-elf` target for using the `rustup target add riscv32imc-unknown-none-elf` command in order to compile for the board.

From there, `cargo run` should result in the code being compiled and uploaded to the serial port that your board is connected to, and remaining connected in monitor mode. If multiple serial ports are found, espflash should ask you to select a port at upload time.
