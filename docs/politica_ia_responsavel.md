# Política de IA Responsável e Governança Corporativa — Taranis Black

> **Documento Institucional de Governança, Ética e Conformidade (LGPD)**  
> **Empresa:** Taranis Black Móveis Corporativos  
> **Aplica-se a:** Todos os colaboradores, gestores, terceiros e sistemas automatizados  
> **Versão:** 1.0 — Ciclo 2026  

---

## 1. Diretrizes Executivas e Princípios Gerais

A Taranis Black reconhece a Inteligência Artificial como uma tecnologia estratégica para alavancar a eficiência operacional, reduzir o tempo de ciclo da esteira B2B (de 5,2 dias úteis para menos de 24 horas úteis) e otimizar a tomada de decisão em Finanças, Vendas, RH e Marketing.

Para garantir que o uso de modelos de linguagem (LLMs), visão computacional (OCR) e algoritmos preditivos ocorra de forma ética, segura e alinhada à legislação vigente, estabelece-se o princípio fundamental do **"Copiloto Corporativo"**: a Inteligência Artificial atua estritamente como ferramenta de suporte e automação de tarefas repetitivas, mantendo a responsabilidade final, a validação crítica e a decisão estratégica sob controle humano (*Human-in-the-Loop*).

---

## 2. Matriz de Permissões: O que Pode e o que Não Pode

Para orientar a atuação diária de todas as equipes, fica estabelecida a matriz clara de uso permitido e proibido:

### 2.1. Usos Permitidos (O que PODE fazer)
1. **Automação de Tarefas Repetitivas:** Utilizar IA para extração e leitura de dados estruturados a partir de documentos em PDF (como propostas comerciais B2B), auxílio na geração de rascunhos de e-mails, resumos de reuniões e automação de fluxos de trabalho.
2. **Análise de Dados Agregados:** Processar e analisar DREs financeiras, indicadores operacionais de fretes/PDD e pesquisas de clima organizacional utilizando dados previamente anonimizados ou pseudonimizados.
3. **Simulação e Treinamento:** Utilizar assistentes de IA para treinamento de vendas (contorno de objeções no CRM) e simulações de conversas difíceis de liderança (modelo SBI no RH) em ambientes corporativos homologados.
4. **Tratamento de Dados Financeiros e Operacionais:** Executar scripts de sanitização de dados em Python para correção de formatos, remoção de caracteres de moeda e padronização ISO de datas.

### 2.2. Usos Proibidos (O que NÃO PODE fazer)
1. **Upload de PII e Dados Sensíveis (LGPD):** É estritamente proibido inserir nomes completos, CPFs, credenciais bancárias de clientes ou dados médicos/pessoais dos 280 colaboradores em modelos públicos de IA sem contrato corporativo de privacidade ou sem anonimização prévia.
2. **Disparo Automático sem Validação Humana:** Proibido o envio automatizado de propostas comerciais, orçamentos, contratos, notas fiscais (NF-e) ou laudos ergonômicos a clientes e órgãos reguladores sem checagem prévia.
3. **Decisões Automatizadas Unilaterais:** Proibido utilizar IA para aprovação definitiva e autônoma de concessão de crédito, contratações, demissões, reajustes salariais ou punições disciplinares sem intervenção humana.
4. **Treinamento de Modelos Públicos:** Proibida a utilização de ferramentas de IA que utilizem os dados corporativos e segredos industriais da Taranis Black para treinamento de modelos comerciais abertos.

---

## 3. Conformidade com a LGPD e Segurança da Informação

1. **Garantia de Privacidade de Dados:** Todas as soluções de IA contratadas ou desenvolvidas internamente devem operar via APIs corporativas privadas com cláusulas contratuais explícitas de não-retenção e não-treinamento de modelos com dados da empresa.
2. **Anonimização de PII:** Em análises de People Analytics e DRE, os campos de identificação pessoal e cadastral devem ser substituídos por identificadores sintéticos ou mascarados antes do envio ao modelo.
3. **Segregação de Ambientes:** Os modelos de linguagem e assistentes virtuais devem rodar isolados de sistemas com permissão de execução financeira direta ou credenciais bancárias.

---

## 4. Mitigação de Riscos Técnicos e Algorítmicos

### 4.1. Prevenção de Alucinações
- **Base de Verdade Oficial:** As respostas geradas por IA relativas a preços, especificações técnicas (NR-17) e políticas de frete (CIF/FOB) devem ser checadas obrigatoriamente contra a base de dados oficial da empresa (Catálogo de Produtos 2026 e Tabela de Preços vigente).
- **Incentivo à Recusa:** Prompts do sistema devem ser configurados com a instrução explícita de responder *"Informação não localizada na base"* caso o dado consultado não esteja no contexto fornecido, evitando inferências arbitrárias.

### 4.2. Prevenção de Vieses Algorítmicos
- **Auditoria de People Analytics:** Modelos preditivos utilizados para mapear risco de turnover ou análise de clima no RH não poderão utilizar variáveis demográficas (gênero, idade, raça ou estado civil) como fatores de decisão ou classificação de risco.
- **Régua de Crédito Transparente:** O motor preditivo de análise de crédito B2B deve basear-se exclusivamente em critérios financeiros objetivos (Score Serasa, histórico de compras e limite cadastral).

---

## 5. Estrutura de Governança, Comitê e Rituais

### 5.1. Composição do Comitê de Governança de IA
O Comitê de IA da Taranis Black é o órgão responsável pela supervisão ética e homologação de tecnologias, composto por:
- **Gerente de TI** (Coordenação Técnica e Arquitetura de Sistemas)
- **Encarregado de Proteção de Dados / DPO** (Conformidade Legal e LGPD)
- **Controller Financeiro / Gerente de Operações** (Representação da Rota 4)
- **Gerente de People & Culture / RH** (Representação da Rota 3)
- **Gerente Comercial / B2B** (Representação da Rota 1)

### 5.2. Rituais e Cadência de Auditoria
1. **Reunião Mensal de Governança:** Avaliação de novas ferramentas de IA solicitadas pelos departamentos, revisão de logs de segurança, análise de custos com tokens e tratamento de potenciais incidentes.
2. **Auditoria Trimestral de Acurácia e Algoritmos:** Verificação amostral da taxa de precisão da leitura de OCR em PDFs, validação da aderência das aprovações de crédito e auditoria dos modelos do RH contra vieses.

---

## 6. Disposições Finais

O descumprimento das diretrizes desta Política de IA Responsável sujeitará o infrator às sanções administrativas e disciplinares previstas no Código de Conduta Interno da Taranis Black, sem prejuízo das responsabilizações civis e penais cabíveis sob a legislação brasileira.
