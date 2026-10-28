# TORUS Shell Browser v0.1.2

## Изменения
- Статус хранилища уточнён: оболочка опубликована в Firebase Hosting; состояние остаётся локальным для браузера.
- Кнопка проверки выполняет реальную тестовую запись/чтение/удаление отдельного ключа и не затрагивает журнал решений.
- Остальная геометрия и функциональность оболочки не изменялись.

## Установка через Termux
1. Распакуйте архив в `~/torus-shell/update/TORUS_Shell_Browser_v0.1.2/`.
2. Сделайте резервную копию: `cp ~/torus-shell/public/index.html ~/torus-shell/public/index.v0.1.1.backup.html`
3. Скопируйте новый файл: `cp ~/torus-shell/update/TORUS_Shell_Browser_v0.1.2/index.html ~/torus-shell/public/index.html`
4. Проверьте файлы и затем опубликуйте: `cd ~/torus-shell && firebase deploy --only hosting`
5. После `Deploy complete` откройте `https://torus-shell.web.app` и проверьте раздел «Хранилище и перенос».

## Ограничения интеграций
GitHub и Google Drive не подключаются этим HTML-файлом автоматически. Для агентной связи нужны отдельная авторизация и безопасный серверный/CI-процесс; секреты нельзя хранить в браузерном HTML.
