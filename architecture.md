# 🏗️ Arquitetura — PizzariaBot

## 🧩 Visão Geral

O sistema possui 5 camadas:

1. **Entrada** → WhatsApp / API / Webhook  
2. **Classificação** → IA identifica intenção  
3. **RAG** → Recupera dados do cardápio  
4. **Agente Delivery** → Conduz conversa  
5. **Camada de Execução** → Pagamento, Cozinha, Entrega  

---

## 🔄 Fluxo Completo

1. Cliente envia mensagem  
2. Classificador → (Delivery/Cardápio/Info/Reserva)  
3. Vem para o agente correto  
4. IA consulta cardápio (embeddings locais)  
5. Carrinho é montado e salvo no Redis  
6. Quando finaliza:  
   - Solicita endereço  
   - Valida endereço via Google Maps  
   - Mostra total final  
   - Pergunta pagamento  
   - Gera pedido  
7. Envia cópia à cozinha e à entrega  

---

## 🧠 IA Envolvida

### 1. Classificador
Prompt: `prompts/classifier_prompt.txt`

### 2. Agente Delivery
- entende pedidos
- realiza upsell
- monta carrinho
- exibe total

### 3. RAG
- usa o JSON do cardápio em `/docs/cardapio.json`
- embeddings locais
- consultas sem alucinação

---

## 🗄 Banco de Dados

### Redis (Upstash)
- carrinho
- sessões
- clientes
- histórico curto

### Supabase (opcional)
- pedidos históricos  
- dados avançados  

---

## ☁️ Infra
- n8n rodando em VPS, Railway ou Node  
- Mercado Pago API  
- Google Maps Geocode  

---

## 🧱 Escalabilidade
- Multi-tenancy simples  
- Fluxos independentes  
- Modular e fácil de replicar  
