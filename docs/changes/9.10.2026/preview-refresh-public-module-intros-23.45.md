# Change Log — Повторная публикация публичных разделов LifeGame — Version 1.0

- **Дата:** 09.10.2026
- **Время:** 23:45 MSK (UTC+03:00)
- **Цель:** опубликовать актуальный коммит ветки `feature/pwa-static-cache` в изолированной тестовой среде.
- **Статус:** DEPLOY TRIGGERED — результат GitHub Actions требует проверки.

## Причина

Изменение публичных представлений Health и Development находится в исходной ветке LifeGame, но тестовая публикация запускается только при изменении `main` репозитория Test-web. Предыдущая публикация предшествовала коммиту с исправлением.

## Что сделано

Создан Change Log в Test-web, чтобы запустить существующий workflow `LifeGame Preview Deploy`. Workflow берёт код из `raymondovich-cloud/LifeGame`, ветка `feature/pwa-static-cache`, и пишет SHA собранного исходника в `PREVIEW_BUILD.txt`.

## Границы

- Исходный код LifeGame и ветка `main` LifeGame не изменяются.
- Логика Domain/Application, данные, Supabase и авторизация не меняются.
- Не добавлены зависимости.

## Проверка

После завершения workflow проверить статус публикации и SHA в `PREVIEW_BUILD.txt`. Затем проверить публичные маршруты Finance, Health и Development в Safari.
