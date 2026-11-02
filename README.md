# Microsoft Teams Company Communicator — implementação na Casa Flora


[![Capa da implantação do Company Communicator na Casa Flora](linkedin-cover-company-communicator-casa-flora.jpg)](linkedin-cover-company-communicator-casa-flora.jpg)

[Prévia para o LinkedIn](https://soteropolitano.github.io/microsoft-teams-apps-company-communicator/linkedin-preview-v2/)

Participei da implantação do **Microsoft Teams Company Communicator** na **Casa Flora**. Deixei aqui o que fiz na parte técnica e a documentação do template usado.

A ideia era criar e enviar comunicados internos pelo Teams, complementando os canais que a empresa já usava. Atuei na implementação, configuração, validação, suporte à operação e adoção pelas áreas envolvidas.

> Este é um fork do template open source originalmente mantido pela Microsoft.
> Informações sensíveis, nomes de usuários, identificadores do tenant,
> credenciais e configurações internas da Casa Flora não fazem parte deste
> repositório.

## O que fiz

- Preparação e implantação dos aplicativos do Company Communicator no
  **Microsoft Teams**, contemplando a experiência de autores e destinatários.
- Configuração dos aplicativos no ambiente de **Teams Apps** da organização.
- Configuração do **Azure Bot** utilizado pela solução para interação e entrega
  das mensagens no Teams.
- Integração da aplicação com o ambiente **Microsoft 365 e Azure**.
- Validação do fluxo de criação, pré-visualização e envio de comunicados.
- Apoio técnico à operação e à adoção da ferramenta pelas áreas usuárias.
- Troubleshooting durante a implantação, com verificação das configurações do
  aplicativo, do bot, das permissões e dos componentes hospedados no Azure.

## Visão da solução

```mermaid
flowchart LR
    A[Autores no Microsoft Teams] --> B[Company Communicator]
    B --> C[Aplicação hospedada no Azure]
    C --> D[Azure Bot]
    D --> E[Microsoft Teams]
    E --> F[Colaboradores e grupos destinatários]
```

Os componentes ficaram assim:

| Camada | Papel na implementação |
| --- | --- |
| Microsoft Teams | Interface utilizada pelos autores e canal de entrega aos destinatários |
| Teams Apps | Publicação e disponibilização dos pacotes da aplicação no ambiente corporativo |
| Azure Bot | Comunicação entre a aplicação e os usuários do Teams |
| Microsoft Azure | Hospedagem e execução dos componentes de aplicação do template |
| Microsoft 365 | Identidade, permissões e integração com o ambiente corporativo |

## Resultado profissional

A solução ficou em funcionamento no Teams para apoiar os comunicados internos. Foi uma aplicação prática de infraestrutura e sustentação com Microsoft 365, Teams, Azure, identidade, permissões e diagnóstico de aplicações.

## Tecnologias usadas

`Microsoft Teams` · `Teams Apps` · `Microsoft Azure` · `Azure Bot` ·
`Microsoft 365` · `identidade e permissões` · `implantação` · `troubleshooting` ·
`documentação` · `adoção de solução`

## Sobre o template original

Abaixo mantive a documentação original do **Company Communicator App Template**, com os créditos e termos legais. Essa parte descreve o template da Microsoft, não uma autoria minha.

---

## Company Communicator App Template

[Architecture](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Solution-overview) | [Documentation](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki) | [Deployment guide powershell](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Deployment-guide-powershell)  |[Deployment guide](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Deployment-guide) | [User manual](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/User-manual) |
| ---- | ---- | ---- | ---- | ---- |

Company Communicator is a custom Teams app that enables corporate teams to create and send messages intended for multiple teams or large number of employees over chat allowing organization to reach employees right where they collaborate. Use this template for multiple scenarios, such as new initiative announcements, employee onboarding, modern learning and development, or organization-wide broadcasts.

The app provides an easy interface for designated users to create, preview, collaborate and send messages. It's also a foundation for building custom targeted communication capabilities, such as custom telemetry on how many users acknowledged or interacted with a message.

![Company Communicator compose message screen](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/images/company-communicator-compose.png)

## Key features

* **Message creation:** Easily create messages by using a team tab where team members who are permissioned can collaborate and create messages.
* **Audience selection:** Pick from four options to target audience. Send to general channel of selected teams, send in 1:1 chat to members of selected teams, send to all users who have the app installed or send to M365 groups, distribution lists or security groups.
* **Message metrics:** Export messages delivery report.
* **Localization:** Supports multiple locales.
* **Accessibility Compliant:** Company Communicator v5.4.1 is in compliant with Microsoft accessibility standards for Web, Windows and Mac OS.
* **Feedback:** Submit your feedback to the product team.

## Get started

Begin with the [Solution overview](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Solution-overview) to read about what the app does and how it works.

When you're ready to try out Company Communicator, or to use it in your own organization, you can choose to follow one of the below guides.
* [Deployment guide powershell](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Deployment-guide-powershell).
    * **Recommended** Use this option to deploy the latest version of Company Communicator using powershell script. The entire set-up is done by the powershell script.
* [Deployment guide](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Deployment-guide).
    * Use this option to deploy the latest version of Company Communicator with client secrets.
* [Deployment guide certificate](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Deployment-guide-certificate).
    * Use this option to deploy the latest version of Company Communicator with certificates.

## Migration

If you already have older version of Company Communicator installed, then please use this [v5 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v5-migration-guide). Please note that deploying the major version update, like the latest version of Company Communicator involves more than syncing the App Service and Azure Functions, so plan to review the migration guide before migrating to latest.

Migrating to newer versions.

 * [v5 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v5-migration-guide)
 * [v4 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v4-migration-guide)
 * [v3 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v3-migration-guide)
 * [v2 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v2-migration-guide)

## Feedback

Thoughts? Questions? Ideas? Share them with us [here](https://aka.ms/M365CCFeedback)

Please report bugs and other code issues [here](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/issues/new).

## Legal notice

This app template is provided under the [MIT License](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/blob/main/LICENSE) terms.  In addition to these terms, by using this app template you agree to the following:

- You, not Microsoft, will license the use of your app to users or organization.

- This app template is not intended to substitute your own regulatory due diligence or make you or your app compliant with respect to any applicable regulations, including but not limited to privacy, healthcare, employment, or financial regulations.

- You are responsible for complying with all applicable privacy and security regulations including those related to use, collection and handling of any personal data by your app. This includes complying with all internal privacy and security policies of your organization if your app is developed to be sideloaded internally within your organization. Where applicable, you may be responsible for data related incidents or data subject requests for data collected through your app.

- Any trademarks or registered trademarks of Microsoft in the United States and/or other countries and logos included in this repository are the property of Microsoft, and the license for this project does not grant you rights to use any Microsoft names, logos or trademarks outside of this repository. Microsoft’s general trademark guidelines can be found [here](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general.aspx).

- If the app template enables access to any Microsoft Internet-based services (e.g., Office365), use of those services will be subject to the separately-provided terms of use. In such cases, Microsoft may collect telemetry data related to app template usage and operation. Use and handling of telemetry data will be performed in accordance with such terms of use.

- Use of this template does not guarantee acceptance of your app to the Teams app store. To make this app available in the Teams app store, you will have to comply with the [submission and validation process](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/appsource/publish), and all associated requirements such as including your own privacy statement and terms of use for your app.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
