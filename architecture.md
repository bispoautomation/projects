# 🏗️ Arquitetura — Radar de Leads

---

## 📌 Visão Geral
A arquitetura é composta por:

### - n8n → Orquestração principal  
### - Python (opcional) → Scraper avançado  
### - IA → Qualificação e limpeza  
### - Supabase → Armazenamento de leads  
### - Redis → Cache + duplicados  

---

## 🔄 Fluxo Completo

1. n8n dispara pesquisa
2. Scraper do Maps coleta dados (API ou scraping indireto)
3. IA qualifica e pontua
4. Redis evita duplicados
5. Supabase armazena
6. Exportação automática (planilha/CRM)

---

## 🧠 IA Envolvida

### Prompt principal (ver prompts/qualifier_prompt.txt)
- Analisa nicho
- Determina relevância
- Calcula score
- Remove leads ruins
- Retorna JSON com estrutura validada

---

## 🧩 Banco de Dados (Supabase)

Tabela: `leads`

| Campo         | Tipo         |
|---------------|--------------|
| id            | uuid         |
| name          | text         |
| phone         | text         |
| email         | text         |
| address       | text         |
| latitude      | float        |
| longitude     | float        |
| category      | text         |
| city          | text         |
| score         | int          |
| created_at    | timestamp    |

---

## ☁️ Infra
- Deploy opcional no PythonAnywhere, Vercel ou Render
- n8n rodando em contêiner (Replit, Railway, VPS etc.)

---

## 📦 Escalabilidade
- Paralelização por regiões
- Caching pesado em Redis
- Requisições controladas ao Maps
