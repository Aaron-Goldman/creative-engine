# Modus Create presents Creative Engine

[![Build Status](https://ci.moduscreate.com/buildStatus/icon?job=ModusCreateOrg/genus/master&build=1)](https://ci.moduscreate.com/job/ModusCreateOrg/job/genus/job/master/1/)
[![MIT Licensed](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/ModusCreateOrg/creative-engine/blob/master/LICENSE)
[![Powered by Modus_Create](https://img.shields.io/badge/powered_by-Modus_Create-blue.svg?longCache=true&style=flat&logo=data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMzIwIDMwMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8cGF0aCBkPSJNOTguODI0IDE0OS40OThjMCAxMi41Ny0yLjM1NiAyNC41ODItNi42MzcgMzUuNjM3LTQ5LjEtMjQuODEtODIuNzc1LTc1LjY5Mi04Mi43NzUtMTM0LjQ2IDAtMTcuNzgyIDMuMDkxLTM0LjgzOCA4Ljc0OS01MC42NzVhMTQ5LjUzNSAxNDkuNTM1IDAgMCAxIDQxLjEyNCAxMS4wNDYgMTA3Ljg3NyAxMDcuODc3IDAgMCAwLTcuNTIgMzkuNjI4YzAgMzYuODQyIDE4LjQyMyA2OS4zNiA0Ni41NDQgODguOTAzLjMyNiAzLjI2NS41MTUgNi41Ny41MTUgOS45MjF6TTY3LjgyIDE1LjAxOGM0OS4xIDI0LjgxMSA4Mi43NjggNzUuNzExIDgyLjc2OCAxMzQuNDggMCA4My4xNjgtNjcuNDIgMTUwLjU4OC0xNTAuNTg4IDE1MC41ODh2LTQyLjM1M2M1OS43NzggMCAxMDguMjM1LTQ4LjQ1OSAxMDguMjM1LTEwOC4yMzUgMC0zNi44NS0xOC40My02OS4zOC00Ni41NjItODguOTI3YTk5Ljk0OSA5OS45NDkgMCAwIDEtLjQ5Ny05Ljg5NyA5OC41MTIgOTguNTEyIDAgMCAxIDYuNjQ0LTM1LjY1NnptMTU1LjI5MiAxODIuNzE4YzE3LjczNyAzNS41NTggNTQuNDUgNTkuOTk3IDk2Ljg4OCA1OS45OTd2NDIuMzUzYy02MS45NTUgMC0xMTUuMTYyLTM3LjQyLTEzOC4yOC05MC44ODZhMTU4LjgxMSAxNTguODExIDAgMCAwIDQxLjM5Mi0xMS40NjR6bS0xMC4yNi02My41ODlhOTguMjMyIDk4LjIzMiAwIDAgMS00My40MjggMTQuODg5QzE2OS42NTQgNzIuMjI0IDIyNy4zOSA4Ljk1IDMwMS44NDUuMDAzYzQuNzAxIDEzLjE1MiA3LjU5MyAyNy4xNiA4LjQ1IDQxLjcxNC01MC4xMzMgNC40Ni05MC40MzMgNDMuMDgtOTcuNDQzIDkyLjQzem01NC4yNzgtNjguMTA1YzEyLjc5NC04LjEyNyAyNy41NjctMTMuNDA3IDQzLjQ1Mi0xNC45MTEtLjI0NyA4Mi45NTctNjcuNTY3IDE1MC4xMzItMTUwLjU4MiAxNTAuMTMyLTIuODQ2IDAtNS42NzMtLjA4OC04LjQ4LS4yNDNhMTU5LjM3OCAxNTkuMzc4IDAgMCAwIDguMTk4LTQyLjExOGMuMDk0IDAgLjE4Ny4wMDguMjgyLjAwOCA1NC41NTcgMCA5OS42NjUtNDAuMzczIDEwNy4xMy05Mi44Njh6IiBmaWxsPSIjRkZGIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiLz4KPC9zdmc+)](https://moduscreate.com)

This is a library of C++ classes for developing games for the ODROID-GO, the Raspberry Pi, and desktop Linux & MacOS.

The design criteria for this library/game engine are:

1. Portability. Games written using Creative Engine should easily port to other devices - it already runs on host and ODROID GO.
2. Development using [CLion](https://www.jetbrains.com/clion/) and SDL2 (CMake)
3. Run on device via Makefiles. (See [ESP32 IDF framework](https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html))
4. Support for 2D and 3D games
5. Extendable through class inheritance

## Features

1. Double-buffered LCD display driver, running at 30Hz.
2. Resource management (and resource compiler).
3. Audio driver using [LibXMP](http://xmp.sourceforge.net/).
4. Rich bitmap classes that support ROM and RAM pixel sources (resources).
5. Simple Sprites using sprite sheets.
6. Animated Sprites via animation interpreter, inherits from Simple Sprite.
7. State machines (processes) for player and enemy logic.
8. Develop on host using rich development tools, run on target with little or no effort.

# Games that use Creative Engine:

#### [Genus](https://github.com/moduscreateorg/genus)

[![./md/img/genus-gameplay.gif](./md/img/genus-gameplay.gif)](https://github.com/moduscreateorg/genus)

#### [Boing](https://github.com/moduscreateorg/boing)

[![./md/img/boing-gameplay.gif](./md/img/boing-gameplay.gif)](https://github.com/moduscreateorg/boing)

#### [Brickout](https://github.com/moduscreateorg/brickout)

[![./md/img/brickout-gameplay.gif](./md/img/brickout-gameplay.gif)](https://github.com/moduscreateorg/brickout)

## How Creative Engine works

The following visualization depicts the layers of the various libraries at play.
![genus-block-diagram](./md/img/genus-block-diagram.jpg)

#### All platforms

[Creative Engine](https://github.com/ModusCreateOrg/creative-engine) This game engine. It implements LibXMP, SDL2, ESP-IDF (Audio, Video and Input drivers).\
[LibXMP](http://xmp.sourceforge.net/) is a fantastic cross-platform library for playing music using the [Xtended Module (XM)](<https://en.wikipedia.org/wiki/XM_(file_format)>) format and also has additional functionality to play sound effects.\

[Rcomp](https://github.com/ModusCreateOrg/creative-engine/blob/master/tools/rcomp.cpp) is a CLI tool that takes any binary resources and packages (graphic, audio, etc.) them into a binary blob to be included in the game executable and is part of [Creative Engine](https://github.com/ModusCreateOrg/creative-engine).

#### macOS, Linux

[SDL2](https://www.libsdl.org/download-2) is a cross-platform low-level media layer framework. Creative Engine generates audio data with LibXMP and feeds it into the SDL2 audio runloo and does similar to present visuals in the application window as well as poll for keyboard input to allow for gameplay.

#### ODROID GO

[Espressif IoT development Framework (ESP IDF)](https://github.com/espressif/esp-idf) is a low level framework for accessing capabilities of the ESP32-WOVER SOC.

# Set up

See [our developer guide](./md/DEVELOPING.md) for instructions on getting things set up.

# Modus Create

[Modus Create](https://moduscreate.com) is a digital product consultancy. We use a distributed team of the best talent in the world to offer a full suite of digital product design-build services; ranging from consumer facing apps, to digital migration, to agile development training, and business transformation.

<a href="https://moduscreate.com/?utm_source=labs&utm_medium=github&utm_campaign=create-engine"><img src="https://res.cloudinary.com/modus-labs/image/upload/h_80/v1533109874/modus/logo-long-black.svg" height="80" alt="Modus Create"/></a>
<br />

This project is part of [Modus Labs](https://labs.moduscreate.com/?utm_source=labs&utm_medium=github&utm_campaign=create-engine).

<a href="https://labs.moduscreate.com/?utm_source=labs&utm_medium=github&utm_campaign=create-engine"><img src="https://res.cloudinary.com/modus-labs/image/upload/h_80/v1531492623/labs/logo-black.svg" height="80" alt="Modus Labs"/></a>

# License

Creative Engine is licensed under [MIT](./LICENSE) and contains a heavily modified version of [LibXMP](https://sourceforge.net/p/xmp/libxmp/ci/master/tree/README).

# Contributing

Interested in contributing to Genus? Please see our [contributions](./.github/CONTRIBUTING.md) guidelines.
