---
title: Ошибки, связанные с сертификатом
sidebar_position: 2
---

:::info

В этой статье рассказывается об AdGuard для Windows — многофункциональном блокировщике рекламы, который защищает ваше устройство на системном уровне. Чтобы увидеть, как он работает, [скачайте приложение AdGuard](https://adguard.com/download.html?auto=true)

:::

Чтобы фильтровать HTTPS-трафик и эффективно блокировать рекламу и трекеры, AdGuard генерирует специальный (и уникальный) корневой сертификат и устанавливает его в системное хранилище. Подробнее о том, почему требуется сертификат, вы можете узнать в [этой статье](/general/https-filtering/what-is-https-filtering).

Обычно браузеры доверяют сертификату AdGuard после его добавления в системное хранилище сертификатов в процессе установки. Но в некоторых случаях этого недостаточно, и вы можете столкнуться с предупреждениями или ошибками. Чаще всего это происходит в браузерах на базе Firefox, таких как Mozilla Firefox, PaleMoon, Waterfox и т. д., или в Яндекс.Браузере.

## *Потенциальная угроза безопасности* в браузерах на базе Firefox

![Ошибка угрозы безопасности](https://cdn.adtidy.org/public/Adguard/kb/en/certificate/cert_error_en.png)

Старые версии FireFox, а также браузеры на их основе, не доверяют сертификатам из системного хранилища, а только сертификатам из своего локального хранилища. Начиная с v68, FireFox доверяет системным сертификатам, но вы всё равно можете столкнуться с ошибкой «Соединение ненадёжно». Если что-то подобное произойдёт, сначала попробуйте нажать кнопку *Переустановить сертификат* — вы найдёте её на вкладке *Сеть*.

![Переустановить сертификат](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/reinstall.jpg)

Если это не помогло, следуйте инструкциям по ручному добавлению сертификата AdGuard в хранилище FireFox.
> Эта инструкция предназначена для браузера Firefox. Названия кнопок и пунктов меню могут отличаться в других браузерах на основе Firefox.

1) Запустите AdGuard.

2) Перейдите на страницу [http://local.adguard.org/cert](http://local.adguard.org/cert) и нажмите кнопку *Скачать* . Браузер начнёт загрузку файла **cert.cer** .
> Вы также можете открыть страницу загрузки, нажав на ссылку через приложение AdGuard: *Настройки → Сеть → HTTPS-фильтрация*.

![Настройки сертификата](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/link.jpeg)

3) Откройте браузер, а затем откройте *Настройки*.

4) Перейдите на вкладку *Приватность & защита*.

5) Прокрутите вниз до раздела *Сертификаты* и нажмите кнопку *Просмотр сертификатов*.

![Окно просмотра сертификатов](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/import1.jpeg)

Выберите вкладку *Центры сертификации*.

Нажмите кнопку *Импортировать...*.

![Настройки сертификата — импорт](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/import2.jpeg)

8) Найдите загруженный файл **cert.cer** и нажмите *Открыть*.

9) Установите флажок *Доверять этому ЦС для идентификации веб-сайтов* и нажмите *ОК*.

Вы успешно установили сертификат AdGuard. Перезапустите браузер, ошибка должна исчезнуть.

## Предупреждение сертификата Яндекс.Браузера

Если вы пользуютесь AdGuard для Windows и Яндекс.Браузером, вы могли столкнуться с этим предупреждением:

![Предупреждение сертификата Яндекс.Браузера](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/yandex-cert.png)

### Почему это происходит

И AdGuard, и Яндекс очень серьёзно относятся к безопасности пользователей в интернете. Текущая политика Яндекса заключается в том, чтобы предупреждать своих пользователей о любом сертификате, который не распознаётся браузером. Это небезосновательно, потому что иногда вредоносные приложения могут внедрять свои собственные сертификаты и использовать их для нанесения вреда системе и кражи личных данных.

Однако AdGuard также добавляет свой сертификат в список доверенных. Это и приводит к появлению предупреждения.

### Как решить проблему

Самый простой способ — нажать на кнопку **Перейти на сайт**. Это заставит Яндекс.Браузер запомнить сертификат AdGuard как доверенный хотя бы на время. Скорее всего вам больше не придётся видеть это сообщение, но вполне возможно, оно будет время от времени появляться по каким-то другим причинам. В таких случаях просто нажмите ту же кнопку ещё раз *(убедитесь, что это сертификат AdGuard!)*.

Отключение HTTPS-фильтрации в AdGuard также предотвратит повторное отображение этого сообщения в Яндекс.Браузере. Однако это приведёт к тому, что вы будете видеть рекламу, загружаемую по HTTPS (в том числе **собственную рекламу Яндекса**) на таких сайтах, как YouTube , Facebook, Instagram и многие другие. Мы настоятельно не рекомендуем делать это, если вы хотите сохранить высокое качество блокировки рекламы.
