# Teste de núcleo PS1 com Memory Card

Esta página de teste não substitui o núcleo atual do PS1NEON.

## Núcleo preservado

O núcleo atual baseado no WASMPSX continua sendo a referência porque já abriu BIN e foi validado visualmente no celular. Ele não expõe uma interface pública clara para inserir ou retirar um Memory Card virtual.

## Núcleo candidato

O EmulatorJS documenta os núcleos `pcsx_rearmed` e `mednafen_psx_hw` para o sistema PlayStation. O candidato principal para o teste é `pcsx_rearmed`, por possuir suporte conhecido a Memory Cards no ecossistema PCSX.

## Critérios de aprovação

- BIOS própria e legalmente obtida inicia sem tela preta.
- Jogo BIN inicia com vídeo e áudio.
- CUE/BIN continua funcionando quando aplicável.
- Controles touchscreen continuam funcionando.
- Um Memory Card de 128 KB é reconhecido no jogo.
- O jogo grava um progresso real no cartão.
- O emulador fecha e abre novamente.
- O progresso é carregado do mesmo cartão.
- O cartão pode ser exportado como `.mcr`.
- O backup pode ser restaurado sem enviar BIOS ou jogos.

## Regra de integração

O núcleo atual não será removido antes de todos os critérios serem aprovados. A interface PS1NEON, a biblioteca, o backup local e a estrutura da nuvem devem continuar funcionando independentemente do núcleo escolhido.
