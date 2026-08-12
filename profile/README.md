# ZapClaw

**A WhatsApp Business API gateway on the official Meta Cloud API.** Inbound messages
arrive at your webhook, outbound messages go through a REST API, and the number keeps
working in the WhatsApp app on the phone at the same time, through Meta's Coexistence.

Built for developers, makers and agencies in Brazil who already have a bot, an
automation or an AI agent on WhatsApp and need the number not to be blocked by using an
unofficial reverse-engineered client.

```sh
curl -X POST https://api.zapclaw.app/api/v1/send/text \
  -H "X-API-Key: zc_live_..." \
  -d '{ "from": "5511...", "to": "5511...", "text": "Order #1234 is confirmed" }'
```

## Repositories here

- **[chatwoot-zapclaw](https://github.com/zapclaw/chatwoot-zapclaw)**, connect Chatwoot
  self-hosted to the official WhatsApp Cloud API without going through Meta App Review
  yourself. Two environment variables and a restart.

## What it is not

Honest limits, because finding them out an hour in is worse than reading them now. These
come from Meta's Coexistence mode and no provider can lift them: throughput is fixed at
20 messages per second, there is no support for groups, voice or video calls, ephemeral
messages or the Official Business Account green badge, and messages the business sends
from WhatsApp for Windows or WearOS do not generate webhooks. It is also not a tool for
bulk broadcasting.

Running on the official API removes the ban risk that comes from reverse-engineered
WhatsApp Web clients. It does not make an account unbannable: Meta can still restrict a
WhatsApp Business Account for quality, policy or verification reasons.

## Links

- [zapclaw.app](https://zapclaw.app)
- [API and webhook reference](https://zapclaw.app/docs.html)
- [OpenAPI 3.0 specification](https://zapclaw.app/openapi.yaml)
- [Pricing](https://zapclaw.app/pricing.html)
- [llms.txt](https://zapclaw.app/llms.txt), a machine-readable summary for LLMs and agents

---

## Em português

O **ZapClaw** é um gateway de mensagens do WhatsApp na **API oficial da Meta Cloud**, com
Coexistência: as mensagens recebidas chegam no seu webhook, o envio é feito por uma API
REST, e o número continua funcionando no aplicativo do celular ao mesmo tempo.

Serve para quem já construiu uma automação, um chatbot ou um agente de IA no WhatsApp e
precisa que o número não seja bloqueado. Sem CNPJ para conectar, e números ilimitados nos
planos pagos.

- [Site e preços](https://zapclaw.app/pt/)
- [Chatwoot sem App Review da Meta](https://github.com/zapclaw/chatwoot-zapclaw)
- [Resumo para LLMs](https://zapclaw.app/llms-pt.txt)

WhatsApp é marca registrada da Meta Platforms, Inc. O ZapClaw não tem vínculo com a Meta
nem é endossado por ela.
