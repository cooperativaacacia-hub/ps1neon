# PS1NEON — status do núcleo alternativo

Atualizado em 2026-09-07.

## Resultado atual

A página isolada `PS1NEON-core-test.html` foi aberta no celular com o núcleo PCSX ReARMed/EmulatorJS.

### Confirmado

- BIOS própria carregada;
- jogo BIN carregado;
- vídeo iniciado sem tela preta;
- menu do PlayStation exibido;
- controles touchscreen exibidos;
- botões de ação, START e SELECT disponíveis;
- jogo Yu-Gi-Oh! executado no navegador.

### Ainda pendente

- validar save real dentro de um jogo com suporte a Memory Card;
- fechar e reabrir o jogo;
- confirmar recuperação do progresso;
- exportar o cartão funcional como `.mcr`;
- testar restauração do backup.

O jogo usado no teste atual não apresentou uma opção de salvamento acessível. O recurso **Save State** do emulador não conta como teste de Memory Card real.

## Decisão

O núcleo alternativo está aprovado apenas para teste de BIOS, vídeo e controles. Ele não deve substituir o núcleo principal do PS1NEON até a validação do Memory Card com um jogo legalmente obtido que tenha opção de salvamento.
