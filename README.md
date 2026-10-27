# Disputa de Pênaltis

Jogo de disputa de pênaltis feito em HTML, CSS e JavaScript puro (canvas), num único arquivo, `index.html`.

**Jogar:** https://lucaslima223.github.io/disputa-de-penaltis/

## Como jogar

- **Batendo:** toque no gol para mirar e pare a barra de precisão no verde. Quanto mais perto do centro, mais certeira a batida.
- **No gol:** escolha onde pular antes do chute.
- Cinco cobranças para cada lado, alternando. Se empatar, vai para as cobranças alternadas até alguém errar.

## Modos

- **Online, 2 jogadores:** um jogador cria a partida e recebe um código de 4 letras; o outro abre o mesmo link e entra com o código. Não precisa de conta.
- **Contra a CPU:** cada cobrador da CPU tem um “relatório” com o canto preferido.

## Como funciona o online

No GitHub Pages (ou em qualquer site), os dois navegadores trocam mensagens por WebSocket através de servidores MQTT públicos e gratuitos ([EMQX](https://www.emqx.com/en/mqtt/public-mqtt5-broker) e [HiveMQ](https://www.hivemq.com/mqtt/public-mqtt-broker/)), usando a biblioteca [MQTT.js](https://github.com/mqttjs/MQTT.js) carregada do jsDelivr. O jogo publica nos dois servidores ao mesmo tempo, então basta um deles funcionar. Cada partida usa um canal com o código de 4 letras. Como os servidores são públicos, não coloque informações pessoais no apelido.

Quando o jogo é aberto como artefato no Claude (claude.ai), ele usa a sincronização própria do Claude no lugar dos servidores MQTT.

Cada jogador envia só a própria jogada (onde chutou ou para onde pulou), e os dois aparelhos calculam o resultado da cobrança com a mesma regra, então o placar fica igual nos dois lados.

## Rodando localmente

Basta abrir o `index.html` no navegador. Não há etapa de build.
