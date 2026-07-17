# Content Protection Bot (Python + Pyrogram)

## Heroku Par 4 Environment Variables Set Karo

| Variable | Value |
|---|---|
| `TELEGRAM_BOT_TOKEN` | BotFather se mila token |
| `TELEGRAM_API_ID` | my.telegram.org se |
| `TELEGRAM_API_HASH` | my.telegram.org se |
| `OWNER_ID` | Aapka Telegram User ID |

## Apna User ID Kaise Pata Kare
@userinfobot ko message karo Telegram par — wo aapka ID bata dega.

## Heroku Deploy (Phone se bhi ho sakta hai)

```bash
heroku create your-bot-name

heroku config:set TELEGRAM_BOT_TOKEN="123:ABC"
heroku config:set TELEGRAM_API_ID="1234567"
heroku config:set TELEGRAM_API_HASH="abcdef123"
heroku config:set OWNER_ID="7954041423"

git init
git add .
git commit -m "init"
git push heroku main

heroku ps:scale worker=1
heroku logs --tail
```

## Bot Kaise Kaam Karta Hai

1. Bot ko Target Channel aur Source Channel ka admin banao
2. Admin Panel → Channel Configurations → Link New Channels
3. Target Channel ID bhejo (-100 se shuru)
4. Source Channel ID bhejo
5. Ab jab bhi Target par video/photo/document upload hoga:
   - Bot protected link Source Channel par post karega
   - User link click karega → bot se media milega (protected, forward-proof)

## Features
- ✅ Owner + Multi-Admin system
- ✅ Admin expiry (30d, 365d etc.)
- ✅ Daily view limits per user
- ✅ Ban/Unban users
- ✅ Broadcast to all users
- ✅ Log channel backup
- ✅ Private message to users
- ✅ Maintenance mode
- ✅ ASCII loading animation
- ✅ SQLite database (Heroku par persist karta hai)
