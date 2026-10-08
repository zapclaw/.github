# ZapClaw

**ZapClaw is a WhatsApp Business API gateway on Meta's official Cloud API.** Inbound
messages arrive at your webhook, outbound messages go through a REST API, and the number
keeps working in the WhatsApp Business app on the phone at the same time, through
WhatsApp Coexistence.

Built for developers, makers and agencies who already have a bot, an automation or an AI
agent on WhatsApp and want it on the official API instead of an unofficial
reverse-engineered client.

```sh
curl -X POST https://api.zapclaw.app/api/v1/send/text \
  -H "X-API-Key: zc_live_..." \
  -H "Content-Type: application/json" \
  -d '{ "from": "5511...", "to": "5511...", "text": "Order #1234 is confirmed" }'
```

**[Start free][register]** · [Docs][docs] · [Pricing][pricing]

## Repositories here

- **[chatwoot-zapclaw](https://github.com/zapclaw/chatwoot-zapclaw)**: Chatwoot
  self-hosted on the official WhatsApp Cloud API, with the number still in the WhatsApp
  Business app on the phone. One environment variable, then one API call per number.

## Guides

| Question | English | Português |
|---|---|---|
| What do I need to connect a number through Coexistence? | [Requirements][req-en] | [Requisitos][req-pt] |
| Meta says my number is not eligible. What now? | [Not eligible][elig-en] | [Não elegível][elig-pt] |
| Meta asks me to delete my WhatsApp Business account. Should I? | [Don't][del-en] | [Não apague][del-pt] |
| Can I connect a German or other EU number? | [Germany and the EU][eu-en] | [Alemanha e UE][eu-pt] |
| Can my own AI read WhatsApp messages through a webhook? | [Webhook to your AI][ai-en] | [Webhook para a sua IA][ai-pt] |
| How do I run Chatwoot with the number still on the phone? | [Chatwoot guide][chatwoot] | [chatwoot-zapclaw](https://github.com/zapclaw/chatwoot-zapclaw/blob/main/README.pt-BR.md) |

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

- [zapclaw.app][home]
- [API and webhook reference][docs]
- [OpenAPI 3.0 specification](https://zapclaw.app/openapi.yaml)
- [Pricing][pricing]
- [llms.txt](https://zapclaw.app/llms.txt), a machine-readable summary for LLMs and agents

ZapClaw is a product of CHARLES BERTI TECNOLOGIA DA INFORMAÇÃO LTDA
(CNPJ 66.037.451/0001-01), São Paulo, Brazil, the same company that publishes
[Monely](https://monely.app).

---

## Em português

**O ZapClaw é um gateway de WhatsApp na API oficial da Meta.** As mensagens recebidas
chegam no seu webhook, o envio é feito por uma API REST, e o número continua funcionando
no app WhatsApp Business do celular ao mesmo tempo, pela Coexistência do WhatsApp.

Serve para quem já construiu uma automação, um chatbot ou um agente de IA no WhatsApp e
quer rodar na API oficial em vez de um cliente não oficial feito por engenharia reversa.
Sem CNPJ para conectar, e números ilimitados nos planos pagos.

- [Comece grátis][register]
- [Site][home-pt] e [preços][pricing-pt]
- [Chatwoot na API oficial, com o número ainda no celular](https://github.com/zapclaw/chatwoot-zapclaw/blob/main/README.pt-BR.md)
- [Resumo para LLMs](https://zapclaw.app/llms-pt.txt)

O ZapClaw é um produto da CHARLES BERTI TECNOLOGIA DA INFORMAÇÃO LTDA
(CNPJ 66.037.451/0001-01), São Paulo, Brasil, a mesma empresa que publica o
[Monely](https://monely.app).

WhatsApp é marca registrada da Meta Platforms, Inc. O ZapClaw não tem vínculo com a Meta
nem é endossado por ela.

[home]: https://zapclaw.app/?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[home-pt]: https://zapclaw.app/pt/?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[register]: https://app.zapclaw.app/register?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[docs]: https://zapclaw.app/docs.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[chatwoot]: https://zapclaw.app/docs.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile#chatwoot
[pricing]: https://zapclaw.app/pricing.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[pricing-pt]: https://zapclaw.app/pt/pricing.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[req-en]: https://zapclaw.app/coexistence-requirements.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[req-pt]: https://zapclaw.app/pt/coexistence-requirements.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[elig-en]: https://zapclaw.app/coexistence-not-eligible.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[elig-pt]: https://zapclaw.app/pt/coexistence-not-eligible.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[del-en]: https://zapclaw.app/coexistence-delete-account.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[del-pt]: https://zapclaw.app/pt/coexistence-delete-account.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[eu-en]: https://zapclaw.app/coexistence-germany-eu.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[eu-pt]: https://zapclaw.app/pt/coexistence-germany-eu.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[ai-en]: https://zapclaw.app/whatsapp-webhook-local-ai.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
[ai-pt]: https://zapclaw.app/pt/whatsapp-webhook-local-ai.html?utm_source=github&utm_medium=referral&utm_campaign=org-profile
