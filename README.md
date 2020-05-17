
# Noisy-ru
[![CircleCI](https://circleci.com/gh/1tayH/noisy/tree/master.svg?style=shield)](https://circleci.com/gh/1tayH/noisy/tree/master)

Русифицированный fork скрипта noisy

Внимание! Сейчас скрипт в начальной стадии перевода, ведётся работа! 

noisy - простой Python скрипт, который генерирует цифровой "шум" с помощью фоновых запросов к различным сервисам. Такие запросы помогают замаскировать ваши действия от провайдера среди цифрового "шума"

noisy-ru отличается наличием перевода на русский язык и наличием российских сервисов в списке тех, к которым скрипт будет обращаться для генерации "шума"

Скрипт протестирован на MacOS High Sierra, Ubuntu 16.04, Raspbian Stretch, Termux 0.94 и совместим с Python 2.7 и 3.6

## Начало работы

Эта инструкция поможет установить и запустить noisy

### Dependencies

Установите `requests` при помощи `pip`, если вы этого еще не сделали:

```
pip install requests
```

### Использование

Скопируйте репозиторий командой 
```
git clone https://github.com/Mihailovily/noisy-ru
```

Переместитесь в папку с `noisy-ru`
```
cd noisy-ru
```

Запустите скрипт 

```
python noisy.py --config config.json
```

The program can accept a number of command line arguments:
```
$ python noisy.py --help
usage: noisy.py [-h] [--log -l] --config -c [--timeout -t]

optional arguments:
  -h, --help    show this help message and exit
  --log -l      logging level
  --config -c   config file
  --timeout -t  for how long the crawler should be running, in seconds
```
only the config file argument is required.


## Сборка при помощи Docker

1. Build the image

`docker build -t noisy .`

**Or** if you'd like to build it for a **Raspberry Pi** (running Raspbian stretch):

`docker build -f Dockerfile.pi -t noisy .`

2. Create the container and run:

`docker run -it noisy --config config.json`

## Авторы

* **Itay Hury** - *Initial work* - [1tayH](https://github.com/1tayH)

See also the list of [contributors](https://github.com/1tayH/Noisy/contributors) who participated in this project.

## Лицензия

This project is licensed under the GNU GPLv3 License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

This project has been inspired by
* [RandomNoise](http://www.randomnoise.us)
* [web-traffic-generator](https://github.com/ecapuano/web-traffic-generator)