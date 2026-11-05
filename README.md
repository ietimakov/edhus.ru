# edhus.ru

Статический сайт Эдуарда Хуснутдинова: афиша ноября–декабря 2026 года и прямые ссылки на Ticketscloud.

## Локальный запуск

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Откройте http://127.0.0.1:4173 . Сборка и установка пакетов не нужны. Шрифты и логотип хранятся локально.

## Источник дизайна

https://web.archive.org/web/20260509191822/https://edhus.ru/

Сохранены оригинальные логотип, Montserrat, чёрно-белая палитра. Кнопки обновлены на жёлтые. По запросу заказчика в Hero и блок об артисте добавлены фотографии; ссылки на соцсети и музыкальные сервисы представлены логотипами. Исходные HTML и CSS архива сохранены локально в reference/ и исключены из Git.

## GitHub Pages

Публикация включена 05.11.2026: Deploy from a branch → main → /(root). Custom domain: edhus.ru; файл CNAME добавлен GitHub.

DNS перенесены с Бегета на ns1.reg.ru и ns2.reg.ru. В REG.RU сохранены:

- A @: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153.
- CNAME www: ietimakov.github.io.
- Прежние MX mx1.beget.com (10), mx2.beget.com (20), TXT SPF и подтверждение Google.

На момент настройки публичные DNS ещё возвращали старый IP 87.236.16.20; REG.RU указывает срок обновления до 24 часов. GitHub отдаёт новую страницу (HTTP 200, семь концертов) при обращении к его серверу с Host: edhus.ru. После обновления DNS и выпуска сертификата включите Enforce HTTPS в Settings → Pages. До этого HTTPS на собственном домене не подтверждён.

## Обновление афиши

Карточки находятся в index.html, в секции #concerts. Обновляйте город, дату time[datetime], видимую дату, aria-label и ссылку Ticketscloud вместе. Все семь дат взяты из списка заказчика; время и площадки не добавлены без подтверждения.

## Фотографии и логотипы

- Hero: https://i.ytimg.com/vi/DWA2VvE1UjY/maxresdefault.jpg
- Портрет: https://avatars.mds.yandex.net/get-afishanew/5098259/2269820fb426cebf13d9f7992fa6e082/960x690_noncrop
- Логотипы музыкальных сервисов восстановлены из архива edhus.ru. SVG-иконки соцсетей: [Font Awesome Free 6.7.2](https://fontawesome.com/) ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)).
