# CF VLESS Worker

Личный VLESS-over-WebSocket прокси на Cloudflare Workers (бесплатный план).

## Деплой

1. Cloudflare Dashboard -> **Workers & Pages** -> **Create** -> **Import a repository**.
2. Подключить GitHub и выбрать репозиторий **edgetunnel**.
3. Project name: `cf-vless`.
4. Build command: оставить пустым. Deploy command: `npx wrangler deploy`.
5. Deploy.

## UUID

После первого деплоя:

Worker `cf-vless` -> **Settings** -> **Variables and Secrets** -> **Add**:

- Name: `UUID`
- Value: `97585332-3c72-41c2-874e-7fcde5490146`

Save and deploy.

## Ссылка для клиента

Открыть:

```
https://cf-vless.<твой-subdomain>.workers.dev/97585332-3c72-41c2-874e-7fcde5490146
```

Страница вернёт готовую `vless://` ссылку. Импортировать её в **v2rayNG** на Android.

## Если workers.dev не открывается

Привязать свой домен в Worker -> Settings -> Domains & Routes, либо использовать
другой клиент/сеть. Для России `workers.dev` иногда режется провайдером.
