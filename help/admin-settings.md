---
title: Configurações de administração
description: Saiba como gerenciar campos do CRM, sincronização de atividades, recusa de email e outras configurações de administração do Sales Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/vbtO6I67ZEaZz3oio9InNErvq5D0wjbRxyDZpTq8Lzo'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
internal-label: Administration
source-git-commit: 08dd05e1d13b501d43d457e6217a43aaabdb1d0d
workflow-type: tm+mt
source-wordcount: 670
ht-degree: 0%

---


# Configurações de administração

Use as **[!UICONTROL Configurações de Administração]** para configurar as integrações de CRM, gerenciar o Centro de Conhecimento e configurar a recusa de email.

O Sales Qualifier se conecta ao Salesforce ou Microsoft Dynamics 365. A conexão fornece à Account Qualification Agent (AQA) uma visualização consistente de clientes potenciais, contas, contatos, atividades e proprietários. O Sales Qualifier também pode gravar atividades de alcance geral e status de recusa no CRM e sincronizar atividades de alcance geral com o Marketo.

Para configurar conexões do CRM, mapeamento de campos e sincronização de atividades, vá para **[!UICONTROL Administração]** > **[!UICONTROL Configurações de Administração]** > **[!UICONTROL Conexões do CRM]**. Os usuários padrão podem usar os dados e filtros do CRM configurados, mas não podem alterar essas configurações. Para conectar um CRM pela primeira vez, consulte [Introdução](getting-started.md#connect-your-crm).

>[!IMPORTANT]
>
>O acesso a **[!UICONTROL Configurações de Administrador]** requer associação aos grupos de usuários `Sales Qualifier` e `Sales Qualifier Admins`. Consulte [Funções e permissões de usuário](user-roles-permissions.md).

## MCP do CRM e o plug-in incorporado

O Sales Qualifier funciona com seu CRM das seguintes maneiras:

* **Consultas do MCP do CRM** — O Account Qualification Agent consulta dados do CRM ao vivo para que as respostas e os insights reflitam o estado atual de seus registros.
* **Plug-in incorporado** — o plug-in do CRM exibe [!DNL Marketo Sales Insights] insights e dados de agente no seu CRM. Use o plug-in para adicionar um cliente potencial ao Sales Qualifier.
* **Sincronização de atividade** — Quando um administrador ativa a **[!UICONTROL Sincronização de atividade]**, as atividades de alcance externo são sincronizadas com o CRM e o Marketo.

## Escopo de acesso do CRM

O Sales Qualifier lê usuários, contatos, mapeamentos de proprietários, clientes potenciais, contas, oportunidades e atividades do CRM. Ele grava no CRM somente atividades de alcance reportadas e status de recusa, e sincroniza atividades de alcance reportadas ao Marketo. Seu administrador de CRM prepara o acesso à API no Salesforce ou Dynamics. Em seguida, um administrador do Sales Qualifier conecta o CRM, mapeia campos de entrada e escolhe se deseja sincronizar atividades.

>[!NOTE]
>
>As etapas de credencial em [Introdução](getting-started.md#connect-your-crm) descrevem o acesso de leitura a objetos do CRM. Se você ativar a sincronização de atividades ou o cancelamento da gravação, peça ao administrador do CRM para conceder o acesso de gravação correspondente exigido pela configuração do CRM.

## Mapear campos do CRM (mapeamento de entrada)

Depois que o CRM estiver conectado, selecione **[!UICONTROL Gerenciar]** para a conexão e abra o **[!UICONTROL Mapeamento de entrada]**. O mapeamento de entrada controla quais campos do CRM o Qualificador de Vendas extrai para o aplicativo.

1. Selecione **[!UICONTROL Adicionar seção]**.
1. Insira um nome e uma descrição de seção.
1. Selecione um tipo de entidade. **[!UICONTROL Clientes potenciais]** está selecionado por padrão. **[!UICONTROL Contatos]**, **[!UICONTROL Contas]** e **[!UICONTROL Oportunidades]** também estão disponíveis.
1. Selecione os campos do CRM que serão importados.

   Cada linha de campo exibe seu **[!UICONTROL Nome de exibição]**, **[!UICONTROL Nome do campo]** e **[!UICONTROL Tipo de dados]**.

1. Ative **[!UICONTROL Filtrável]** para cada campo de cliente potencial, contato ou oportunidade que você deseja disponibilizar como filtro na lista **[!UICONTROL Clientes Potenciais]**.
1. Visualize a seção e selecione **[!UICONTROL Adicionar]**.

Os campos mapeados aparecem nas áreas correspondentes do Sales Qualifier:

* Os campos de cliente potencial aparecem na guia **[!UICONTROL Pessoa]**.
* Os campos de conta aparecem na guia **[!UICONTROL Conta]**.
* Os campos de oportunidade aparecem na seção **[!UICONTROL Oportunidade de conta]**. Os campos de oportunidade filtráveis também aparecem como suas próprias colunas em **[!UICONTROL Meus Contatos de Oportunidade]**, com rótulos como **[!UICONTROL Preparo (Oportunidade)]** para diferenciá-los dos campos de contato.

## Configurar a sincronização de atividades (mapeamento de saída)

1. Em **[!UICONTROL Conexões do CRM]**, selecione **[!UICONTROL Gerenciar]** para o CRM conectado.
1. Abra **[!UICONTROL Mapeamento de saída]**.
1. Ative a **[!UICONTROL Sincronização de atividade]** para sincronizar atividades de alcance da Sales Qualifier com o CRM e a Marketo. As atividades de email enviadas, abertas, clicadas e respondidas incluem o nome do Plano de Envolvimento.

Quando a sincronização de atividades está desativada, o Sales Qualifier continua a usar dados de entrada do CRM, mas não sincroniza atividades de alcance para o CRM ou o Marketo.

## Configurar opção de não participação de email global

1. Na navegação à esquerda, expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Configurações de Administração]**.
1. Selecione as **[!UICONTROL Configurações de email]** em **[!UICONTROL Conformidade]**.
1. Ative **[!UICONTROL Incluir link para opção de não participação em todos os emails]** para anexar um rodapé de cancelamento de inscrição a emails de saída.
1. Em **[!UICONTROL Modelo de mensagem de recusa]**, digite o texto do rodapé. Inclua o token `{opt_out_link}` no qual o link para cancelar inscrição deve aparecer.

As configurações são salvas automaticamente.

Quando um cliente potencial seleciona o link, o Sales Qualifier interrompe o envio de emails para esse cliente potencial e sincroniza o status de recusa para o CRM conectado.

## Referência: amostra de parâmetros da API

Sua equipe de CRM pode usar esses exemplos para confirmar os retornos de acesso de leitura dos campos de cliente potencial esperados.

### Exemplo de OData do Dynamics

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

### Exemplo de Salesforce SOQL

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

>[!MORELIKETHIS]
>
>* [Introdução](getting-started.md)
>* [Funções e permissões do usuário](user-roles-permissions.md)
>* [Clientes Potenciais](prospects.md)
