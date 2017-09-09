# Russian description

Ypload - небольшая утилита для загрузки изображений на фотохостинг [Яндекс.Фотки](https://fotki.yandex.ru/next). Написана на Go вот этим [товарищем](https://github.com/ivanzoid), за что ему спасибо.

Что было сделано мной:

* исходники собраны под Windows X64
* был найден и отредактирован скрипт, чтобы удобнее было грузить много изображений

Порядок работы:

* идём в [releases](https://github.com/silentbay/ypload/releases) и качаем архив
* распаковываем содержимое
* готовим изображения для загрузки, собираем их в одной папке
* в папку с изображениями копируем файлы утилиты: **ypload.exe start.bat**
* запускам **start.bat**
* скрипт формирует и запускает новый скрипт **ypload.bat**
* в **ypload.bat** собраны все jpg-изображения из текущей папки с командой загрузки
* перед загрузкой откроется браузер для получения токена
* изображения будут загружены в папку **Неразобранное**

Проблемы:

* бывает, что крупные изображения не загружаются, придётся за этим проследить

Послесловие.

Если кто знает, как улучшить скрипт, или сделать GUI-обвязку, или саму программу сделать удобнее, прошу, дайте [знать](https://github.com/silentbay/ypload/issues).

И ещё. Привет [яндексу](https://github.com/yandex). Спасибо, забросили свой фотохостинг. Когда будете его хоронить, не забудьте, пожалуйста, предупредить заранее (а не как с подписками). И на панихиду пригласите. Да. У меня всё.

# ypload

`ypload` is utility for uploading image files to Yandex.Fotki service.

## Usage

    ypload <imageFile>

## Installation

- If you have Go installed (install with `apt-get install golang` for Ubuntu/Debian, `brew install go` with Homebrew on OS X):
 0. Make sure you have set `GOPATH` environment variable (to some existing folder, ~/go for example)
 1. `go install github.com/ivanzoid/ypload`
 2. If your `PATH` contains `GOPATH`, then just run as `ypload ...`, otherwise run as `$GOPATH/bin/ypload ...`

- If you don't have (and/or don't want) Go installed: grab binary in releases tab.

## Author

Ivan Zezyulya, ypload@zoid.cc

## License

`ypload` is available under the MIT license. See the LICENSE file for more info.
