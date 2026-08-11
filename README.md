# PersOrgTelegramBotTriage

One static HTML file: the capture-triage form for a personal Telegram bot.

**It holds no data and talks to no server of mine.** The bot opens it as a
Telegram Mini App with the proposed items in the URL *fragment* — a fragment is
never sent to the host, so nothing typed or captured reaches GitHub — and the
edited result goes straight back to the bot through Telegram's own
`WebApp.sendData`, which Telegram authenticates. There is no API, no endpoint,
no inbound port anywhere in the design.

Open it in a plain browser and it renders a demo capture, so the form can be
looked at without any of that.

This repository exists only to serve the page over HTTPS, which Telegram
requires. The source of truth is `miniapp/triage.html` in the (private) bot
repository; this is a published copy.
