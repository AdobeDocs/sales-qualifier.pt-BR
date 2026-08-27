---
title: Gerenciar integrações
description: Saiba como conectar o Outlook, gerenciar conexões do CRM, mapear campos de entrada, sincronizar atividades e configurar a recusa de email global no Sales Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: User, Admin
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 483e57ab9d8f3f5e4201e0b691e37727a25d3f22
workflow-type: tm+mt
source-wordcount: 1377
ht-degree: 1%

---


# Integrações

Conecte o Outlook para enviar emails, reconhecer respostas de clientes potenciais e agendar reuniões. Para disponibilizar clientes potenciais, contatos, contas, oportunidades, atividades e proprietários para o Account Qualification Agent (AQA) e para Workflows de saída, você também pode conectar o Sales Qualifier ao Salesforce ou Microsoft Dynamics 365. O Sales Qualifier lê os dados do CRM, pode gravar atividades de alcance geral e status de recusa no CRM e pode sincronizar atividades de alcance geral com o Marketo. Caso contrário, ela não modificará os registros do CRM.

Este artigo explica como conectar o Outlook, gerenciar uma conexão de CRM, mapear campos, sincronizar atividades e configurar a opção de não participação de email. Para conectar um CRM pela primeira vez, consulte [Introdução](getting-started.md#connect-your-crm).

>[!IMPORTANT]
>
>A conexão do Outlook é por representante. As configurações de CRM e conformidade descritas posteriormente neste artigo se aplicam a toda a organização. Para acessar essas configurações em toda a organização, você deve pertencer aos grupos de usuários `Sales Qualifier` e `Sales Qualifier Admins`. Os usuários padrão podem usar os dados e filtros do CRM configurados, mas não podem alterar as configurações.

## Conectar o Outlook

Cada representante conecta sua própria conta do Outlook:

1. Selecione **[!UICONTROL Conectar ao Outlook]**.
1. Faça logon com sua conta da Microsoft.
1. Revise e aprove o acesso solicitado.

A conexão permite que o Sales Qualifier envie de sua caixa de correio, reconheça quando um cliente potencial responde e agende reuniões em seu calendário.

Ao se conectar, você aprova o acesso que permite ao Sales Qualifier:

* Reconhecer respostas de clientes potenciais.
* Crie e envie emails em seu nome.
* Use seu calendário para agendar reuniões.
* Leia o fuso horário da caixa de correio e o horário de trabalho para agendamento.
* Permaneça conectado automaticamente para que esses recursos continuem funcionando sem exigir logon novamente.

### Aprovações do Outlook (se necessário)

Por padrão, nenhuma ação do administrador é necessária. Cada representante aprova o acesso para si mesmo ao conectar o Outlook.

Se sua organização tiver desativado o consentimento do usuário para aplicativos de terceiros no Microsoft 365 ou Microsoft Entra, um administrador do Microsoft 365 ou Entra deverá aprovar o Sales Qualifier uma vez para toda a organização. O administrador conclui esta aprovação antes que os representantes conectem suas contas do Outlook. Após a aprovação em toda a organização, cada representante pode conectar sua conta.

### Como o Sales Qualifier lida com os dados da sua caixa de correio

O Sales Qualifier lê somente as respostas para emails enviados, não para o restante da caixa de entrada. Ele não armazena anexos ou emails de entrada fora de um envolvimento ativo. As credenciais de entrada armazenadas estão criptografadas.

## Abrir configurações do CRM

Na navegação à esquerda, expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Configurações de Administração]**. As configurações são organizadas em dois grupos:

| Grupo | Itens |
| --- | --- |
| **[!UICONTROL Integrações]** | **[!UICONTROL Conexões do CRM]**, **[!UICONTROL Centro de Conhecimento]** |
| **[!UICONTROL Conformidade]** | **[!UICONTROL Configurações de email]** |

