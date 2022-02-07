# Setup

```
brew tap osx-cross/avr
brew install avr-gcc
brew install avrdude
```

use nightly:
`rustup override set nightly-2021-01-07`

build:
`cargo build`

navigate to target:
eg. `cd target/avr-atmega328p/debug`

flash: 
```
avrdude -p m328p -c arduino -P /dev/tty.usbserial-14440 -b 115200 -U  flash:w:rust-arduino-blink.elf
```
my serial connection was on: `/dev/tty.usbserial-14440`, check connection.