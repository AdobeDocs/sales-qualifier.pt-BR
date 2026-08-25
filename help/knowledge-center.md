---
title: Criar um manual da Central de conhecimento
description: Saiba como fazer upload de materiais de apoio de vendas e criar um manual no Centro de conhecimento da Sales Qualifier para informar o alcance e a assistência da IA.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/5dpADHs-37gBKs-d1lf2rFLP-bJJQs-06kGCzhgGeRw'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 08dd05e1d13b501d43d457e6217a43aaabdb1d0d
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---


# Centro de conhecimento

O **[!UICONTROL Centro de Conhecimento]** dá à Account Qualification Agent (AQA) acesso aos seus materiais de vendas. A Sales Qualifier usa esses materiais para gerar pesquisas, insights de qualificação e alcance que refletem como sua organização vende. Somente administradores podem criar e gerenciar o manual.

## Carregar material de apoio de vendas

1. Na navegação à esquerda, expanda **[!UICONTROL Administração]** e selecione **[!UICONTROL Configurações de Administração]**.
1. Selecione **[!UICONTROL Centro de conhecimento]** em **[!UICONTROL Integrações]**.
1. Defina o **[!UICONTROL Nome da empresa]** e a **[!UICONTROL URL da empresa]** que a Sales Qualifier usa para pesquisar sua empresa e rascunhar emails.
1. Faça upload das ações de vendas, perfis de clientes ideais (ICPs), guias de posicionamento e outros materiais de apoio de vendas nos formatos PDF, PPTX ou DOCX.

Cada documento carregado exibe seu status de processamento, como **[!UICONTROL Pronto]**, e quando foi atualizado pela última vez.

## Criar um manual

Após carregar os documentos, selecione **[!UICONTROL Criar Manual]**.

>[!NOTE]
>
>Um manual pode levar até 24 horas para ser processado.

Quando o manual estiver pronto, os representantes poderão usá-lo em dois lugares:

* **Prompts de email de saída** — Em um prompt de ponto de contato, nomeie o documento e descreva o contexto a ser usado. Por exemplo, digite `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Consulte [Gerar e analisar pontos de contato](outbound-workflows.md#step-3-generate-and-review-touchpoints).
* **Chat de IA**: consulte o Centro de Conhecimento em sua pergunta. Por exemplo, digite `From the Knowledge Center, help me position our security solution for ABC Corp before tomorrow's call`. Consulte [Chat de IA](ai-assistant.md).

Em ambos os casos, o conteúdo gerado reflete a mensagem no seu manual em vez da pesquisa genérica.

>[!MORELIKETHIS]
>
>* [Fluxos de Trabalho de Saída](outbound-workflows.md)
>* [Bate-papo de IA](ai-assistant.md)
>* [Funções e permissões do usuário](user-roles-permissions.md)
