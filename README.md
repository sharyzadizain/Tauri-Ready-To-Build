# AI-Boris (Tauri + Vite + TypeScript + iOS)

## Стек:
Node.js 20+ и npm
Rust (stable toolchain)
Xcode (последняя версия)
Xcode Command Line Tools
iOS Simulator или iPhone (с включённым Developer Mode)
Tauri CLI

## Установка зависимостей

```bash
npm install
```

## Быстрый запуск (iOS, dev режим)

```bash
npm run tauri ios dev
```


## Запуск через Xcode (рекомендуется при ошибках)

Открыть проект:

```bash
open src-tauri/gen/apple/tauri-app.xcodeproj
```

Дальше:

1. Выбрать устройство (Simulator или iPhone)
2. Нажать  **Run**

## Signing (обязательно для iPhone)

В Xcode:
1. Target → `tauri-app_iOS`
2. Вкладка **Signing & Capabilities**
3. Включить: Automatically manage signing
4. Выбрать Team (Apple ID)

## Bundle Identifier
Установить уникальный:
```
com.yourname.aiboris
```

## Собрать iOS приложение (release)
```bash
npm run tauri ios build
```

## Установка на iPhone (через Xcode)

1. Подключить iPhone
2. Выбрать его в Xcode
3. Нажать  Run
4. На устройстве:Settings → Privacy & Security → Developer Mode → включить
5. Доверить сертификат

## IPA файл (ручная установка)
После сборки:

```
src-tauri/gen/apple/build/Release-iphoneos/
```

Дальше можно:
1. установить через Xcode
2. или через сторонние инструменты (AltStore, etc.)

