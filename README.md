# Multi-package coverage for Golang
Coverage report script for multi-package repositories, which can be executed remotely.

If you will try to test with coverage a golang project with multiple packages in it, you will see `cannot use test profile flag with multiple packages` error. You can use this shell script to execute tests and store overall coverage output.

### Remote usage (handy for CI tasks, no configuration needed)
Execute your tests with 
```
bash <(curl -s https://raw.githubusercontent.com/Vehsamrak/go-multi-package-coverage/1.0.0/test.sh)
```

Then you can pass tests to coverage report server. For instance, to use codecove run: 
```
bash <(curl -s https://codecov.io/bash)
```


See [travis.yml](https://github.com/Vehsamrak/genetics/blob/master/.travis.yml) for example usage.

## Local usage
Clone this repository, and then run your tests with `./test.sh` instead of simple go test.
After that, coverage.txt file, which contains overall coverage data, will apear in working directory.

## Upcoming features

* Definable covermode (now it is always atomic)
* Definable coverage report file name (now it is always coverage.txt)
* Informational update message if new version released
* Forward any parameters from script arguments to go test
