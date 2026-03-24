# API Conta Simples — Developer Portal

Documentação técnica da API Conta Simples, construída com [Documentation.ai](https://documentation.ai).

## Estrutura

```
├── documentation.json          # Configuração principal (navegação, cores, branding)
├── index.mdx                   # Página inicial do portal
├── comece-aqui/                # Guias iniciais
│   ├── quickstart.mdx          # Primeira chamada em 5 minutos
│   ├── autenticacao.mdx        # OAuth 2.0 Client Credentials
│   └── ambientes.mdx           # Sandbox vs Produção
├── guias/                      # Guias de integração
│   ├── fluxo-integracao.mdx    # Passo a passo do Sandbox à Produção
│   └── boas-praticas.mdx       # Paginação, retry, segurança
├── referencia/                 # Material de referência
│   └── dicionario-dados.mdx    # Entidades, campos e enumerações
├── operacao/                   # Operação e suporte
│   ├── erros-comuns.mdx        # Diagnóstico de erros por código HTTP
│   ├── suporte.mdx             # Canais de suporte e template de chamado
│   └── changelog.mdx           # Histórico de mudanças da API
├── api-reference/              # Referência técnica da API
│   ├── introducao.mdx          # Visão geral dos endpoints
│   └── openapi.json            # Especificação OpenAPI 3.0.3
└── collections/                # Ferramentas de teste
    ├── index.mdx               # Guia de uso da Postman Collection
    ├── postman_collection.json # Collection v2.1 com os 3 endpoints
    └── postman_environment_sandbox.json # Environment Sandbox
```

## Navegação

O portal é organizado em 4 tabs:

| Tab | Conteúdo |
|-----|----------|
| **Guides** | Quickstart, autenticação, ambientes, fluxo de integração, boas práticas, dicionário de dados, erros e suporte |
| **API Reference** | Introdução + endpoints gerados automaticamente a partir do OpenAPI |
| **Collections** | Postman Collection e Environment para testes rápidos |
| **Changelog** | Histórico de versões e mudanças da API |

## Endpoints da API

| Endpoint | Método | Descrição |
|----------|--------|-----------|
| `/oauth/v1/access-token` | POST | Obter token de acesso (OAuth 2.0 Client Credentials, Basic api_key:api_secret) |
| `/statements/v1/credit-card` | POST | Consultar extrato de transações de cartão |
| `/attachments/v1/content/{attachmentId}` | GET | Download de anexos (comprovantes, notas fiscais) |

## Ambientes

| Ambiente | URL Base |
|----------|----------|
| Sandbox | `https://api-sandbox.contasimples.com` |
| Produção | `https://api.contasimples.com` |

## Desenvolvimento local

Para visualizar a documentação localmente, siga as instruções do [Documentation.ai](https://documentation.ai).

As credenciais da API são gerenciadas pelo [Internet Banking da Conta Simples](https://ib.contasimples.com/integracoes/api/credenciais).
