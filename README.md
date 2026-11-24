# BeatMorph — VST3 мультиэффектор (стиль Gross Beat)

Автор: Jetty Gas  |  Telegram: https://t.me/jetty808gas  |  плагин абсолютно бесплатный.

Интерфейс как у дорогого аппаратного процессора (графитовая шлифованная панель, ореховые боковины, латунная табличка,
алюминиевые ручки с накаткой, LCD, VU-метры, катушки, 7-сегментные индикаторы).
Девять модулей-вкладок: Rhythm, Slicer, Granular, Spectral (17 режимов), Distortion, Filter, Ring Mod, Delay, Reverb,
плюс вкладка LFO: 4 LFO, каждый можно привязать к любому числу параметров (правый клик по любой ручке).
Браузер пресетов (папки, v2, User), сохранение своих пресетов в папку User, страница About.
Кнопки BYPASS, PANIC, RANDOM; замочки на Mix и Out фиксируют значение при смене пресетов.
399 фабричных пресетов в 15 категориях (папка v2 — 162 новых).
Латентность плагина 1024 сэмпла (спектральный модуль) — хост компенсирует её автоматически.

Пользовательские пресеты хранятся в:
- Windows: %APPDATA%\BeatMorph\User
- macOS: ~/Library/Application Support/BeatMorph/User
- Linux: ~/.config/BeatMorph/User

## Получить готовый .vst3 без установки компиляторов (GitHub Actions)
1. Создайте пустой репозиторий на github.com и загрузите в него содержимое этой папки
   (вместе со скрытой папкой `.github`).
2. Вкладка **Actions** -> дождитесь зелёной галочки (5–15 минут).
3. Откройте последний запуск -> раздел **Artifacts** -> скачайте
   `BeatMorph-VST3-windows-latest` (или macOS / Linux).

## Установка
- Windows: папку `BeatMorph.vst3` -> `C:\Program Files\Common Files\VST3\`
- macOS: `BeatMorph.vst3` -> `~/Library/Audio/Plug-Ins/VST3/` (может понадобиться
  `xattr -cr BeatMorph.vst3` и ad-hoc подпись: `codesign --force --deep -s - BeatMorph.vst3`)
- Linux: `~/.vst3/`
Затем пересканируйте плагины в DAW.

## Локальная сборка
    cmake -B build -DCMAKE_BUILD_TYPE=Release
    cmake --build build --config Release
