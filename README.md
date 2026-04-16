[README_CrmFlowAI.md](https://github.com/user-attachments/files/26771980/README_CrmFlowAI.md)
#  CRM Flow AI

> CRM automatizado com IA — ao adicionar um novo cliente no Google Sheets, o sistema gera e envia um email de boas-vindas personalizado automaticamente.

---

##  Sobre o projeto

O **CRM Flow AI** é uma automação de relacionamento com clientes construída com **n8n** que conecta **Google Sheets**, **Groq AI** e **Gmail** em um fluxo inteligente.

Sempre que um novo cliente é adicionado na planilha, o sistema detecta a entrada, usa a **Groq AI** para gerar um email de boas-vindas personalizado com os dados do cliente e o envia automaticamente via Gmail — sem nenhuma ação manual.

Ideal para times de vendas, freelancers e pequenas empresas que usam planilhas como CRM e querem automatizar o primeiro contato com novos clientes.

---

##  Como funciona

```
Novo cliente adicionado no Google Sheets
               ↓
n8n detecta a nova linha na planilha
               ↓
Groq AI gera email de boas-vindas personalizado
  (com nome, contexto e tom profissional)
               ↓
Gmail envia o email automaticamente ao cliente
```

---

##  Tecnologias utilizadas

| Ferramenta | Função |
|---|---|
| [n8n](https://n8n.io) | Orquestração do fluxo de automação |
| [Google Sheets API](https://developers.google.com/sheets) | Monitoramento e leitura de dados do CRM |
| [Groq AI](https://groq.com) | Geração do email de boas-vindas personalizado |
| [Gmail API](https://developers.google.com/gmail) | Envio automático do email ao cliente |

---

##  Funcionalidades

- ✅ Monitoramento automático de novas entradas no Google Sheets
- ✅ Geração de email personalizado com dados do cliente via Groq AI
- ✅ Envio automático via Gmail sem intervenção humana
- ✅ Funciona como um CRM leve usando apenas planilhas
- ✅ Fluxo 100% no-code via n8n

---

##  Como usar

### Pré-requisitos

- Conta no [n8n](https://n8n.io) (self-hosted ou cloud)
- Chave de API da [Groq](https://console.groq.com)
- Conta Google com Google Sheets API e Gmail API habilitadas

### Configuração

1. Clone este repositório
2. Importe o arquivo `index` no n8n
3. Configure as credenciais:
   - Google Sheets OAuth2
   - Groq API Key
   - Gmail OAuth2
4. Aponte o nó do Google Sheets para sua planilha de clientes
5. Ative o workflow

### Estrutura da planilha

A planilha deve conter ao menos as colunas:

| Nome | Email | Empresa (opcional) |
|------|-------|-------------------|
| João Silva | joao@email.com | Empresa X |

---

##  Estrutura do projeto

```
Crm-flow-ai/
├── index           # Fluxo exportado do n8n
└── README.md
```

---

##  Autor

**João Pedro Silva dos Santos**  
[GitHub](https://github.com/JoaoPedroske) · [Email](mailto:joaopedrosilvadossantos94@gmail.com)

---

##  Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
