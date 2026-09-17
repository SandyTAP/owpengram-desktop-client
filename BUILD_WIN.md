# Сборка OwpenGram на Windows

## Требования
- Visual Studio 2022 (C++ x64)
- Python 3.10
- Git

## Сборка

```bat
build-windows.bat
```

Скрипт спросит API-ключи, подтянет подмодули и соберёт проект.

## Вручную

```bat
git submodule update --init --recursive
cd Telegram
cmake -B build -G "Visual Studio 17 2022" -A x64
cmake --build build --config Debug --target Telegram
```

Готовый exe: `build/Debug/Telegram.exe`
