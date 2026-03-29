# 🧛 DarkRise | V Rising Dedicated Server

Приватний PvP Duo сервер з VoIP підтримкою.

## Вимоги
- Docker
- Docker Compose

---

## Запуск

**1. Створи `.env`:**
```bash
cp .env.example .env
# Заповни своїми даними
```

**2. Налаштуй VoIP:**
```bash
cp config/ServerVoipSettings.json.example config/ServerVoipSettings.json
# Заповни даними з https://cloud.unity.com/home/organizations
```

**3. Запусти:**
```bash
docker compose up -d
```

**4. Логи:**
```bash
docker logs -f vrising
```

**5. Зупинити / перезапустити:**
```bash
docker compose down
docker compose down && docker compose up -d
```

---

## Конфіги

### `.env` — секрети (не пушити в git!)
```bash
TZ=Europe/Kiev
SERVERNAME="[UA/EU] DarkRise | Duo PvP | x2 | VoIP"
GAMEPORT=9876
QUERYPORT=9877
WORLDNAME=world1
WINEDEBUG=fixme-all
```

### `config/ServerVoipSettings.json` — VoIP (не пушити в git!)
Скопіюй з `ServerVoipSettings.json.example` і заповни даними з [Vivox dashboard](https://cloud.unity.com/home/organizations) (Видалити .example).

### `config/adminlist.txt` — адміни
Додай Steam ID кожного адміна з нового рядка:
```
7656119**********
```