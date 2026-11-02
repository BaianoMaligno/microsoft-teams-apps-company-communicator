# Scripts de diagnóstico

Esta pasta vem do projeto original do Company Communicator. Os scripts ajudam a conferir problemas de implantação no tenant. Não são uma prova de que a instalação da Casa Flora usa exatamente esta configuração.

## `Start-ChatWithUser.ps1`

Testa o chat do bot dentro do Teams. Antes de usar, preencha as variáveis na seção “Variables need to be replaced to start using the script”:

- `$tenantId`: domínio do tenant, como `tenant.onmicrosoft.com`, ou GUID.
- `$teamsAppId`: AppId do manifesto do aplicativo Teams.
- `$graphAppId`: AppId da aplicação Graph.
- `$userAppId`: AppId da aplicação de usuário.

Para os segredos, a orientação original é criar um segredo temporário por aplicação e removê-lo após o teste. Assim, o teste não depende de substituir os segredos já usados pela aplicação. Não salve credenciais reais no repositório nem compartilhe a saída com tokens.

## `Check-AppRegistrations.ps1`

Confere se as App Registrations e os segredos armazenados no Key Vault funcionam juntos. Receber um access token indica que a combinação de AppId e segredo foi aceita. Isso, sozinho, não valida todo o envio de mensagens.

## `Check-GraphApp.ps1`

É uma verificação mais simples da aplicação Graph. Confere AppId, segredo e permissões de API para consultar grupos e usuários. Use quando a dúvida estiver nessa combinação, sem precisar executar o diagnóstico completo.
