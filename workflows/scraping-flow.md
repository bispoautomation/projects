# Scraping Flow — n8n

## Nodes
1. Trigger → parâmetro de busca (nicho + cidade)
2. Function → gerar variações de termos
3. HTTP Request → Google Maps API
4. IF → páginas válidas
5. Function → extrair campos
6. Redis → checar duplicados
7. Supabase → inserir lead novo
8. Merge → próximos resultados
9. Export CSV (opcional)
