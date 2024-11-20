#Bot de Atualização de Preço do Bitcoin no Discord

Este bot para Discord foi desenvolvido para enviar atualizações periódicas sobre o preço do Bitcoin e suas variações ao longo de diferentes períodos (24 horas, 7 dias e 30 dias). Ele utiliza as APIs do Binance e CoinGecko para obter os dados mais recentes.

Funcionalidades
Atualização do preço do Bitcoin: Busca o preço atual do Bitcoin.
Variações de preço: Calcula as variações do preço ao longo dos últimos 1, 7 e 30 dias.
Mensagens automáticas: Envia mensagens periódicas em um canal específico no Discord.
Configuração personalizável: Intervalo de atualização e canal de envio podem ser ajustados.

Tecnologias Utilizadas:
Node.js
Discord.js: Interação com a API do Discord.
Node-Fetch: Para realizar chamadas HTTP às APIs externas.

APIs Utilizadas:
Binance API: Para buscar o preço atual do Bitcoin.
CoinGecko API: Para obter as variações de preço.

Configuração
Pré-requisitos
Node.js instalado na sua máquina.
Um bot configurado no Discord com o token disponível.
Permissões para o bot enviar mensagens no canal especificado.
Variáveis e Configuração

Token do bot Discord:
Defina a constante TOKEN com o token do seu bot no Discord.

ID do canal:
Altere a constante CHANNEL_ID com o ID do canal onde o bot enviará as mensagens.

Intervalo de atualização:
Ajuste a constante UPDATE_INTERVAL para definir o intervalo de atualização em milissegundos (o padrão é 1 hora).

Estrutura do Código
sendRegularUpdate(): Função principal que busca os dados de preço e variações, formata a mensagem e envia para o canal.
fetchCurrentPrice(): Obtém o preço atual do Bitcoin a partir da Binance API.
fetchPriceChanges(): Calcula as variações de preço ao longo de 1, 7 e 30 dias usando a CoinGecko API.
createPriceUpdateMessage(): Formata a mensagem para ser enviada no Discord.
formatCurrentPrice(): Formata o preço atual em um padrão monetário legível.
formatPriceChanges(): Gera as mensagens de variação de preço.
Exemplo de Mensagem no Discord
javascript

**Variação do preço do Bitcoin!**
**Variação atual:** $40,000.00
```diff
+ Últimas 24h: +2.50%
- Últimos 7 dias: -1.20%
+ Último mês: +5.00%
````

Limitações
O bot pode enfrentar limitações de taxa de requisições da API (rate limit) dependendo do volume de uso.
Certifique-se de que o bot possui permissões no canal configurado para enviar mensagens.
Contribuição
Sinta-se à vontade para contribuir! Sugestões, melhorias e correções são bem-vindas. Abra um pull request ou envie uma issue.

Licença
Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.

Se precisar de ajuda adicional, entre em contato! 
