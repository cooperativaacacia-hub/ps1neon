# Sincronização em nuvem do PS1NEON

## Pasta de destino

Os backups do projeto serão organizados na pasta PS1NEON Backups do Google Drive do usuário. A página não deve enviar BIOS, jogos ou arquivos de terceiros para a nuvem.

## O que será sincronizado

- Memory Card virtual do usuário.
- Lista de jogos recentes, sem os arquivos dos jogos.
- Configurações da interface.
- Versão e data do backup.

## Formato

O backup local usa um arquivo JSON com o formato `PS1NEON-BACKUP-1`. O campo do cartão contém os dados do Memory Card em Base64. O backup não deve conter BIOS, BIN, CUE, ISO ou qualquer ROM.

## Fluxo planejado

1. Criar ou abrir o Memory Card virtual.
2. Salvar alterações localmente.
3. Gerar um backup completo.
4. Autenticar o usuário no serviço de nuvem.
5. Enviar o backup para uma pasta privada do PS1NEON.
6. Manter versões anteriores para recuperação.
7. Ao abrir o emulador em outro aparelho, listar os backups disponíveis.
8. Restaurar o backup escolhido somente depois da confirmação do usuário.

## Segurança

A sincronização deve usar autenticação OAuth, pasta privada e somente arquivos criados pelo PS1NEON. O jogo e a BIOS permanecem no aparelho do usuário. O projeto não deve publicar o cartão nem compartilhar a pasta com terceiros.

## Estado atual

A pasta de destino foi criada no Google Drive e o exportador/importador local já está preparado. A sincronização automática ainda depende de uma camada web autenticada; não deve ser simulada por um botão que apenas diga que sincronizou. O Memory Card também precisa ser conectado ao núcleo do emulador antes que os saves feitos dentro dos jogos sejam considerados válidos.
