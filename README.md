# projects# 🍕 PizzariaBot — Atendimento Inteligente com IA + n8n + RAG

O PizzariaBot é um sistema completo para atendimento automatizado de restaurantes via WhatsApp e API, utilizando:

- Classificador de intenção (Delivery, Cardápio, Informações, Reserva)
- IA com RAG baseado no cardápio
- Carrinho inteligente com múltiplos itens
- Histórico do cliente via Redis
- Geolocalização do endereço
- Integração com Mercado Pago
- Copia de pedido para cozinha e entrega
- Fluxos completos em n8n

---

## 🚀 Objetivo
Automatizar atendimento de restaurantes de forma natural, rápida, inteligente e com upsell automático.

---

## 🧠 Funcionalidades Principais

✔ Classificação da intenção  
✔ Envio de cardápio dinâmico  
✔ RAG baseado no JSON do cardápio  
✔ Carrinho inteligente multi-itens  
✔ Pedido e confirmação do cliente  
✔ Captura e validação de endereço  
✔ Geolocalização Google Maps  
✔ Pagamento Mercado Pago  
✔ Histórico via Redis (Upstash)  
✔ Notificações para cozinha e entrega  

---

## 📐 Arquitetura
Veja `architecture.md`.

---

## 🔄 Fluxos n8n
Disponíveis em `/workflows/`:

- intention-classifier.md  
- rag-delivery-flow.md  
- carrinho-flow.md  
- pagamento-flow.md  
- reserva-flow.md  

---

## 📊 Banco de Dados
- Redis para sessão/carrinho  
- Supabase para pedidos históricos  

Modelo em `docs/data-model.md`.

---

## 📦 Instalação
1. Configure ambiente do n8n (>= v1.89.2)  
2. Importe os fluxos  
3. Configure:
   - UPSTASH_REDIS_URL  
   - OPENAI_API_KEY  
   - MERCADO_PAGO_KEY  
4. Suba o cardápio em `docs/cardapio.json`

---

## 📞 Autor
**Diogo Bispo**  
IA • n8n • Automação • RAG • SaaS • WhatsApp Bots
