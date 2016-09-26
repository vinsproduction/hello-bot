# hello-bot
Пример бота для телеграм на PHP

# Создание телеграм бота. Настройка Webhook.

1 Добавить BotFather (https://telegram.me/BotFather) в свой телеграм

2 Создать черерез него нового бота и получить ТОКЕН

3 Создать на своем сервере страницу <хуемоебот.php> Это будет ваш Webhook

5 Прикрутиь https к вашему сайту! Для этого понадобится ssl сертификат. Подойдет самописный. 
Как его создать, описано тут https://core.telegram.org/bots/webhooks#a-self-signed-certificate

Сертификат должен быть в  pem формате! 
(лично я делал его путем экспорта crt в pem, через связку ключей Mac. Она автоматически открывается если кликнуть по crt файлу)

6 Связать свой Webhook с сервером Telegram

curl -F "url=https://<Ваш сайт>/<хуемоебот.php>" -F "certificate=@<Ваш сертификат>.pem" https://api.telegram.org/bot<Ваш токен>/setWebhook

Это все! Если не запутилось, смотрите сертификат

------

Проверить работет вебхук  или нет, можно так https://core.telegram.org/bots/webhooks#testing-your-bot-with-updates
Проставьте свой чат id на котором стоит бот
