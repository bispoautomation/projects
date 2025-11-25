# 🍕 PRD — PizzariaBot

## 🎯 Objetivo
Construir o bot de atendimento mais completo e inteligente para pizzarias, restaurantes e hambúrguerias usando IA + n8n + automação.

---

## 🧩 Problema
Atendimentos manuais são lentos, imprecisos e sem histórico.  
Restaurantes perdem vendas porque cada atendente trabalha de um jeito.

---

## 💡 Solução Proposta
Um bot com fluxo natural, inteligente e 100% configurável que:

- Entende a intenção do cliente
- Consulta cardápio real via RAG
- Responde de forma humana e contextual
- Mantém carrinho inteligente
- Gera total da compra
- Solicita endereço
- Integra com Google Maps
- Processa pagamento via Mercado Pago
- Envia pedidos para cozinha e entrega

---

## 🛠 Escopo Funcional

### 1. Classificação da intenção
Categorias:
- DELIVERY
- CARDÁPIO
- INFORMAÇÕES
- RESERVA
- NÃO IDENTIFICADO

### 2. RAG com JSON do cardápio
- Recuperação de itens
- Descrição detalhada
- Preço
- Upsell automático

### 3. Carrinho inteligente
- Múltiplos itens
- Edição do carrinho
- Remoção
- Total dinâmico

### 4. Endereço
- Solicitação do endereço
- Validação
- Extração automática
- Conversão para latitude/longitude
- Passagem para o motoboy

### 5. Pagamento
- Mercado Pago Checkout
- Pix (opcional)
- Confirmação automática

### 6. Cozinha
- Envio de pedido final
- Lista de itens
- Observações
- Endereço
- Pagamento escolhido

---

## 🧱 Requisitos Não-Funcionais
- Baixo custo por interação
- Zero alucinação
- Estrutura modular
- Logs completos
- Fluxo sem travamentos

---

## 📊 Métricas
- N° de pedidos por dia
- Conversão em vendas
- Ticket médio
- Tempo médio por pedido

---

## 🧪 MVP
- [ ] Classificador  
- [ ] RAG do cardápio  
- [ ] Carrinho básico  
- [ ] Endereço  
- [ ] Pagamento  
- [ ] Cozinha  
