# 📡 PRD — Radar de Leads

## 🎯 Objetivo
Criar uma ferramenta que encontra leads automaticamente via Google Maps, filtra, qualifica e entrega listas altamente relevantes para prospecção comercial.

---

## 🧩 Problema
Empresas e freelancers gastam muito tempo “caçando” leads manualmente — um processo lento, caro e impreciso.

---

## 💡 Solução Proposta
Um sistema automatizado que pesquisa cidades, nichos e regiões, extrai contatos, aplica IA para qualificar e transforma isso numa lista pronta para prospecção.

---

## 🛠 Escopo Funcional

### 1. Entrada de parâmetros
- Nicho (ex: pizzaria, mecânico, advogado)
- Localização (cidade, bairro, raio)
- Filtros adicionais (aberto agora, classificação mínima etc.)

### 2. Scraping Google Maps
- Busca dinâmica por termos combinados
- Extração de:
  - Nome da empresa
  - Endereço
  - Telefone
  - Site
  - Horário
  - Tags (restaurante, farmácia etc.)

### 3. IA de Qualificação
A IA deve:
- Analisar relevância
- Avaliar fit ideal
- Criar pontuação (0–100)
- Eliminar leads ruins

### 4. Pipeline de Duplicados
- Redis para evitar buscar o mesmo lead novamente

### 5. Exportação
- CSV
- Excel
- Envio para CRM via API
- Envio para WhatsApp (opcional)

---

## 🧱 Requisitos Não-Funcionais
- Alta escalabilidade  
- Execução rápida  
- Logs completos  
- Resiliência a erros do Maps  

---

## 📊 Métricas
- Leads capturados por dia
- Leads qualificados
- Tempo médio por busca
- Custo de IA por lote

---

## 🧪 MVP (primeira versão)

- [ ] Scraper básico Google Maps
- [ ] IA de qualificação (modelo simples)
- [ ] Exportação CSV
- [ ] Workflow n8n v1
