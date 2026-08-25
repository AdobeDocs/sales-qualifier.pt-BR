---
title: Clientes potenciais no Sales Qualifier
description: Saiba como criar, filtrar e revisar sua lista de clientes potenciais no Sales Qualifier para priorizar o alcance externo.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 08dd05e1d13b501d43d457e6217a43aaabdb1d0d
workflow-type: tm+mt
source-wordcount: 535
ht-degree: 2%

---


# Clientes potenciais

Selecione **[!UICONTROL Clientes potenciais]** na navegação à esquerda para ver os clientes potenciais e os contatos que você pode acessar. Use a lista para examinar o status de cada cliente potencial e a atividade mais recente.

![Tabela de clientes potenciais exibindo o status do cliente potencial e a última atividade para gerenciamento de clientes potenciais](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL Clientes Potenciais]** — Clientes Potenciais atribuídos a você no CRM conectado.
* **[!UICONTROL Contatos]** — Contatos atribuídos a você no CRM conectado.
* **[!UICONTROL Lista de pessoas]** — Clientes potenciais que você importa ou adiciona manualmente.

## Criar sua lista de clientes potenciais

A lista de clientes potenciais combina pessoas de mais de uma fonte:

* **Prospetos do CRM** — o Sales Qualifier importa automaticamente clientes potenciais e contatos atribuídos ao usuário conectado. Consulte [Integrações](integrations.md).
* **Prospetos importados** — Prospetos importados de um arquivo CSV.
* **Prospetos adicionados manualmente** — Prospetos individuais adicionados ao Sales Qualifier.

Para adicionar prospetos que não vêm do seu CRM:

1. Na página **[!UICONTROL Clientes potenciais]**, selecione **[!UICONTROL Lista de pessoas]**.
1. Selecione **[!UICONTROL + Adicionar pessoas]** e **[!UICONTROL Importar CSV]** ou **[!UICONTROL Adicionar pessoa]**.

   * Para uma importação de CSV, carregue um CSV no formato `firstname,email`.
     O nome e o email são obrigatórios. O sobrenome é opcional. O modelo CSV não inclui a coluna de ID de cliente potencial do CRM, mas você pode adicionar a coluna e seus valores ao arquivo antes da importação. Se a importação falhar, revise a mensagem de erro para os campos ou valores a serem corrigidos e, em seguida, faça upload do arquivo novamente.
   * Para adicionar uma pessoa manualmente, insira seus detalhes no formulário.

1. Selecione **[!UICONTROL Salvar]**.

## Filtrar e localizar clientes potenciais

Selecione **[!UICONTROL Filtro]** para restringir a lista. Você pode filtrar por:

* Status do plano de engajamento
* Criado por
* Nome do cargo
* Conta
* Fonte
* Última atualização

Os administradores também podem disponibilizar campos do CRM mapeados como filtros. Em **[!UICONTROL Configurações de Administrador]**, ative **[!UICONTROL Filtrável]** para cada campo que os representantes usam para localizar clientes potenciais. Consulte [Mapear campos do CRM](integrations.md#map-crm-fields-inbound-mapping).

Em **[!UICONTROL Meus Contatos da Oportunidade]**, você também pode filtrar contatos por campos de suas oportunidades associadas, como estágio, tipo e data de fechamento. Os campos de oportunidade têm rótulos como **[!UICONTROL Estágio (Oportunidade)]**, que os distingue dos campos de contato. O administrador controla quais campos de oportunidade estão disponíveis como filtros.

### Filtrar por envolvimento da Marketo

Encontre e priorize prospetos por meio do envolvimento dinâmico do [!DNL Marketo], como aberturas e cliques de email, visitas da Web, preenchimentos de formulário e momentos interessantes. O engajamento aparece em tempo quase real, à medida que acontece.

Para filtrar clientes potenciais por envolvimento da Marketo:

1. Selecione **[!UICONTROL Filtro]**.
1. Adicione um filtro de envolvimento [!DNL Marketo] e defina o tipo de atividade, a campanha ou outros atributos para se concentrar no envolvimento que é importante.

Cada cliente potencial mostra sua atividade [!DNL Marketo] mais recente junto com o histórico recente.

A filtragem de envolvimento do Marketo está disponível em todas as regiões de produção. O administrador ativa a organização e a sandbox, e um profissional de marketing conclui uma configuração única no [!DNL Marketo]. Consulte [Ativar a filtragem de envolvimento do Marketo](integrations.md#turn-on-marketo-engagement-filtering).

## Revisar detalhes do cliente potencial

Selecione um cliente potencial para abrir seu perfil. Revise os sinais importantes antes de entrar em contato com:

* **Resumo da pessoa de IA** — um instantâneo escrito por IA do cliente potencial ou contato e seu envolvimento recente. Use o resumo para entender a pessoa rapidamente antes de revisar atividades individuais. Os resumos da pessoa de IA estão disponíveis em instâncias que executam o Adobe Journey Optimizer B2B edition Prime ou o Ultimate.
* **Lista de atividades** — Uma lista cronológica de atividades e comportamentos recentes.
* **Modo de exibição de Linha do Tempo** — uma linha do tempo visual do envolvimento entre canais.
* **Conteúdo exibido** — páginas da Web e ativos que o cliente potencial visualizou. Selecione um item para abri-lo.

>[!MORELIKETHIS]
>
>* [Contas](accounts.md)
>* [Fluxos de Trabalho de Saída](outbound-workflows.md)
>* [Bate-papo de IA](ai-assistant.md)
