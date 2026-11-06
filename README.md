# 🚀 Taranis Black — Automação B2B & Inteligência Preditiva

> **Caso de Consultoria em IA Aplicada & Gestão Financeira/Operacional**  
> 🏆 *Desafio Final desenvolvido na formação **AI Builder (Turma G11)** — Parceria **Alura + Oracle Next Education (ONE)***  
> 🎯 *Especialização: Rota 4 (Finanças e Operações)*

---

## 📌 Visão Geral do Projeto

A **Taranis Black** é uma empresa consolidada no segmento de vestuário e equipamentos táticos, apresentando um faturamento anual de **R$ 48 milhões** e um quadro de **280 colaboradores**. 

A esteira de vendas B2B corporativa é responsável por **70% do faturamento total (R$ 33,6M/ano)**. No entanto, a operação enfrentava sérios gargalos operacionais e financeiros decorrentes de processos legados e manuais.

---

## 💔 Dores do Negócio (Pain Points Diagnosticados)

Durante a fase de diagnóstico operacional e financeiro, identificaram-se as seguintes dores críticas na operação da Taranis Black:

- **Gargalo no Tempo de Ciclo B2B (SLA de 5,2 dias úteis):** Da emissão da proposta comercial em PDF ao despacho físico no Centro de Distribuição (CD) de Joinville/SC, o processo consumia 5,2 dias úteis, prejudicando a experiência do cliente e o fluxo de caixa.
- **Sobrecarga de Trabalho Manual (~120h/mês em rotinas repetitivas):** Assistentes financeiros gastavam cerca de 40 minutos por pedido na triagem de propostas em PDF, digitação manual no ERP legado e consultas individuais ao birô de crédito (Serasa).
- **Estouro de Custos Logísticos e Fretes (+18,4% no 2º Semestre):** Divergências na checagem de modalidades CIF/FOB e erros na digitação de fretes geraram um aumento expressivo e não previsto nas despesas logísticas.
- **Acúmulo de PDD e Inadimplência B2B (R$ 1,42 milhão):** Falta de um motor preditivo de regras de crédito e consultas manuais inconsistentes resultaram no acúmulo de R$ 1,42M em Provisão para Devedores Duvidosos.
- **Gargalo em Aprovações de Alçada (Retenção por E-mail):** Processo manual de solicitação de aprovação de crédito retinha ordens por 24h a 48h na caixa de e-mail dos gestores.
- **Turnover Elevado na Operação (22,5% ao ano):** Insatisfação e fadiga da equipe geradas pelo acúmulo de tarefas operacionais repetitivas e falta de inteligência na gestão de pessoas.

---

## 🎯 Objetivos Estratégicos
- **Redução do Tempo de Ciclo Operacional:** De 5,2 dias úteis para **menos de 24 horas úteis**.
- **Eficiência Financeira:** Economia estimada de **~120 horas/mês** da equipe de controladoria e finanças.
- **Contenção de Anomalias Orçamentárias:** Combate ao estouro de fretes (+18,4% no 2º semestre) e mitigação da Provisão para Devedores Duvidosos / Inadimplência B2B (**R$ 1,42M** acumulado em PDD).

---

## 🏗️ Estrutura de Soluções & Iniciativas de IA

### 1. Automação de Faturamento & Motor Preditivo de Crédito (Operações — Rota 4)
- **OCR e Extração Estruturada:** Processamento automático de propostas comerciais em PDF com extração em JSON (CNPJ, itens, tabela de preços e regras CIF/FOB) em menos de 40 segundos.
- **Motor de Alçada e Crédito Preditivo:** Aplicação automática da matriz de risco baseada no score Serasa, aprovando diretamente ordens de baixo/médio risco e aplicando a premissa de **Human-in-the-Loop** apenas para exceções e limites elevados.

### 2. Agente de Qualificação B2B (Vendas — Rota 1)
- Assistente generativo integrado ao CRM para atendimento rápido, consulta ao catálogo técnico de produtos e contorno padronizado de objeções comerciais sobre prazos e fretes.

### 3. Copiloto de People Analytics (RH — Rota 3)
- Análise preditiva e processamento de linguagem natural (NLP) sobre pesquisas de clima interno, visando conter a taxa de turnover operacional (**22,5%**).

---

