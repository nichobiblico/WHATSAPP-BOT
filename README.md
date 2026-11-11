# Prévia mobile de conversa no WhatsApp

Prévia vertical em estilo WhatsApp. Em telas grandes, fica centralizada na proporção de um celular; em celulares, ocupa a tela inteira sem moldura.

## Abrir

Use [http://localhost:5173](http://localhost:5173) com o servidor local ativo. Para iniciar o servidor novamente, rode `node server.js` nesta pasta. Também é possível abrir `index.html` diretamente no navegador.

## Idiomas e rotas

- `/mexico` abre a conversa em espanhol mexicano.
- `/pt` e `/brasil` abrem a versão em português do Brasil.
- A raiz `/` continua abrindo a versão mexicana.
- Os planos brasileiros usam os links da ZuckPay: 1 mês (R$ 9,90), 3 meses (R$ 14,90) e 1 ano (R$ 17,90).
- Os parâmetros `utm_*` da URL da página são encaminhados ao checkout escolhido, incluindo valores repetidos de um mesmo parâmetro.

## Personalizar

Edite `MEXICO_CHAT_CONFIG` ou `BRAZIL_CHAT_CONFIG`, no início de `app.js`:

- `profile.name`, `profile.status` e `profile.avatarUrl` definem o cabeçalho.
- `conversation` contém as mensagens exibidas em sequência. Mensagens do bot aparecem com animação de digitação.
- `options` define as opções clicáveis que aparecem depois da conversa. Deixe vazio até definir as escolhas.
- `pauseBeforeReply` ajusta quanto tempo os três pontinhos aparecem antes da mensagem completa.

