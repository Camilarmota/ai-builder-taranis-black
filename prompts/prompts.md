# 🤖 Engenharia de Prompts — Taranis Black (Claude Sonnet)

> **Documentação dos Prompts Utilizados na Rota 4 (Finanças e Operações)**  
> *Projeto: Desafio AI Builder (Alura + Oracle Next Education - Turma G11)*

Este documento reúne os dois prompts principais desenvolvidos e executados no **Claude (Sonnet)** para a sanitização de dados financeiros, identificação de anomalias na DRE e construção do **Dashboard Interativo (Live Artifact)**.

---

## 📋 1. Prompt de Limpeza, Sanitização e Integridade de Dados (Data Quality)

* **Finalidade:** Auditar e higienizar a planilha de DRE Financeira (`05_Financas_Orcado_vs_Realizado.xlsx`) via script Python executado no Claude, garantindo a integridade dos dados antes da geração dos gráficos visuais.
* **Etapa da Rota 4:** Etapa 3 (Validação de Integridade & ETL).
* **Entrada:** Arquivo `.xlsx` bruto com caracteres monetários (`R$`), datas em formatos mistos e potenciais valores nulos.
* **Saída:** Base tratada e relatório de inconformidades técnicas.

### 📄 Conteúdo do Prompt:

```text
Você é um Engenheiro de Dados Sênior e Auditor de Qualidade Financeira da Taranis Black.
Analise a planilha financeira anexada (05_Financas_Orcado_vs_Realizado.xlsx) e execute um script Python para validar a integridade dos dados e higienizar a base antes da análise executiva.

Requisitos obrigatórios do tratamento de dados:

1. SANITIZAÇÃO DE FORMATOS MONETÁRIOS:
   - Remova todos os caracteres "R$", espaços em branco e separadores de milhar pontuados.
   - Converta os campos de valores financeiros em float com duas casas decimais.

2. PADRONIZAÇÃO DE DATAS:
   - Identifique e converta todas as colunas de data/período para o padrão internacional ISO 8601 (YYYY-MM-DD ou YYYY-QQ para trimestres).

3. TRATAMENTO DE VALORES NULOS E DIVERGÊNCIAS:
   - Substitua valores ausentes em colunas numéricas por 0.00 e em colunas categóricas por "NÃO ESPECIFICADO".
   - Identifique registros duplicados ou com inconsistência matemática entre Orçado e Realizado.

4. LOG DE AUDITORIA:
   - Exiba um resumo com o total de linhas processadas, tipo de dados convertidos e uma tabela com os desvios discrepantes encontrados nas colunas de Frete e PDD.

Retorne o script Python executado e a confirmação da base higienizada pronta para carregamento gráfico.
```

---

## 📊 2. Prompt Master — Análise de Anomalias DRE & Dashboard Preditivo (Live Artifact)

* **Finalidade:** Orientar o Claude na análise analítica da DRE Orçado vs. Realizado, destacar as 5 anomalias operacionais e compor um **Live Artifact** (painel interativo em HTML/Tailwind/Chart.js) com simulação preditiva para T1-2027.
* **Etapa da Rota 4:** Etapa 3 (Dashboard Inteligente - Artefato Principal).
* **Entrada:** Base de dados financeira sanitizada.
* **Saída:** Aplicação web interativa (*Live Artifact*) exibindo KPIs, gráficos comparativos e projeção de ciclo de tempo.

### 📄 Conteúdo do Prompt:

```text
Você é um Consultor Sênior de IA e Controller Financeiro da Taranis Black. 
Com base na planilha de DRE Orçado vs. Realizado (Planilha 05) tratada, crie um Live Artifact (Dashboard Interativo em HTML/React/Tailwind com Chart.js) que consolide a análise financeira e preditiva da Rota 4 (Finanças e Operações).

O Dashboard deve conter obrigatoriamente as seguintes seções:

1. CABEÇALHO & KPIS PRINCIPAIS (4 CARDS DE IMPACTO):
   - Tempo de Ciclo Operacional Atual: 5,2 dias úteis (Meta: < 24h úteis).
   - Estouro em Fretes/Logística (2º Semestre): +18,4% acima do orçado (divergências CIF/FOB).
   - Provisão PDD / Inadimplência B2B: R$ 1,42 M acumulado (gargalo de concessão de crédito).
   - Ganho Estimado com IA: ~120 horas/mês liberadas na controladoria.

2. VISUALIZAÇÃO GRÁFICA DRE (ORÇADO VS. REALIZADO):
   - Gráfico de colunas comparando valores Orçados x Realizados por trimestre (T1 a T4).
   - Destaque visual e alertas para o estouro nos trimestres T3 e T4 causados por Fretes e PDD.

3. GRÁFICO PREDITIVO (PROJEÇÃO T1-2027):
   - Gráfico de linhas comparando dois cenários para o próximo trimestre:
     a) Cenário Manutenção (Status Quo): ciclo mantido em ~5,2 dias úteis.
     b) Cenário Otimizado (Automação OCR + Crédito por IA): ciclo reduzido para < 24h úteis.

4. MATRIZ / CARDS DAS 5 ANOMALIAS OPERACIONAIS & FINANCEIRAS:
   Exiba em destaque as 5 anomalias identificadas no diagnóstico:
   1) Fretes e logística de entrega (+57% de estouro por divergências CIF/FOB e fretes extras).
   2) Cancelamentos e devoluções por atraso (+121% por clientes B2B afetados pelo SLA de 5 dias).
   3) PDD / Inadimplência B2B (+152% por falhas na esteira de concessão de crédito 30/60/90).
   4) Reentregas e multas por divergência em NF-e (+245% por erros de digitação e retenção em Joinville).
   5) Despesas administrativas e sistemas legados (+15% por custo de digitação manual de 40 min/pedido).

Gere o código como um Live Artifact interativo, visualmente elegante (tema escuro/slate) e pronto para apresentação executiva.
```
