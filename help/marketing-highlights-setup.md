---
title: Configurar destaques de marketing
description: Saiba como conectar o Marketo ao Sales Qualifier para que os representantes possam visualizar e filtrar prospetos por atividade em tempo real do Marketo em Destaques de marketing.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 17bfe0a1ce9b289ed85af0f72ddd089b11cca875
workflow-type: tm+mt
source-wordcount: 675
ht-degree: 3%

---


# Configurar destaques de marketing

Destaques de marketing mostra a atividade [!DNL Marketo] ativa de cada cliente potencial, como aberturas e cliques de email, visitas à Web e preenchimentos de formulário. Este artigo explica como conectar sua instância [!DNL Marketo] para que a atividade flua para dentro.

>[!IMPORTANT]
>
>A conclusão desta instalação requer acesso à Adobe Developer Console e ao **[!UICONTROL Administrador]** em [!DNL Marketo]. Trabalhe com seu contato da Adobe e com seu administrador do [!DNL Marketo] para concluir as quatro partes abaixo.

A instalação tem quatro partes:

* Parte A: Criar credenciais de API na Adobe Developer Console.
* Parte B: Obtenha seus identificadores e endpoint do Sales Qualifier.
* Parte C: Configurar um webhook no [!DNL Marketo Engage].
* Parte D: adicionar o webhook a um acionador de Campanha inteligente.

Após a conclusão da instalação, os usuários verão e filtrarão esta atividade em **[!UICONTROL Clientes potenciais]** > **[!UICONTROL Destaques de marketing]**.

## Parte A: Criar credenciais de API {#part-a-create-api-credentials}

Essas credenciais permitem que o [!DNL Marketo] se autentique com segurança no Sales Qualifier.

Para criar as credenciais:

