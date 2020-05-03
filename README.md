# Naurok AutoSolver | FIXED
Скрипт для автоматического прохождения домашних заданий на naurok.ua. \
Демо: [Бот в Telegram](https://teleg.run/UrsulaEBot) (может поддерживать не все возможности).

## Требования
Для корректной работы желательно иметь интернет, PHP7.4+, расширение curl, openssl и json (эти расширения входят в стандартную поставку PHP). \
Также убедитесь, что php имеет доступ к папке со скриптом, так как там появится файл `urCookieXXXXXXXX`, который необходим для поддержания сессии.

## Ограничения
Пока что, этот скрипт не может проходить тесты в реальном времени. Но для домашних заданий работает!

## Использование
`php index.php -C <код учителя> --name="<имя>"`
```
Пример использования:
php index.php -T 30 -C 133712 --name="Амелия Понд" --mistakes=1

Часто используемые опции:
-C                      Код от учителя
-T                      Среднее время на ответ в секундах (по умолчанию 1)
--name                  Имя участника теста
--mistakes              Количество ошибок, которые нужно сделать (по умолчанию 0)
--quiet                 Не выводить сообщения
--vvv                   Отображать отладочные сообщения
--dont-clean            Не удалять временные файлы после завершения сессии
--override-point-count  Принудительно установить количество баллов за ответ (по умолчанию установленное автором теста значение)
```
