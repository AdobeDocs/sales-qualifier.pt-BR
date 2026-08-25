---
title: Funções e permissões do usuário
description: Saiba como os grupos de usuários do Sales Qualifier controlam o acesso do aplicativo e da administração.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/9X9DYGMvLGcPG--G6rHcDEk91hdT9-XYc9wbiL2Qoww'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: d6a8091bd893ea80a26edfc1526646aec037223f
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 4%

---


# Funções e permissões do usuário

A Sales Qualifier usa dois grupos de usuários necessários para separar as tarefas de vendas da configuração em toda a organização.

## Grupos de usuários necessários

| Grupo | A quem pertence | O que concede |
| --- | --- | --- |
| `Sales Qualifier` | Todos os usuários, incluindo administradores | Acesso ao aplicativo: clientes potenciais, contas, planos de envolvimento, tarefas, desempenho e configurações de perfil. |
| `Sales Qualifier Admins` | Somente administradores, além do grupo `Sales Qualifier` | Acesso às **[!UICONTROL Configurações de Administrador]**, que controlam as conexões do CRM, o Centro de Conhecimento e as configurações de conformidade de toda a organização. |

Usuários padrão precisam apenas do grupo `Sales Qualifier`. Os administradores precisam ser membros de ambos os grupos. Consulte [Introdução](getting-started.md) para criar esses grupos.

As organizações também podem criar um grupo `Sales Qualifier BDR managers` opcional. Os membros podem acessar relatórios de desempenho de email.

## Acesso de administrador

**[!UICONTROL Configurações de Administrador]** aparece em **[!UICONTROL Administração]** somente para usuários que pertencem a ambos os grupos necessários. As alterações nessas configurações se aplicam a toda a organização.

## O que os administradores controlam

| Configuração | Onde configurar | Efeito |
| --- | --- | --- |
| Conexão do CRM e mapeamento de campo | [Integrações](integrations.md#map-crm-fields-inbound-mapping) | Determina quais campos do CRM aparecem para um cliente potencial ou conta e quais campos estão disponíveis como filtros. |
| Recusa de email global | [Integrações](integrations.md#configure-global-email-opt-out) | Adiciona um rodapé de cancelamento de inscrição a cada email de saída. |
| Centro de conhecimento e manual | [Centro de conhecimento](knowledge-center.md) | Disponibiliza o manual da empresa em prompts de saída e no [Chat de IA](ai-assistant.md). |
| Sincronização de atividade | [Integrações](integrations.md#configure-activity-sync-outbound-mapping) | Determina se as atividades de alcance geral do Sales Qualifier aparecem no CRM. |

Usuários padrão podem usar essas configurações, mas não podem alterá-las. Se um filtro, uma referência de manual ou um campo CRM esperado estiver ausente, entre em contato com um administrador.

>[!MORELIKETHIS]
>
>* [Introdução](getting-started.md)
>* [Integrações](integrations.md)
>* [Centro de conhecimento](knowledge-center.md)
