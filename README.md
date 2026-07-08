# kryyaa launcher

гуи на egui/eframe: скачивание steam игр по манифестам (zip с .lua) через DepotDownloaderMod + лаунчер 

## возможности

- **скачать** — кидаешь .zip с lua-манифестом, парсит appid/депоты/ключи, при нескольких депотах даёт выбрать нужные чекбоксами, гоняет `DepotDownloaderMod`, подменяет файлы из `gbe/` (goldberg emu и т.п.) рекурсивно по всем подпапкам
- **игры** — сканит `games/*`, тянет название и вертикальную обложку со steam cdn, находит exe и запускает
- **логи** — полный лог скачивания в реальном времени, отдельным табом
- кроссплатформенно: на windows запускает exe напрямую, на linux — через wine со своим `WINEPREFIX` на каждую игру

## сборка

```
cargo build --release
```

бинарник — `target/release/kryyaa-launcher`. рядом с ним нужны папки `win/`, `linux/`, `gbe/` (можно пустые).

## зависимости в рантайме

- linux: `wine` в PATH — для запуска windows-игр
- бинарники `DepotDownloaderMod` под нужную платформу в `win/` / `linux/`

## манифесты
можно брать из:
- https://discord.gg/dBbXAJTxH5
- https://t.me/kryyaasteambot 

онлайн/дрм фиксы:
- https://generator.ryuu.lol/fixes
