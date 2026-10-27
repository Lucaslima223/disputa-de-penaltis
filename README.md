# Disputa de Pênaltis

Jogo de disputa de pênaltis feito em HTML, CSS e JavaScript puro (canvas), num único arquivo, `index.html`.

## Como jogar

- **Batendo:** toque no gol para mirar e pare a barra de precisão no verde. Quanto mais perto do centro, mais certeira a batida.
- **No gol:** escolha onde pular antes do chute.
- Cinco cobranças para cada lado, alternando. Se empatar, vai para as cobranças alternadas até alguém errar.

## Modos

- **Contra a CPU:** funciona em qualquer navegador, inclusive no GitHub Pages. Cada cobrador da CPU tem um “relatório” com o canto preferido.
- **Online, 2 jogadores:** um jogador cria a partida e recebe um código de 4 letras; o outro entra com o código. A sincronização usa a capacidade `room` dos artefatos publicados no Claude (claude.ai), então o modo online só funciona com o jogo aberto lá, com os dois jogadores logados. Fora do Claude, o jogo mostra só o modo contra a CPU.

## Rodando localmente

Basta abrir o `index.html` no navegador. Não há dependências nem etapa de build.
