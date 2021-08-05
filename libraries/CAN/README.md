# Arduino CAN

This is a modified version of the Arduino CAN library version 0.3.1 by Sandeep Mistry <sandeep.mistry@gmail.com>. 
It has been modified to be used with the BuildRS UAC module and can be used for sending and receiving data using CAN bus.

## Compatible Hardware

* [Microchip MCP2515](http://www.microchip.com/wwwproducts/en/en010406) based BuildRS UAC board.
 
### Microchip MCP2515 wiring

| Microchip MCP2515 | Arduino |
| :---------------: | :-----: |
| VCC | 5V |
| GND | GND |
| SCK | SCK |
| SO | MISO |
| SI | MOSI |
| CS | 42 |
| INT | 36 |


`CS` and `INT` pins can be changed by using `CAN.setPins(cs, irq)`. `INT` pin is optional, it is only needed for receive callback mode. If `INT` pin is used, it **must** be interrupt capable via [`attachInterrupt(...)`](https://www.arduino.cc/en/Reference/AttachInterrupt).

**NOTE**: Logic level converters must be used for boards which operate at 3.3V.

## Installation

### Using the Arduino IDE Library Manager

1. Choose `Sketch` -> `Include Library` -> CAN
 
or simply include the API header in your sketch:
```sh
#inlcude <CAN.h>
```

## API

See [API.md](API.md).

## Examples

See [examples](examples) folder.

## License

This library is [licensed](LICENSE) under the [MIT Licence](http://en.wikipedia.org/wiki/MIT_License).