1. Acesse o [Adobe Developer Console](https://developer.adobe.com/console/) e faça logon com seu Adobe ID.
1. Selecione **[!UICONTROL Criar novo projeto]** ou abra um projeto existente.
1. Selecione **[!UICONTROL Editar projeto]**, renomeie o projeto para algo identificável, como `Sales Qualifier Marketing Highlights`, e selecione **[!UICONTROL Salvar]**.
1. Selecione **[!UICONTROL Adicionar API]**, selecione **[!UICONTROL API Experience Platform]** e **[!UICONTROL Avançar]**.
1. Escolha **[!UICONTROL OAuth Server-to-Server]** como o tipo de autenticação e selecione **[!UICONTROL Avançar]**.

   O **[!UICONTROL OAuth Server-to-Server]** permite que o [!DNL Marketo] chame a API do Sales Qualifier diretamente do servidor, sem exigir que uma pessoa entre.

1. Insira um nome de credencial com 45 caracteres ou menos, como `Sales Qualifier Marketing Highlights Creds`.
1. Selecione o perfil de produto a ser associado e selecione **[!UICONTROL Salvar API configurada]**.
1. Em **[!UICONTROL Credenciais conectadas]**, abra a credencial **[!UICONTROL servidor para servidor OAuth]**. Selecione **[!UICONTROL Recuperar segredo do cliente]** e copie a **[!UICONTROL ID do Cliente]** e o **[!UICONTROL Segredo do Cliente]**. Você usa estes valores na [Parte C](#part-c-configure-the-marketo-webhook).

>[!WARNING]
>
>Mantenha o segredo do cliente privado. Tratá-la como uma senha e não enviá-la por email. Use o canal seguro aprovado da sua organização para compartilhá-lo com quem configurar o webhook.

## Parte B: Coletar endpoint e identificadores {#part-b-gather-your-endpoint-and-identifiers}

Você precisa de três valores para a [Parte C](#part-c-configure-the-marketo-webhook):

* **URL do Ponto de Extremidade** — O endereço do webhook do Sales Qualifier para sua região.
* **imsOrg ID** — O identificador da sua organização no Adobe Identity Management System (IMS), no formato `{ORG_ID}@AdobeOrg`.
* **Nome da sandbox** — O nome da sandbox do AEP exatamente como aparece no URL do Sales Qualifier (o valor `sname`), não o nome de exibição mostrado na interface. Use o valor de URL em minúsculas, por exemplo `prod`, não `Prod`.

| Região | URL do ponto de extremidade do Webhook |
| --- | --- |
| América do Norte | `https://5r6xakp9k3.execute-api.us-east-1.amazonaws.com/prod/external/marketo/signals` |
| EMEA | `https://pc72i8q1k3.execute-api.eu-west-1.amazonaws.com/prod/external/marketo/signals` |
| APAC / Austrália | `https://5cxxxyqlai.execute-api.ap-southeast-2.amazonaws.com/prod/external/marketo/signals` |

{style="table-layout:auto"}

Se você não tiver certeza da sua região, ID imsOrg ou nome da sandbox, o contato da Adobe poderá confirmá-los.

## Parte C: Configurar o webhook do Marketo {#part-c-configure-the-marketo-webhook}

Para criar o webhook:

1. Em [!DNL Marketo], selecione **[!UICONTROL Admin]** > **[!UICONTROL Webhooks]**.
1. Selecione **[!UICONTROL Novo Webhook]**.
1. Defina a **[!UICONTROL URL]** para a URL do ponto de extremidade da sua região da [Parte B](#part-b-gather-your-endpoint-and-identifiers).
1. Definir **[!UICONTROL Tipo de Solicitação]** como `POST`.
1. Defina **[!UICONTROL Solicitar Codificação de Token]** para `JSON`. Esta configuração é obrigatória.
1. Cole o modelo de conteúdo abaixo no **[!UICONTROL Modelo]**. Use o **[!UICONTROL Token de Inserção]** de [!DNL Marketo] para corresponder aos nomes de campo na sua instância.

   >[!NOTE]
   >
   >Com a codificação JSON, não coloque os tokens de sequência entre aspas. [!DNL Marketo] os adiciona automaticamente.

   ```json
   {
     "leadId": {{lead.Id:default=0}},
     "email": {{lead.Email Address:default=}},
     "fullName": {{lead.Full Name:default=}},
     "company": {{company.Company Name:default=}},
     "title": {{lead.Job Title:default=}},
     "department": {{lead.Department:default=}},
     "country": {{lead.Country:default=}},
     "score": {{lead.Lead Score:default=0}},
     "rating": {{lead.Lead Rating:default=}},
     "leadStatus": {{lead.Lead Status:default=}},
     "leadSource": {{lead.Lead Source:default=}},
     "isCustomer": {{lead.Is Customer:default=false}},
     "industry": {{company.Industry:default=}},
     "annualRevenue": {{company.Annual Revenue:default=0}},
     "numEmployees": {{company.Num Employees:default=0}},
     "campaignId": {{campaign.id:default=0}},
     "campaignName": {{campaign.name:default=}},
     "programName": {{program.name:default=}},
     "occurredAt": {{system.dateTime:default=}},
     "munchkinId": {{system.munchkinId:default=}},
     "triggerName": {{trigger.Trigger Name:default=}},
     "crmId": {{lead.SFDC ID:default=}},
     "crmType": {{lead.SFDC Type:default=}},
     "crmOwnerEmail": {{lead.Lead Owner Email Address:default=}},
     "crmOwnerFirstName": {{lead.Lead Owner First Name:default=}},
     "crmOwnerLastName": {{lead.Lead Owner Last Name:default=}},
     "attributes": {
       "asset": {{trigger.Name:default=}},
       "link": {{trigger.Link:default=}},
       "subject": {{trigger.Subject:default=}},
       "webPage": {{trigger.Web Page:default=}},
       "category": {{trigger.Category:default=}},
       "details": {{trigger.Details:default=}},
       "sentBy": {{trigger.Sent By:default=}},
       "receivedBy": {{trigger.Received By:default=}},
       "referrer": {{trigger.Referrer:default=}},
       "searchEngine": {{trigger.Search Engine:default=}},
       "searchQuery": {{trigger.Search Query:default=}},
       "imDescription": {{lead.Last Interesting Moment Desc:default=}},
       "imType": {{lead.Last Interesting Moment Type:default=}},
       "imDate": {{lead.Last Interesting Moment Date:default=}},
       "imSource": {{lead.Last Interesting Moment Source:default=}},
       "chatAgentName": {{trigger.Agent Name:default=}},
       "chatAgentEmail": {{trigger.Agent Email:default=}},
       "chatConversationStatus": {{trigger.Conversation Status:default=}},
       "chatConversationSummary": {{trigger.Conversation Summary:default=}},
       "chatGoalName": {{trigger.Goal name:default=}},
       "chatMeetingStatus": {{trigger.meeting status:default=}},
       "chatScheduledFor": {{trigger.Scheduled For:default=}},
       "chatDocumentName": {{trigger.Document Name:default=}},
       "chatDocumentUrl": {{trigger.Document URL:default=}},
       "chatPageUrl": {{trigger.Page URL:default=}}
     }
   }
   ```

1. Selecione **[!UICONTROL Ações do Webhook]** > **[!UICONTROL Definir Cabeçalho Personalizado]** e adicione os seguintes cabeçalhos, usando os valores da [Parte A](#part-a-create-api-credentials) e da [Parte B](#part-b-gather-your-endpoint-and-identifiers):

   | Header | Valor |
   | --- | --- |
   | `Content-Type` | `application/json` |
   | `x-client-id` | Sua ID do cliente |
   | `x-client-secret` | Segredo do cliente |
   | `x-gw-ims-org-id` | Sua ID imsOrg |
   | `x-sandbox-name` | O nome da sua sandbox |

   {style="table-layout:auto"}

1. Selecione **[!UICONTROL Salvar]**.

## Parte D: Adicionar o webhook a um acionador de Campanha inteligente {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

Adicione uma etapa de fluxo do **[!UICONTROL Webhook de chamada]** para acionar uma Campanha Inteligente, existente ou nova. Os acionadores da Smart List nessa campanha decidem quais atividades são enviadas para o Sales Qualifier.

Para adicionar o webhook:

1. Abra uma Campanha Inteligente de acionador existente ou crie uma nova (**[!UICONTROL Atividades de Marketing]** > **[!UICONTROL Novo]** > **[!UICONTROL Campanha Inteligente]**).
1. Na guia **[!UICONTROL Smart List]**, adicione o(s) acionador(es) para as atividades que deseja enviar, por exemplo **[!UICONTROL Link de Cliques no Email]**, **[!UICONTROL Preenche o Formulário]** ou **[!UICONTROL Página da Web de Visitas]**.
1. Na guia **[!UICONTROL Fluxo]**, adicione a etapa **[!UICONTROL Chamar Webhook]** e selecione o webhook criado na [Parte C](#part-c-configure-the-marketo-webhook).
1. Ative a Campanha inteligente.

A atividade dessa Campanha inteligente agora flui para o Sales Qualifier. Os representantes veem e filtram esta atividade em **[!UICONTROL Clientes potenciais]** > **[!UICONTROL Destaques de marketing]**.

>[!MORELIKETHIS]
>
>* [Gerenciar integrações](integrations.md)
>* [Clientes Potenciais](prospects.md)
>* [Introdução](getting-started.md)
