# 📡 Radar de Leads — Automação Inteligente de Prospecção

O Radar de Leads é uma ferramenta inteligente que automatiza a busca, filtragem e qualificação de leads em regiões específicas utilizando:

- Google Maps
- Busca por nicho + região
- Extração de contatos (e-mail, telefone, WhatsApp)
- IA para qualificação
- n8n para orquestração dos fluxos
- Exportação automática para planilhas, CRM ou WhatsApp

Este projeto faz parte do **Estúdio Diogo — IA, Automação e SaaS**.

---

## 🚀 Objetivo
Automatizar a captação de leads de forma estratégica, escalável e personalizada para prospecção comercial.

---

## 🧠 Funcionalidades Principais

- Busca em Google Maps com termos dinâmicos
- Extração de contatos quando disponíveis
- Filtro de duplicados (Redis)
- Qualificação por IA conforme nicho
- Exportação CSV / Excel / API
- Execução programada (ex: diário)
- Possível integração com WhatsApp para mensagens automáticas

---

## 📐 Arquitetura
Veja `architecture.md` no diretório raiz.

---

## 🔄 Fluxos n8n
Fluxos disponíveis em:

/workflows/scraping-flow.md
/workflows/qualification-flow.md


---

## 📊 Banco de Dados

- Supabase: armazenamento persistente de leads
- Redis: cache + duplicados + estatísticas rápidas

Modelo completo em `docs/data-model.md`.

---

## 📦 Instalação

1. Copiar os fluxos n8n
2. Configurar as variáveis:
   - GOOGLE_API_KEY
   - SUPABASE_URL
   - SUPABASE_KEY
3. Importar o workflow principal
4. Rodar a pipeline de teste

---

## 📞 Autor
**Diogo Bispo**  
IA • Automação • n8n • Bots • SaaS
