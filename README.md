# Agente WhatsApp com IA

Agente de IA para WhatsApp construído com Claude (Anthropic), FastAPI, Redis e Z-API.

## Funcionalidades

- Responde mensagens de texto
- Transcreve áudios automaticamente (Groq Whisper)
- Lê e analisa PDFs e planilhas Excel
- Memória persistente por usuário
- Painel admin com visualização de conversas
- Prompt editável pelo painel — sem redeploy
- Arquivos de referência injetados no prompt automaticamente

## Variáveis de ambiente necessárias

| Variável | Descrição |
|----------|-----------|
| ANTHROPIC_API_KEY | Chave da API da Anthropic |
| GROQ_API_KEY | Chave da API do Groq (transcricao de audio) |
| AGENT_NAME | Nome do agente |
| AGENT_MODEL | Modelo do Claude (padrao: claude-haiku-4-5-20251001) |
| ZAPI_INSTANCE_ID | Instance ID da Z-API |
| ZAPI_TOKEN | Token da Z-API |
| ZAPI_CLIENT_TOKEN | Client Token da Z-API |
| REDIS_URL | URL do Redis |
| ADMIN_USER | Login do painel admin |
| ADMIN_PASS | Senha do painel admin |
| BASE_URL | URL publica do servidor |

## Deploy

Start Command:
```
uvicorn main:app --host 0.0.0.0 --port $PORT
```

## Painel admin

Acesse `/admin` com o login e senha configurados nas variaveis.
