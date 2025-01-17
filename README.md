# Поиск "потеряшек" в списке аниме на Anilist
## TL;DR
#### В чём проблема?
В большом списке очень тяжело проверить отсутствие продолжения каждого тайтла. 
Этот хардкодный скрипт спарсит не просмотренные продолжения и side-stories.

## Использование
Установка необходимых пакетов
`python -m venv .venv; source .venv/bin/activate; pip install gql aiohttp`
Скрипт запускается командой:
`python parse.py НИКНЕЙМ_ПОЛЬЗОВАТЕЛЯ`.

Пример: `python parse.py Rachel`. Рядом создастся файл output_Rachel.txt

## Ограничения
1) Скрипт не проходится по тайтлам рекурсивно. Поэтому, если вы посмотрели 1 из 3 сезонов, он выдаст вам лишь второй.
2) Работа не проверялась на 100% :)
3) Для 18+ тайтлов не возвращается средняя оценка.
4) Из допустимых продолжений убраны типы "MANGA", "NOVEL", "ONE_SHOT". Пример сиквела, где продолжение в виде новеллы: https://anilist.co/anime/98576/CHAOSCHILD-Silent-Sky/