## 📂 Estrutura do Repositório

```text
📁 ai-builder-taranis-black/
├── 📄 README.md                        <-- Documentação principal do projeto
├── 📁 dashboard/
│   └── taranis_black_dashboard.html    <-- Dashboard Interativo (Live Artifact no Claude)
├── 📁 prompts/
│   ├── prompts.md                      <-- Prompts de limpeza e criação de dashboard usando Live Artifact
├── 📁 diagrams/
│   ├── matriz_sipoc_as_is.png          <-- Diagrama visual da Matriz SIPOC Lean
│   └── diagrama_ishikawa_6m.png        <-- Diagrama de Causa-Raiz (Espinha de Peixe 6M)
└── 📁 docs/
    ├── politica_ia_responsavel.md      <-- Guia de Governança, LGPD e Comitê de IA
    └── challenge_taranis_black_rota_4_final.pdf  <-- Relatório Executivo Final
```

---

## 📊 Artefatos Desenvolvidos & Evidências Técnicas

### 📈 1. Dashboard Financeiro & Preditivo (Live Artifact)
Painel analítico interativo gerado no **Claude (Sonnet)** a partir da auditoria da DRE Orçado vs. Realizado (Planilha 05):
- **Indicadores Executivos (KPIs):** Monitoramento do tempo de ciclo, estouro de fretes, PDD e ganho em horas de trabalho.
- **Análise DRE Comparativa:** Gráfico de colunas evidenciando os desvios orçamentários do 2º semestre.
- **Projeção Preditiva T1-2027:** Comparativo gráfico entre o *Cenário Manutenção* (Status Quo de 5,2 dias) e o *Cenário Otimizado* (com IA, atingindo <24h).

### 🔍 2. Mapeamento Operacional Lean (SIPOC & Ishikawa)
- **Matriz SIPOC:** Mapeamento em 5 colunas (*Suppliers, Inputs, Process, Outputs, Customers*) identificando o gargalo de 40 min na triagem manual de PDFs.
- **Diagrama de Ishikawa (6M):** Diagnóstico estruturado em *Método, Máquina, Mão de Obra, Material, Medição e Meio Ambiente*, destacando a falta de OCR e a dependência de e-mails.

### 🐍 3. Script Python de Data Quality & Integridade
Desenvolvimento de script em Python para validação e higienização da Planilha 05:
- Sanitização de caracteres monetários (`R$`).
- Padronização de datas para o formato ISO 8601 (`YYYY-MM-DD`).
- Tratamento defensivo de valores nulos e validação de tipos de dados antes do carregamento visual.

---

## ⚖️ Governança de IA & Segurança (LGPD)

- **Regras de "Pode / Não Pode":** Proibição do envio de PII (Informações Pessoais Identificáveis) dos 280 colaboradores a modelos públicos sem anonimização.
- **Segregação de Acessos:** Modelos de linguagem isolados de credenciais de execução bancária direta.
- **Human-in-the-Loop (HitL):** Roteamento obrigatório para supervisão humana em reprovações de crédito ou alterações de limites cadastrais.
- **Comitê de IA & Auditoria:** Rituais mensais de revisão de acurácia dos modelos e auditoria contra vieses e alucinações.

---

## 🛠️ Tecnologias & Ferramentas Utilizadas

| Categoria | Tecnologias / Ferramentas |
| :--- | :--- |
| **Modelos de IA Generativa & Preditiva** | Claude (Sonnet) / Anthropic |
| **Desenvolvimento & Scripts** | Python 3.12 (Pandas, NumPy, Plotly), HTML5, Tailwind CSS, JavaScript (Chart.js) |
| **Engenharia de Prompts** | JSON Schemas, System Prompts Estruturados, Few-Shot Prompting |
| **Metodologia & Gestão** | Lean Six Sigma (SIPOC, Ishikawa 6M), DRE Financeira, AI Canvas |
| **Hospedagem & Controle de Versão** | Git, GitHub, GitHub Pages |

---

## 👤 Autoria e Créditos

Projeto desenvolvido por **Camila Rodrigues Mota** no âmbito do **Desafio AI Builder**.

- **Programa:** Oracle Next Education (ONE) + Alura
- **Turma:** G11
- **Especialização:** Rota 4 — Finanças e Operações
