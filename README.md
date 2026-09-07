# PS1NEON

PS1NEON é um emulador real de PlayStation 1 para navegador, com interface neon e controles para teclado e telas sensíveis ao toque.

## Estado atual

O projeto usa um núcleo de emulação PlayStation em JavaScript e WebAssembly. O arquivo `PlayStation.js` precisa permanecer no mesmo diretório das páginas HTML para que o núcleo seja carregado corretamente.

O formato comprovado atualmente é `.bin`. O carregamento de `.cue` foi preparado para localizar o arquivo BIN correspondente quando os dois arquivos são selecionados juntos. O formato `.iso` ainda não é executado diretamente pelo núcleo atual; para maior compatibilidade, converta o jogo para BIN/CUE.

O usuário precisa fornecer uma BIOS de PlayStation obtida legalmente e seus próprios jogos obtidos legalmente. O projeto não distribui BIOS nem jogos comerciais.

## Interface

A interface possui identidade visual escura com detalhes neon, tela de carregamento, renderização do jogo, áudio, modo de tela cheia e controles para toque.

Os botões virtuais seguem a disposição tradicional do controle PlayStation:

```text
             △
       □           ○
             ×
```

O direcional fica separado à esquerda. START e SELECT ficam na região central, afastados do seletor de arquivos. No computador, o teclado físico continua disponível através do mapeamento do núcleo original.

## Arquivos

- `index.html`: página inicial do projeto.
- `PS1NEON.html`: interface principal personalizada.
- `PS1NEON-mobile.html`: versão atualizada para touchscreen, com seleção de BIN, CUE e ISO.
- `PlayStation.js`: núcleo PlayStation em JavaScript/WebAssembly.

## Como usar

Abra a página por um servidor web ou pela hospedagem do projeto. Selecione uma BIOS válida quando solicitado e carregue um arquivo BIN. Para um jogo CUE, selecione o CUE e o BIN correspondente juntos. Não abra o HTML diretamente pelo gerenciador de arquivos do celular, pois o navegador pode bloquear recursos WebAssembly e gerar uma tela preta.

## Próximas etapas

As próximas etapas são finalizar o suporte a CUE com múltiplas faixas, melhorar o tratamento de erros, validar áudio de CD, ajustar o tamanho dos controles em diferentes telas, adicionar pausa, reinício, volume, biblioteca de jogos, favoritos, histórico, cartões de memória virtuais e estados de salvamento. Depois da estabilização da versão web, será preparada uma versão APK Android.

## Compatibilidade e testes

Cada alteração deve ser testada preservando o carregamento BIN já validado. A prioridade é evitar tela preta e manter o núcleo original funcionando. Compatibilidade universal com todos os jogos, formatos e celulares não deve ser presumida sem teste individual.
