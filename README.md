<div align="center">

# 🎙️ ReyVoice

**Discord-бот для озвучивания текста и создания голосовых моделей только с явного согласия пользователя.**

![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white)
![Discord.js](https://img.shields.io/badge/discord.js-v14-5865F2?logo=discord&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?logo=sqlite&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)

</div>

## Возможности

- `/сказать` — подключение к голосовому каналу и озвучивание текста;
- `/клонировать` — запрос согласия, запись образца и создание модели;
- `/голоса` и `/удалить_голос` — управление сохранёнными голосами;
- `/админ` — панель владельца;
- Fish Audio и ElevenLabs;
- локальный режим для проверки без API-ключей;
- SQLite, журналирование и русские сообщения об ошибках.

## Принцип согласия

ReyVoice не выполняет скрытую запись. Запись начинается только после того, как выбранный пользователь нажал кнопку подтверждения. Записывается только голос подтвердившего пользователя.

## Установка

```bash
npm install
```

Скопируй `.env.example` в `.env` и заполни:

```env
DISCORD_TOKEN=your_bot_token
CLIENT_ID=your_application_id
GUILD_ID=your_test_server_id
OWNER_ID=your_discord_user_id
TTS_PROVIDER=local
```

Затем зарегистрируй команды и запусти бота:

```bash
npm run deploy
npm start
```

## Провайдеры

- `local` — тестовый локальный режим;
- `fish` — Fish Audio;
- `elevenlabs` — ElevenLabs.

API-ключи читаются только из `.env` и не должны попадать в репозиторий.

## Лицензия

Проект распространяется по лицензии MIT.
