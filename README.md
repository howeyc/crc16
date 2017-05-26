[![GoDoc](https://godoc.org/github.com/howeyc/crc16?status.svg)](https://godoc.org/github.com/howeyc/crc16) [![Build Status](https://secure.travis-ci.org/howeyc/crc16.png?branch=master)](http://travis-ci.org/howeyc/crc16)

# CRC16
A Go package implementing the 16-bit Cyclic Redundancy Check, or CRC-16, checksum.

## Usage
To generate the hash of a byte slice, use the [`crc16.Checksum()`](https://godoc.org/github.com/howeyc/crc16#Checksum) function:
```golang
import "github.com/howeyc/crc16"

data := byte("test")
checksum := crc16.Checksum(data, crc16.IBMTable)
```

The package provides [the following](https://godoc.org/github.com/howeyc/crc16#pkg-variables) hashing tables. For each of these tables, a shorthand can be used.
```golang
// This is the same as crc16.Checksum(data, crc16.IBMTable)
checksum := crc16.ChecksumIBM(data)
```

## Changelog
* 27.03.2017 - Added MBus checksum
* 27.05.2017 - Added checksum function without XOR
