# RAG Delivery Flow — n8n

Nodes:
1. Memory Load (Redis)
2. Vector Store → embeddings do cardápio
3. IA Model → prompt de delivery
4. Function → interpretação do pedido
5. Update Carrinho (Redis)
6. Response → cliente
