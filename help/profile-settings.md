---
title: Definir configurações de perfil
description: Saiba como configurar sua conexão de email, assinatura e disponibilidade de calendário nas configurações de perfil do Sales Qualifier.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/juP3sddkmc-nSTcTEKGWolbCwNWDgSA0yr6XK1X-w94'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: e7de3a1e28cb8268b58f1ab1ec10394035bdfd74
workflow-type: tm+mt
source-wordcount: 375
ht-degree: 3%

---


# Configurações do perfil

Na navegação à esquerda, expanda **[!UICONTROL Configuração]** e selecione **[!UICONTROL Configurações de perfil]**. Use essas configurações para gerenciar seus detalhes pessoais, conexão de email, calendário e disponibilidade de chat.

## Configurações de email

Na guia **[!UICONTROL Configurações de email]**, configure suas conexões de email.

* **[!UICONTROL Conexões de email]**—Selecione **[!UICONTROL Conectar ao Outlook]** e siga o processo de entrada da Microsoft. Consulte [Conectar-se ao Outlook](integrations.md#connect-outlook) para obter o acesso que você aprova e o caminho de aprovação do administrador, se necessário.
* **[!UICONTROL Assinatura de email]** — Adicione ou atualize a assinatura usada nos emails gerados. Inclua o link da sua [reserva de reunião](outbound-workflows.md#meeting-booking) para que os clientes potenciais possam agendar horários com você.

### Contexto de redação do email

Use o **[!UICONTROL Contexto de rascunho de email]** para definir o tom, a estrutura e o estilo do email, de forma que os emails sejam consistentes.

Escreva seu contexto em marcação simples na área **[!UICONTROL Contexto de rascunho de email]**.
Use-a para definir:

* Tom e voz
* Estrutura e comprimento
* Personalization e regras de saudação
* Estilo da linha de assunto
* Como os sinais de engajamento são usados
* Como métricas, pontos de prova e histórias de clientes são enquadradas

Por padrão, os rascunhos usam um contexto de estilo doméstico, de modo que os rascunhos existentes não são alterados até que você adicione seu próprio contexto.

## Configuração do calendário

Na guia **[!UICONTROL Configuração do calendário]**, defina o fuso horário e a disponibilidade.

* **[!UICONTROL Conexão do calendário]**—Selecione **[!UICONTROL Conectar]** e siga o processo de entrada da Microsoft.
* **[!UICONTROL Email de confirmação da reunião]** — Defina o assunto e o corpo do email de confirmação que um cliente potencial recebe após reservar uma reunião.
* **[!UICONTROL Preferências]** — Defina a duração padrão da reunião e o buffer entre reuniões.

Se você desconectar seu calendário:

* Os links de reserva ativos param de funcionar.
* A página de reserva mostra uma mensagem de indisponibilidade temporária.
* Suas configurações são preservadas quando você se reconecta.

## Disponibilidade do calendário

A disponibilidade de seu calendário no Sales Qualifier é baseada em duas entradas:

* Seu calendário de trabalho conectado, como Outlook ou Gmail
* As regras de disponibilidade e intervalo de tempo na **[!UICONTROL Configuração do calendário]**

O Sales Qualifier lê o status de disponibilidade, não os detalhes do evento, do calendário conectado. Ele combina esse status com suas regras para determinar os intervalos de tempo que os clientes potenciais podem reservar.

Você pode configurar:

* Horas de trabalho por dia da semana
* Vários blocos por dia, por exemplo, das 9h às 13h e das 13h às 17h.
* Seu fuso horário
* Duração da reunião
* Buffer antes e depois de reuniões
* Aviso mínimo
* Janela de reserva

>[!MORELIKETHIS]
>
>* [Fluxos de Trabalho de Saída](outbound-workflows.md)
>* [Integrações](integrations.md)
>* [Tarefas](tasks.md)