Para o Centro de Conhecimento, consulte [Criar um manual do Centro de Conhecimento](admin-settings.md#knowledge-center).

## Gerenciar conexões do CRM

Selecione **[!UICONTROL Conexões do CRM]**. A página contém cartões para **[!UICONTROL Salesforce]** e **[!UICONTROL Microsoft]** (Microsoft Dynamics 365). Cada cartão mostra um destes status:

| Status | Significado |
| --- | --- |
| **[!UICONTROL Conectado]** | A conexão está ativa e autenticada. |
| **[!UICONTROL Não ativo]** | Nenhuma conexão está configurada para este CRM. |
| **[!UICONTROL Permissões necessárias]** | A conexão está autenticada, mas os escopos necessários estão ausentes. O cartão lista os escopos ausentes. |

>[!NOTE]
>
>Somente um CRM pode estar ativo por vez. Quando um CRM está conectado, o outro cartão é desabilitado. Desconecte o CRM ativo antes de conectar outro.

Um cartão não configurado mostra **[!UICONTROL Conectar]**. Um cartão configurado mostra o menu **[!UICONTROL Gerenciar]** e **[!UICONTROL Mais]** com **[!UICONTROL Editar configuração]** e **[!UICONTROL Desconectar]**.

### Conectar ou editar uma conexão

1. No cartão do CRM, selecione **[!UICONTROL Conectar]** ou **[!UICONTROL Mais]** > **[!UICONTROL Editar configuração]** para atualizar uma conexão existente.
1. Insira as credenciais do administrador do CRM.

   >[!BEGINTABS]

   >[!TAB Salesforce]

   Insira a **[!UICONTROL ID do Cliente (Chave do Consumidor)]**, a **[!UICONTROL URL da Instância]** e o **[!UICONTROL Segredo do Cliente]**. Use o formulário de URL da instância canônica `https://{{mydomain}}.my.salesforce.com`.

   ![Credenciais do Salesforce](assets/crm-salesforce-config.png){width="800" zoomable="yes"}

   >[!TAB Microsoft Dynamics]

   Insira a **[!UICONTROL ID do Cliente (Chave do Consumidor)]**, **[!UICONTROL ID do Locatário]**, **[!UICONTROL URL da Instância do Microsoft Dynamics]** e **[!UICONTROL Segredo do Cliente]**. Use o formulário de URL da instância canônica `https://{{mydomain}}.crm.dynamics.com`.

   >[!ENDTABS]

1. Selecione **[!UICONTROL Conectar]** (ou **[!UICONTROL Salvar]** ao editar).

Se o Sales Qualifier rejeitar as credenciais, identificará a causa, como credenciais inválidas ou expiradas, permissões ausentes ou um locatário não reconhecido do Dynamics. Corrija o valor e tente novamente.

>[!IMPORTANT]
>
>Não envie segredos do cliente por email. Use o canal seguro aprovado da sua organização para compartilhar credenciais com quem quer que as insira no Sales Qualifier.

### Desconectar uma conexão

1. No cartão do CRM conectado, selecione **[!UICONTROL Mais]** > **[!UICONTROL Desconectar]**.
1. Revise o aviso e selecione **[!UICONTROL Desconectar]** para confirmar.

>[!WARNING]
>
>Quando você desconecta um CRM, os fluxos de trabalho de saída são pausados para todos os prospetos em sua organização e nenhum novo prospecto é sincronizado do seu CRM até que você se reconecte.

## Mapear campos do CRM (mapeamento de entrada) {#map-crm-fields-inbound-mapping}

O mapeamento de entrada controla quais campos do CRM o Sales Qualifier importa e onde eles aparecem. Os campos são agrupados em seções e cada seção pertence a um tipo de entidade.

![Mapeamento de entrada](assets/crm-conn-salesforce.png){width="800" zoomable="yes"}

1. No cartão do CRM conectado, selecione **[!UICONTROL Gerenciar]**.
1. Na guia **[!UICONTROL Mapeamento de entrada]**, selecione **[!UICONTROL Adicionar seção]**.

   ![Adicionar seção](assets/crm-add-section.png){width="800" zoomable="yes"}

1. Na etapa **Selecionar seção**, escolha o tipo de entidade e selecione **[!UICONTROL Avançar]**:

   | Entidade | Onde os campos aparecem |
   | --- | --- |
   | **[!UICONTROL Clientes Potenciais]** | A guia **[!UICONTROL Pessoa]** de um cliente potencial. |
   | **[!UICONTROL Contatos]** | O registro de contato. |
   | **[!UICONTROL Contas]** | A guia **[!UICONTROL Conta]**. Consulte [Contas](accounts.md). |
   | **[!UICONTROL Oportunidades]** | Os detalhes da oportunidade da conta. |

1. Insira um **[!UICONTROL Nome da seção]** e uma **[!UICONTROL Descrição]** opcional. Em seguida, selecione **[!UICONTROL Próximo]**.
1. Na etapa **[!UICONTROL Adicionar campo]**, procure e selecione os campos do CRM a serem importados. Em seguida, selecione **[!UICONTROL Próximo]**. Cada campo mostra seu **[!UICONTROL Nome para exibição]**, **[!UICONTROL Nome do campo]** e **[!UICONTROL Tipo de dados]**.
1. Para as seções **[!UICONTROL Clientes Potenciais]**, **[!UICONTROL Contatos]** e **[!UICONTROL Oportunidades]**, ative **[!UICONTROL Filtrável]** para cada campo que os representantes precisam na lista [Clientes Potenciais](prospects.md).

   Um campo não pode se tornar filtrável se o tipo de dados não for compatível com a filtragem ou se já estiver sendo usado em outra seção.

   Em **[!UICONTROL Meus Contatos da Oportunidade]**, os campos de oportunidade filtráveis aparecem como colunas separadas com rótulos como **[!UICONTROL Preparo (Oportunidade)]**. O sufixo distingue atributos de oportunidade de campos no contato associado.

1. Na etapa **[!UICONTROL Visualizar]**, confirme sua seleção e selecione **[!UICONTROL Adicionar]**.

Para alterar uma seção posteriormente, selecione **[!UICONTROL Editar]** no cartão de seção. Para remover uma seção, selecione **[!UICONTROL Remover]** no cartão de seção. Para remover um campo individual, selecione a ação de exclusão na linha de campo. Confirme cada remoção.

## Configurar a sincronização de atividades (mapeamento de saída) {#configure-activity-sync-outbound-mapping}

A sincronização de atividades grava atividades de alcance da Sales Qualifier no seu CRM e no Marketo. As atividades de email enviado, aberto, clicado e respondido incluem o nome do Fluxo de trabalho de saída. Os representantes podem ver as atividades no CRM, enquanto as equipes de marketing podem usar as atividades do Marketo na pontuação de clientes potenciais e nas linhas do tempo de engajamento.

1. No cartão do CRM conectado, selecione **[!UICONTROL Gerenciar]**.
1. Abra a guia **[!UICONTROL Mapeamento de saída]**.
1. Ative a **[!UICONTROL Sincronização de atividade]**. A configuração é salva imediatamente.

Quando a sincronização de atividades está desativada, o Sales Qualifier continua a usar dados de entrada do CRM, mas não sincroniza atividades de alcance para o CRM ou o Marketo.

>[!NOTE]
>
>A sincronização de atividades requer acesso de gravação no CRM. Se a permissão necessária estiver ausente, o switch será desativado e a Sales Qualifier solicitará que você entre em contato com o administrador. Para conceder acesso de gravação à atividade, fale com o administrador do CRM.

## Configurar destaques de marketing {#turn-on-marketo-engagement-filtering}

Os Destaques de marketing permitem que os representantes encontrem e priorizem clientes potenciais por meio do envolvimento ativo de [!DNL Marketo], como aberturas e cliques de email. Consulte [Filtrar por destaques de marketing](prospects.md#filter-by-marketing-highlights).

Um administrador conclui uma configuração única que conecta o [!DNL Marketo] ao Sales Qualifier para a organização e a sandbox relevantes. A instalação abrange a criação de credenciais de API no Adobe Developer Console, a configuração de um webhook no [!DNL Marketo] e a adição desse webhook a um acionador de Campanha Inteligente. Consulte [Configurar destaques de marketing](marketing-highlights-setup.md) para ver as etapas completas.

Marketing Highlights está disponível em todas as regiões de produção: América do Norte, EMEA e Austrália.

## Configurar opção de não participação de email global {#configure-global-email-opt-out}

A configuração de recusa anexa um rodapé de cancelamento de inscrição a cada email de saída. Usuários padrão não podem desativá-la para um email individual.

1. Na navegação à esquerda, expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Configurações de Administração]**.
1. Selecione as **[!UICONTROL Configurações de email]** em **[!UICONTROL Conformidade]**.
1. Ative **[!UICONTROL Incluir link para opção de não participação em todos os emails]**.
1. Em **[!UICONTROL Modelo de mensagem de recusa]**, digite o texto do rodapé. Inclua o token `{opt_out_link}` no qual o link para cancelar inscrição clicável deve aparecer.

   Por exemplo: `If you'd prefer not to receive these emails, you can {opt_out_link}.`

A configuração e o modelo são salvos automaticamente.

Quando um cliente potencial seleciona o link, o Sales Qualifier interrompe o envio de emails para esse cliente potencial e sincroniza o status de recusa para o CRM conectado.

## Escopo de acesso do CRM

O Sales Qualifier lê as entidades de CRM de que precisa e grava apenas um conjunto definido de dados:

* **Leitura** — Usuários, contatos, mapeamentos de proprietários, clientes potenciais, contas, oportunidades e atividades.
* **Gravação**—Atividades de alcance registradas (quando [a sincronização de atividades](#configure-activity-sync-outbound-mapping) está ativada) e status de recusa.

Seu administrador de CRM prepara o acesso à API no Salesforce ou Dynamics. Em seguida, um administrador do Sales Qualifier conecta o CRM, mapeia campos de entrada e escolhe se deseja sincronizar atividades. A conexão inicial requer acesso somente leitura. A sincronização de atividades e a opção de recusa de gravação exigem o acesso de gravação correspondente.

>[!MORELIKETHIS]
>
>* [Introdução](getting-started.md)
>* [Contas](accounts.md)
