---
title: Contas no Sales Qualifier
description: Saiba como revisar a inteligência de contas no Sales Qualifier, incluindo pesquisa sobre IA, notícias recentes, oportunidades e contatos mais envolvidos, para priorizar o alcance externo.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 632
ht-degree: 0%

---


# Contas

A visualização da conta combina pesquisa gerada por IA, notícias recentes, oportunidades abertas, valor do pipeline e contatos envolvidos. Use essas informações para entender e priorizar uma conta antes de entrar em contato.

## Abrir uma conta

Abrir uma conta do perfil de um cliente potencial associado a ela.

1. Selecione **[!UICONTROL Clientes Potenciais]** na navegação à esquerda e abra um cliente potencial. Consulte [Prospects](prospects.md).
1. Na página de detalhes do cliente potencial, selecione a guia **[!UICONTROL Conta]**.

O Sales Qualifier identifica a conta do registro CRM do cliente potencial. A mesma visualização de conta está disponível em todos os clientes potenciais associados a essa conta. Se o Sales Qualifier não corresponder a uma conta, a guia mostrará _Nenhuma conta encontrada_.

>[!NOTE]
>
>As seções e métricas disponíveis dependem do CRM, da configuração de sua organização e dos dados da conta. Se uma seção descrita aqui não for exibida, os dados ou o recurso necessários não serão configurados.

A exibição de conta tem duas guias: **[!UICONTROL Detalhes]** e **[!UICONTROL Pesquisa de Conta]**.

## Revise os detalhes da conta

A guia **[!UICONTROL Detalhes]** fornece um instantâneo da conta e seu pipeline.

### Visão geral da conta

O cartão de visão geral na parte superior da guia identifica a conta e resume seu valor:

* O nome e a região da conta
* **Receita anual recorrente (ARR)** — A receita anual recorrente de todas as assinaturas ativas. Selecione **[!UICONTROL Exibir todos]** para analisar a ARR por produto na caixa de diálogo **[!UICONTROL Receita recorrente anual]**.
* Estatísticas de conta, incluindo oportunidade em aberto e contagens de contato e o valor do pipeline

### Resumo da visão geral da conta

O painel **[!UICONTROL Visão geral da conta]** resume a conta com base nos dados do CRM e na pesquisa da Account Qualification Agent. Se a pesquisa estiver em andamento, o painel mostrará um estado de carregamento. Se a pesquisa não estiver disponível, o painel mostrará uma mensagem.

### Insights da conta

Use os botões abaixo da visão geral para alternar entre visualizações de conta. As exibições disponíveis dependem do CRM e da configuração:

| Exibir | O que ele mostra |
| --- | --- |
| **[!UICONTROL Oportunidades]** | Abra oportunidades vinculadas à conta, com campos-chave para cada uma. Selecione **[!UICONTROL Exibir tudo]** para ver a lista completa em uma tabela. Detalhes da oportunidade, como estágio, tipo e data de fechamento, também podem ser usados para filtrar os contatos da conta em **[!UICONTROL Meus Contatos da Oportunidade]** quando um administrador torna esses campos filtráveis. |
| **[!UICONTROL Membros Principais]** | Os contatos mais envolvidos da conta, classificados por envolvimento. Cada contato mostra o título do cargo, o endereço de email, a pontuação de engajamento e o indicador de urgência. |
| **[!UICONTROL Dados de intenção]** | Sinais de intenção de compra para a conta, como os produtos e tópicos que a conta está pesquisando. |
| **[!UICONTROL Membros da equipe de conta]** | Pessoas atribuídas à conta, com seu email, cargo, território e grupo de produtos. |
| **[!UICONTROL Campos do CRM]** | Campos de conta importados do seu CRM, conforme configurado no mapeamento de entrada. Consulte [Integrações](integrations.md#map-crm-fields-inbound-mapping). |

Na exibição **[!UICONTROL Membros Principais]**, execute uma destas ações para um contato:

* **[!UICONTROL Adicionar ao Fluxo de Trabalho de Saída]**—Inscreva o contato em um [Fluxo de Trabalho de Saída](outbound-workflows.md).
* **[!UICONTROL Adicionar à campanha do Marketo]**—Acione uma campanha [!DNL Marketo] para o contato.

## Pesquisar a conta

A guia **[!UICONTROL Pesquisa de Conta]** contém três áreas:

* **[!UICONTROL Categorias de pesquisa]**—Tópicos de pesquisa. Selecione uma categoria para exibir sua pesquisa no painel central.
* **Conteúdo de pesquisa** — cartões de pesquisa gerados por IA agrupados por categoria. Um cartão pode incluir o domínio de origem e as datas em que o sinal foi detectado pela primeira e última vez.
* **[!UICONTROL Notícias recentes]**—Notícias atuais sobre a conta, incluindo datas, marcas e links de origem.

Se não for possível carregar a pesquisa ou as notícias, cada área oferecerá uma ação **[!UICONTROL Recarregar]** para tentar novamente.

## Usar a inteligência de conta em alcance

A inteligência de conta é mais valiosa quando molda o que você envia:

* Referencie uma notícia recente ou um sinal de pesquisa para tornar sua abertura relevante, em vez de usar uma apresentação genérica.
* Verifique as oportunidades abertas e o valor do pipeline para decidir se prioriza a conta.
* Use **[!UICONTROL Membros Principais]** para identificar com quem contatar e, em seguida, inscreva-os em um Fluxo de Trabalho de Saída.
* Peça ao [Bate-papo de IA](ai-assistant.md) para desenvolver o posicionamento para a conta antes de uma chamada.

>[!MORELIKETHIS]
>
>* [Clientes Potenciais](prospects.md)
>* [Fluxos de Trabalho de Saída](outbound-workflows.md)
>* [Bate-papo de IA](ai-assistant.md)
