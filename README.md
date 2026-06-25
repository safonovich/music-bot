# Ambient Mixer — Telegram Mini App

Миксер эмбиентных звуков. 9 звуков, слайдеры громкости, Animate, Timer, Share.

---

## Шаг 1 — Задеплоить фронтенд на GitHub Pages

1. Создай новый репозиторий на github.com (например `ambient-miniapp`)
2. Загрузи в него **все файлы из этой папки** (index.html + папку sounds/)
3. Открой Settings → Pages → Source: выбери `main` branch, папку `/ (root)`
4. Через минуту сайт появится по адресу: `https://ТВО_ЛОГИН.github.io/ambient-miniapp/`

> Проверь что сайт открывается в браузере и звуки играют.

---

## Шаг 2 — Вставить URL в бота

Открой `bot/bot.py`, найди строку:
```
WEBAPP_URL = "WEBAPP_URL"
```
Замени на свой URL из шага 1:
```
WEBAPP_URL = "https://ТВО_ЛОГИН.github.io/ambient-miniapp/"
```

---

## Шаг 3 — Запустить бота локально (для теста)

```bash
cd bot
pip install -r requirements.txt
BOT_TOKEN=8869384033:AAGL_... python bot.py
```

Открой Telegram, напиши боту `/start` — появится кнопка с Mini App.

---

## Шаг 4 — Задеплоить бота на Railway (бесплатно, работает 24/7)

1. Зарегистрируйся на railway.app
2. Создай новый проект → Deploy from GitHub repo
3. Подключи репозиторий (или загрузи только папку `bot/`)
4. В настройках проекта добавь переменную окружения:
   - `BOT_TOKEN` = твой токен от BotFather
5. Railway автоматически запустит бота

---

## Структура файлов

```
ambient-miniapp/
├── index.html          ← весь фронтенд Mini App
├── sounds/
│   ├── rain.mp3
│   ├── thunder.mp3
│   ├── waves.mp3
│   ├── wind.mp3
│   ├── fire.mp3
│   ├── birds.mp3
│   ├── handpan.mp3
│   ├── didgeridoo.mp3
│   └── ambient.mp3
├── bot/
│   ├── bot.py
│   └── requirements.txt
└── README.md
```
