# Intention Classifier Flow — n8n

## Nodes
1. Webhook → mensagem do cliente
2. IA Model → classificador de intenção
3. Switch:
   - DELIVERY → DeliveryFlow
   - CARDÁPIO → MenuFlow
   - INFORMAÇÕES → InfoFlow
   - RESERVA → ReservaFlow
   - ELSE → Mensagem padrão
