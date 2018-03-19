# Multi-package coverage for Golang
Coverage report script for multi-package repositories

If you will try to test with coverage a golang project with multiple packages in it, you will see `cannot use test profile flag with multiple packages` error. You can use this shell script to execute tests and store overall coverage output.

## Usage
Execute `bash <(curl -s https://raw.githubusercontent.com/Vehsamrak/go-multi-package-coverage/1.0.0/test.sh)`

After that, coverage.txt file, which contains overall coverage data, will apear in working directory.

## Upcoming features

* Definable covermode (now it is always atomic)
* Definable coverage report file name (now it is always coverage.txt)
* Update info if new version released
