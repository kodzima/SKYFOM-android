# SKYFOM VPN

Android-клиент для протоколов VLESS / VMess / Trojan / Shadowsocks с авто-выбором сервера по живому пингу и переключением "на лету".

![Android](https://img.shields.io/badge/Android-24%2B-3DDC84?logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-2.x-7F52FF?logo=kotlin&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-Material%203-4285F4?logo=jetpackcompose&logoColor=white)
![License](https://img.shields.io/badge/license-Proprietary-blue)

## Возможности

- **Многопротокольный движок** — VLESS, VMess, Trojan, Shadowsocks через нативный Xray-core
- **TUN-туннель** на базе `hev-socks5-tunnel` (точный учёт трафика без двойного счёта)
- **Авто-режим**
  - Quick-connect к лучшему по кэшу/первому валидному конфигу за <500мс
  - Фоновый Xray-пинг до 200 серверов в подписке с TCP-префильтром
  - Live tolerance-switch: переключение на сервер быстрее на ≥50ms (cooldown 10s)
  - Health-monitor + HTTP-проба `cp.cloudflare.com / gstatic.com` каждые 30с
- **Импорт подписок** — URL, QR-код, буфер обмена, deep links (`vless://`, `vmess://`, `trojan://`, `ss://`, `skyfom://`, `sub://`, `v2rayng://`, `clash://` и др.)
- **Сортировка серверов** по пингу в реальном времени с цветовой индикацией (`<150ms` зелёный, `<400ms` оранжевый, `≥400ms` красный)
- **Kill Switch** для блокировки трафика при разрыве туннеля
- **Split Tunneling** — выбор приложений для маршрутизации
- **Pre-resolve DNS** доменов для обхода DPI-блокировок
- **Виджеты** для домашнего экрана + Quick Settings tile
- **Android TV** интерфейс с remote-friendly навигацией
- **Тёмная/светлая** Material 3 тема
- **Локализация** RU/EN
- **Без аналитики, рекламы, трекеров и обязательной регистрации**
