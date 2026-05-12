# Политика конфиденциальности — SKYFOM VPN

**Последнее обновление:** 12 мая 2026 г.

[English version below ↓](#privacy-policy--skyfom-vpn)

---

## 1. Общие сведения

Настоящая Политика конфиденциальности описывает, какую информацию собирает и использует приложение **SkyfomVPN** (идентификатор пакета: `com.bfs.skyfomvpn`), разработанное **Bastion Forge Studio**.

Используя приложение, вы соглашаетесь с условиями данной политики. Если вы не согласны — пожалуйста, удалите приложение.

## 2. Данные, которые мы собираем

### 2.1 Данные, хранимые только на вашем устройстве

- VPN-конфигурации серверов (импортируются вами из URL подписок, QR-кодов или буфера обмена)
- Настройки приложения (тема, язык, kill-switch, сплит-туннелинг и др.)
- Статистика сессий: объём трафика (входящий/исходящий), время соединения — только локально
- Опциональный профиль пользователя: имя, e-mail, Telegram — вводится вручную и нигде не передаётся
- Журналы подключений — только если вы включили параметр «Собирать логи» в настройках

### 2.2 Данные, передаваемые при работе приложения

| Что передаётся | Кому | Цель |
|---|---|---|
| Версия приложения (User-Agent) | `skyfom.ru/api/v1/version/` | Проверка обновлений |
| URL подписки + идентификатор устройства (HWID) | Серверы вашего провайдера подписки | Получение списка серверов, проверка лицензии |
| HEAD-запрос `gstatic.com/generate_204` / `cp.cloudflare.com` | Через ваш VPN-прокси | Проверка работоспособности туннеля (health-probe) |

HWID — это хэш SHA-256 от идентификаторов вашего устройства (Android ID, модель). Он не позволяет лично идентифицировать вас и используется провайдерами подписок исключительно для привязки лицензии к устройству.

## 3. Чего мы не делаем

- ❌ Нет аналитики
- ❌ Нет рекламы
- ❌ Нет Firebase / трекеров
- ❌ Нет отчётов о сбоях
- ❌ Нет сбора местоположения
- ❌ Нет продажи данных
- ❌ Аккаунт не требуется

## 4. Разрешения приложения

| Разрешение | Назначение |
|---|---|
| `INTERNET` | Установка VPN-соединения и загрузка подписок |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_SPECIAL_USE` | Работа VPN-сервиса в фоновом режиме |
| `BIND_VPN_SERVICE` | Системное разрешение VpnService для маршрутизации трафика |
| `CAMERA` | Сканирование QR-кодов с конфигурациями (только по запросу пользователя) |
| `RECEIVE_BOOT_COMPLETED` | Автоподключение после перезагрузки устройства (если включено) |
| `POST_NOTIFICATIONS` | Уведомления о статусе VPN-соединения |
| `QUERY_ALL_PACKAGES` | Выбор приложений для сплит-туннелинга |
| `ACCESS_NETWORK_STATE` / `ACCESS_WIFI_STATE` | Определение текущей сети (Wi-Fi / LTE) для авто-режима |

## 5. Сторонние библиотеки

Приложение использует следующие библиотеки с открытым исходным кодом:

- **Xray-core** (XTLS) через libXray — прокси-движок, работает локально на устройстве
- **hev-socks5-tunnel** (heiher) — TUN↔SOCKS5 мост, нативная С-библиотека
- **Google ML Kit** — сканирование QR-кодов, обработка происходит локально на устройстве
- **AndroidX / Jetpack Compose** — интерфейс, база данных Room, фоновые задачи
- **OkHttp** — HTTP-запросы к API обновлений и подпискам
- **Kotlin Coroutines** — асинхронные операции

Ни одна из этих библиотек не используется для сбора пользовательских данных или показа рекламы.

## 6. Хранение и безопасность данных

Все данные хранятся в приватном хранилище приложения (`/data/data/com.bfs.skyfomvpn/`) на вашем устройстве и не доступны другим приложениям. При удалении приложения или очистке его данных все сохранённые конфигурации и статистика удаляются безвозвратно.

VPN-соединение зашифровано протоколами VLESS / VMess / Trojan / Shadowsocks (TLS 1.3, Reality, AEAD-шифры). Приложение не ведёт серверных баз данных о пользователях.

## 7. Дети

Приложение не предназначено для детей младше 13 лет. Мы не собираем осознанно данные лиц этой возрастной группы.

## 8. Изменения в политике

При существенных изменениях политики мы обновим дату «Последнее обновление» в начале документа. Продолжение использования приложения означает ваше согласие с новой редакцией.

## 9. Контакты

По вопросам конфиденциальности свяжитесь с нами:

- **E-mail:** [yanikita67@gmail.com](mailto:yanikita67@gmail.com)
- **Telegram:** [@skyfom_client](https://t.me/skyfom_client)
- **Сайт:** [skyfom.ru](https://skyfom.ru)

---

# Privacy Policy — SKYFOM VPN

**Last updated:** May 12, 2026

## 1. Overview

This Privacy Policy explains what information **SkyfomVPN** (package: `com.bfs.skyfomvpn`), developed by **Bastion Forge Studio**, collects and how it is used.

By using the app you agree to this policy. If you do not agree, please uninstall the app.

## 2. Data We Collect

### 2.1 Data stored only on your device

- VPN server configurations (imported by you from subscription URLs, QR codes, or clipboard)
- App settings (theme, language, kill-switch, split-tunneling, etc.)
- Session statistics: traffic volume (upload/download), connection duration — local only
- Optional user profile: name, e-mail, Telegram — entered manually and never transmitted
- Connection logs — only if you enable "Collect logs" in settings

### 2.2 Data transmitted during app operation

| What is sent | Recipient | Purpose |
|---|---|---|
| App version (User-Agent header) | `skyfom.ru/api/v1/version/` | Update check |
| Subscription URL + device identifier (HWID) | Your subscription provider's servers | Fetching server list, license validation |
| HEAD request to `gstatic.com/generate_204` / `cp.cloudflare.com` | Through your VPN proxy | Tunnel health probe |

HWID is a SHA-256 hash derived from your device identifiers (Android ID, model). It cannot personally identify you and is used by subscription providers solely for device-based license binding.

## 3. What We Do Not Do

- ❌ No analytics
- ❌ No advertising
- ❌ No Firebase / trackers
- ❌ No crash reporting
- ❌ No location tracking
- ❌ No data selling
- ❌ No account required

## 4. App Permissions

| Permission | Purpose |
|---|---|
| `INTERNET` | Establish VPN connections and download subscriptions |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_SPECIAL_USE` | Run the VPN service in the background |
| `BIND_VPN_SERVICE` | System VpnService permission for traffic routing |
| `CAMERA` | Scan QR codes containing configurations (on demand only) |
| `RECEIVE_BOOT_COMPLETED` | Auto-connect after device reboot (if enabled) |
| `POST_NOTIFICATIONS` | VPN connection status notifications |
| `QUERY_ALL_PACKAGES` | Select apps for split-tunneling |
| `ACCESS_NETWORK_STATE` / `ACCESS_WIFI_STATE` | Detect current network type (Wi-Fi / cellular) for auto-mode |

## 5. Third-party Libraries

The app uses the following open-source libraries:

- **Xray-core** (XTLS) via libXray — proxy engine, runs locally on device
- **hev-socks5-tunnel** (heiher) — TUN↔SOCKS5 bridge, native C library
- **Google ML Kit** — QR code scanning, all processing happens on-device
- **AndroidX / Jetpack Compose** — UI, Room database, background tasks
- **OkHttp** — HTTP requests to update API and subscriptions
- **Kotlin Coroutines** — async operations

None of these libraries are used to collect user data or serve ads.

## 6. Data Storage & Security

All data is stored in the app's private storage (`/data/data/com.bfs.skyfomvpn/`) on your device and is inaccessible to other apps. Uninstalling the app or clearing its data permanently removes all stored configurations and statistics.

VPN connections are encrypted using VLESS / VMess / Trojan / Shadowsocks protocols (TLS 1.3, Reality, AEAD ciphers). We do not maintain any server-side database of users.

## 7. Children

The app is not directed at children under 13. We do not knowingly collect data from this age group.

## 8. Policy Changes

For material changes we will update the "Last updated" date at the top of this document. Continued use of the app constitutes acceptance of the revised policy.

## 9. Contact

For privacy questions contact us:

- **E-mail:** [yanikita67@gmail.com](mailto:yanikita67@gmail.com)
- **Telegram:** [@skyfom_client](https://t.me/skyfom_client)
- **Website:** [skyfom.ru](https://skyfom.ru)
