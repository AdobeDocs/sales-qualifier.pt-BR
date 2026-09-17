---
title: Usar o bate-papo de IA
description: Saiba como usar o AI Chat no Adobe Marketo Qualifier para pesquisar contas, elaborar projetos de alcance e obter respostas com base em seus dados de CRM, envolvimento e Centro de conhecimento.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/LHCHAk0rsNwLsKFhKMlHaLL7xkkCEAKFNDMEonb2TdQ'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Sales Qualifier
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: d967b633fcb63c64169d3e3fbf305fd2ff82236d
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 1%
---

# Chat de IA

O AI Chat responde a perguntas em linguagem natural com base no contexto de vendas. Use-a para pesquisar uma conta, preparar uma chamada, rascunhar um alcance geral e priorizar seu trabalho sem sair do Adobe Marketo Qualifier.

![Botão de bate-papo de IA](assets/ai-chat.png){width="800" zoomable="yes"}

## Abrir o bate-papo de IA

Selecione o botão flutuante **[!UICONTROL Bate-papo de IA]** para abrir o painel de chat. O painel é aberto ao lado da página atual, para que você possa manter um cliente potencial, uma conta ou um Fluxo de trabalho de saída no modo de exibição. Arraste a borda do painel para redimensioná-lo. Para fechar o painel, selecione novamente **[!UICONTROL Chat de IA]**.

>[!NOTE]
>
>A disponibilidade do AI Chat depende da configuração da sua organização e das suas permissões. Se o botão **[!UICONTROL Chat de IA]** não for exibido, o recurso não será habilitado para a sua conta.

## Fontes de dados

O AI Chat pode usar estas fontes:

* O manual da sua organização no [Centro de Conhecimento](admin-settings.md#knowledge-center).
* Seu CRM conectado, incluindo clientes potenciais, contatos, contas, oportunidades e atividades.
* [!DNL Marketo] dados de atividade e envolvimento.
* Pesquisa de contas e notícias recentes reunidas pela Account Qualification Agent.
* Pesquisa pública na web.

## Usar o bate-papo de IA

Use o AI Chat para estes tipos de tarefas:

* **Pesquisar e resumir**: solicitar um resumo de uma conta, um grupo de compras ou o compromisso recente de um cliente potencial.
* **Posicionamento da compilação**: peça ao assistente para posicionar sua solução para uma conta específica antes de uma reunião.
* **Rascunho e refine o alcance**: peça para escrever ou reescrever um email. Especifique o tom, o comprimento, o idioma e se os emojis devem ser incluídos.
* **Obter recomendações**: pergunte a quais clientes potenciais ou contas priorizar, ou solicite uma meta ou cadência para um novo Fluxo de Trabalho de Saída.
* **Localizar detalhes do contato**: peça ao assistente para enriquecer um cliente potencial com mais informações de contato e plano de fundo.

## Pergunte ao bate-papo de IA em todos os dados conectados

O AI Chat pode responder a perguntas no Marketo Qualifier, CRM, [!DNL Marketo], [!DNL Adobe Journey Optimizer B2B Edition] e nos dados de inteligência da empresa. Faça uma pergunta em linguagem simples para pesquisar informações ou extrair contexto. O AI Chat lê e relata os seus dados; ele não cria, edita ou inicia nada.

Estes são alguns exemplos de prompts. Quanto mais específico você for no prompt, mais focados serão os resultados.

Clientes potenciais e contas:

* &quot;Localizar clientes potenciais com status de envolvimento Novo.&quot;
* &quot;Pesquise a empresa Adobe.&quot;
* &quot;Dê-me o perfil completo de um cliente potencial.&quot;
* &quot;Mostre o desempenho de saída nos últimos 30 dias.&quot;
* &quot;Listar reuniões reservadas dos últimos 30 dias.&quot;

Centro de conhecimento:

* &quot;Que garantias temos para lidar com objeções de preços?&quot;
* &quot;Quais são nossos principais diferenciais em relação aos concorrentes?&quot;
* &quot;Listar documentos no Centro de conhecimento.&quot;
* &quot;Resumir um documento.&quot;

CRM:

* &quot;Listar oportunidades abertas.&quot;
* &quot;Liste os cinco primeiros clientes em potencial com nome e email.&quot;
* &quot;Mostrar atividades de vendas de um cliente potencial ou conta.&quot;

[!DNL Marketo]:

* &quot;Navegue pelas minhas campanhas inteligentes&quot;.
* &quot;Obtenha a lista inteligente chamada &#39;Adquirido&#39;.&quot;
* &quot;Navegue pelos meus programas ou obtenha um programa pelo nome.&quot;
* &quot;Lista [!DNL Marketo] tipos de atividade.&quot;

[!DNL Adobe Journey Optimizer B2B Edition]:

* &quot;Quantas jornadas eu tenho?&quot;
* &quot;Como meu público-alvo é segmentado por persona?&quot;
* &quot;Quais páginas de aterrissagem existem em minha conta?&quot;
* &quot;Quais campos de clientes potenciais são alimentados para pontuação?&quot;

Inteligência da empresa:

* &quot;Que tecnologias são usadas por uma empresa?&quot;
* &quot;Mostrar notícias recentes de uma empresa.&quot;
* &quot;Localizar empresas semelhantes a uma determinada empresa.&quot;
* &quot;Lista de aberturas de emprego para uma empresa.&quot;

### Escopo e limites atuais

* O AI Chat lê e relata os seus dados. Ela não cria, edita ou inicia nada. Por exemplo, ele não cria um programa, não inicia uma campanha nem edita uma lista.
* O AI Chat pesquisa informações; não é uma ferramenta de relatório. Ele não cria análises ou tendências ao longo do tempo no estilo [!DNL Marketo], como a integridade do email para o trimestre ou uma lista de clientes potenciais criados nos últimos 10 dias. Use relatórios nativos [!DNL Marketo] para essas tarefas.

## Respostas terrestres no seu manual

Para usar o manual do [Centro de Conhecimento](admin-settings.md#knowledge-center), consulte o Centro de Conhecimento na sua pergunta. Por exemplo:

`From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

A resposta reflete as mensagens no seu manual.

## Fornecer feedback sobre as respostas

Classifique o conteúdo gerado com os controles para polegar para cima ou para baixo. Seus comentários ajudam a melhorar respostas futuras.

## Revisar respostas da IA

As respostas geradas por IA podem ser imprecisas. Analise todo o conteúdo antes de usá-lo.

* Verifique fatos, nomes e números antes de confiar neles.
* Leia os emails em rascunho cuidadosamente e personalize-os antes de enviar.
* Use a saída do assistente como ponto de partida, não como uma entrega concluída.

O uso do Bate-papo de IA pela sua organização é regido pelos termos da IA gerativa da Adobe.

>[!MORELIKETHIS]
>
>* [Centro de conhecimento](admin-settings.md#knowledge-center)
>* [Contas](accounts.md)
>* [Fluxos de Trabalho de Saída](outbound-workflows.md)
