# Estudo Dirigido: Introdução às Finanças Pessoais e Investimentos

Este repositório contém a documentação do caderno de estudos criado no NotebookLM para o desafio de projeto da DIO. O objetivo central é organizar e sintetizar informações sobre planejamento financeiro pessoal e conceitos básicos de investimento a partir de fontes oficiais e materiais educativos.

---

## 1. Contexto e Objetivos

### Contexto
O estudo aborda a gestão de finanças pessoais, focando em organização do orçamento, constituição de reserva de emergência e introdução aos instrumentos de renda fixa no Brasil.

### Objetivos
* Organizar as etapas para a criação de um orçamento pessoal equilibrado.
* Diferenciar os principais títulos de renda fixa (Tesouro Direto, CDBs) e seus indexadores (Selic, IPCA, CDI).
* Mapear os critérios de liquidez e risco para montagem de reserva de emergência.
* Validar a aplicação do NotebookLM no processamento e síntese de documentos técnicos.

---

## 2. Curadoria de Fontes

Foram selecionadas quatro fontes para alimentar o caderno temático no NotebookLM:

1. **Banco Central do Brasil (BCB)** — Portal institucional com diretrizes sobre o sistema financeiro nacional.
2. **Cadernos e Guias de Educação Financeira** — Materiais educativos sobre gestão de orçamentos e conceitos de crédito.
3. **XP Investimentos (Seção de Finanças Pessoais)** — Artigos sobre alocação de recursos, reserva de emergência e produtos financeiros.
4. **Programa de Cidadania Financeira (BCB)** — Documento oficial (`https://www.bcb.gov.br/content/cidadaniafinanceira`) focado em inclusão, planejamento e direitos do consumidor bancário.

---

## 3. Engenharia de Prompts e Diagnóstico de Falhas (Troubleshooting)

### Testes e Refinamento de Prompts

#### Teste 1: Regras para Reserva de Emergência
* **Prompt Inicial (Genérico):** *"Como fazer uma reserva de emergência?"*
  * **Problema Identificado:** A IA retornou conselhos genéricos sobre economia doméstica sem especificar prazos, liquidez ou ativos recomendados pelos materiais do Banco Central.
* **Prompt Refinado:** *"Com base exclusivamente nos documentos do Banco Central e da XP carregados, quais são os critérios técnicos para calcular o valor de uma reserva de emergência e em quais tipos de ativos ela deve ser mantida? Indique a liquidez necessária."*
  * **Resultado:** A resposta detalhou o cálculo (3 a 6 meses de custo fixo) e indicou ativos com liquidez diária ($D+0$ ou $D+1$), como Tesouro Selic e CDBs de liquidez imediata, com citações diretas das fontes.

#### Teste 2: Comparativo entre Indexadores
* **Prompt Inicial (Genérico):** *"O que é melhor, Selic ou IPCA?"*
  * **Problema Identificado:** A resposta trouxe um tom opinativo sem explicar as condições econômicas em que cada taxa é aplicada.
* **Prompt Refinado:** *"Sintetize a diferença entre os indexadores Selic e IPCA segundo o material de Cidadania Financeira. Apresente o objetivo de cada um e em qual cenário de inflação cada título se torna mais indicado."*
  * **Resultado:** A IA gerou uma explicação objetiva separando o controle de juros (Selic) da proteção contra perda do poder de compra (IPCA).

### Ajustes Técnicos (Troubleshooting)
* **Restrição de Fonte:** Para evitar respostas baseadas no conhecimento geral do modelo, foi necessário incluir explicitamente a cláusula *"Com base estritamente nos documentos fornecidos"* no início de cada instrução.
* **Formatação das Saídas:** Respostas longas apresentaram perda de clareza. O uso de pedidos diretos por "tabelas comparativas" ou "listas numeradas em até 3 pontos" resolveu o problema de dispersão do texto.

---

## 4. Miniguia de Estudo

### Resumo Estruturado

#### A. Planejamento Financeiro e Orçamento
* **Diagnóstico:** Mapeamento de receitas fixas/variáveis e despesas fixas/variáveis.
* **Priorização:** Quitação de dívidas com juros altos antes do início de qualquer aplicação financeira.
* **Reserva de Emergência:** Alocação em ativos de baixo risco de crédito e liquidez imediata para cobrir imprevistos.

#### B. Renda Fixa e Indexadores
* **Tesouro Selic:** Título público indicado para reserva de emergência devido ao baixo risco e rentabilidade atrelada à taxa básica de juros.
* **Tesouro IPCA+:** Título que combina uma taxa fixa mais a variação da inflação, recomendado para objetivos de médio e longo prazo para preservação do poder de compra.
* **CDB (Certificado de Depósito Bancário):** Título privado emitido por bancos, rentabilidade geralmente atrelada ao CDI, coberto pelo Fundo Garantidor de Créditos (FGC) até o limite regulatório.

---

### Glossário de Conceitos

| Termo | Definição |
| :--- | :--- |
| **Taxa Selic** | Taxa básica de juros da economia brasileira, definida pelo COPOM. |
| **IPCA** | Índice de Preços ao Consumidor Amplo, medidor oficial da inflação no Brasil. |
| **CDI** | Certificado de Depósito Interbancário, taxa que baliza o rendimento de aplicações de renda fixa privada. |
| **Liquidez** | Velocidade e facilidade com que um ativo pode ser convertido em dinheiro disponível na conta. |
| **FGC** | Fundo Garantidor de Créditos, entidade privada que protege depósitos bancários até determinados limites em caso de intervenção na instituição. |

---

### Prompts Reutilizáveis para Revisão

Estes prompts podem ser copiados e utilizados para revisões futuras no NotebookLM:

1. **Extração de Conceitos Chave:**
   > *"Liste os 5 conceitos centrais do documento [Nome do Documento] em formato de lista numerada, acompanhados de uma definição concisa de uma frase para cada um."*

2. **Gerador de Questões de Fixação:**
   > *"Com base no texto sobre [Tema], crie 3 perguntas objetivas de múltipla escolha com 4 alternativas cada. Forneça o gabarito ao final com a justificativa técnica baseada no texto."*

3. **Análise de Aplicação Prática:**
   > *"Apresente um caso prático simples demonstrando como a variação da taxa Selic afeta diretamente o rendimento de uma aplicação em Renda Fixa versus o custo de crédito pessoal."*
