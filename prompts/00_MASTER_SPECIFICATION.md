
## reports/

Contém uma pasta para cada competência mensal do projeto.

Cada competência é autocontida e possui a seguinte estrutura:

- `source/`: PDFs originais exportados das ferramentas.
- `analysis/`: análises individuais de Google Analytics 4 e Google Search Console.
- `output/`: resumo executivo em Markdown e versão Word.
- `manifest.json`: inventário dos arquivos obrigatórios e mecanismo de validação antes da execução.
- Os PDFs deverão permanecer com os nomes originais exportados pelas ferramentas. Não haverá renomeação manual.

## history/

Armazena o histórico consolidado do projeto, incluindo registros mensais, indicadores históricos e análises evolutivas para facilitar comparações e acompanhamento de longo prazo.

## history/monthly/

Contém registros resumidos de cada mês com principais ganhos, perdas, hipóteses, ações executadas, pendências e recomendações.

## knowledge/

A pasta `knowledge/` constitui a memória permanente do projeto. Todos os arquivos presentes nela deverão ser carregados integralmente antes do início de qualquer análise. Essa base fornece contexto sobre países, indicadores, objetivos, decisões arquiteturais, histórico consolidado, boas práticas e demais conhecimentos necessários para que a IA produza análises consistentes ao longo do tempo.

## prompts/

Contém os prompts utilizados para geração das análises e relatórios, cada um com responsabilidades específicas dentro do fluxo de trabalho.
Todos os prompts da pasta deverão ser carregados em todas as execuções, respeitando suas responsabilidades específicas.

## templates/

Armazena modelos e estruturas para geração de documentos, facilitando a padronização das entregas.


## scripts/

Contém scripts e ferramentas de automação que suportam o processamento dos dados, geração de relatórios e outras tarefas do projeto.

# Relatórios que continuarão com análise individual

## Google Analytics 4

Responsável por analisar:

- comportamento dos usuários
- canais
- engajamento
- eventos
- conversões
- audiência

Entrega:

- análise individual
- utilizada como apoio ao resumo executivo

---

## Google Search Console

Responsável por analisar:

- impressões
- cliques
- CTR
- posição média
- páginas
- consultas

Entrega:

- análise individual
- utilizada como apoio ao resumo executivo

---

# Responsabilidade dos Prompts

## 00_MASTER_SPECIFICATION.md

Documento de arquitetura do projeto, especificando estrutura, fluxos, responsabilidades e regras gerais.

## 01_PROMPT_RELATORIO_EXECUTIVO.md

Prompt responsável pela execução mensal da geração do resumo executivo consolidado.

## 02_ESTILO_DE_ESCRITA.md

Define as regras e diretrizes para o estilo de escrita utilizado nas análises e relatórios.

## 03_REGRAS_DE_ANALISE.md

Estabelece a metodologia e regras para análise dos dados e interpretação dos relatórios.

## 04_GLOSSARIO.md

Contém definições técnicas e termos utilizados no projeto para garantir consistência e clareza.

## 05_HISTORICO_DO_PROJETO.md

Fornece contexto permanente e histórico do projeto, auxiliando na compreensão da evolução e decisões anteriores.

- Exportar todos os PDFs do período.
- Criar a pasta da competência (AAAA-MM).
- Armazenar todos os PDFs em `source/` mantendo seus nomes originais.
- Gerar automaticamente ou validar o `manifest.json`.
- Confirmar que todos os relatórios obrigatórios estão presentes.
- Ler todos os PDFs da competência.

## Convenção dos Arquivos

Os arquivos exportados pelo Google Analytics 4, Google Search Console e SEMrush deverão permanecer exatamente com os nomes gerados pelas respectivas ferramentas.

A identificação de cada relatório será realizada automaticamente utilizando padrões conhecidos dos nomes dos arquivos.

O projeto não depende de renomeação manual dos PDFs.

O arquivo `manifest.json` será responsável por registrar o mapeamento entre os nomes físicos dos arquivos e os tipos de relatório utilizados durante a análise.

---

## Etapa 4

Cruzar automaticamente as informações provenientes de:

- Google Analytics
- Google Search Console
- Auditoria
- SEO Checker
- Backlinks
- Keyword Strategy
- Monitoramento de posições

A IA deverá identificar relações entre os relatórios.

Exemplos:

- queda de impressões acompanhada por perda de posições
- crescimento de backlinks refletindo em ganho de palavras-chave
- problemas técnicos impactando indexação
- crescimento de páginas indexadas
- aumento de erros críticos
- melhora da distribuição de palavras-chave Top 10
- perda de rankings em determinados países

---

# Estrutura do novo Resumo Executivo

O documento deverá possuir no máximo duas páginas.

Seu objetivo é apresentar apenas informações estratégicas.

---

## 1. Resumo Geral

Responder objetivamente:

O que aconteceu no período em comparação ao período anterior?

Explicar:

- evolução
- regressão
- estabilidade

Sem repetir métricas já presentes no Dashboard.

---

## 2. Principais Pontos Positivos

Apresentar apenas os fatos mais relevantes.

Exemplos:

- crescimento de autoridade
- melhora em rankings
- evolução de backlinks
- crescimento orgânico
- redução de erros técnicos
- aumento de páginas indexadas

Quando pertinente, separar por país.

---

## 3. Principais Pontos de Atenção

Apontar os principais problemas observados.

Exemplos:

- perda de posições
- redução de tráfego
- aumento de erros
- queda de CTR
- perda de backlinks
- problemas técnicos

Quando pertinente, separar por país.

---

## 4. Impacto Geral no Projeto

Responder apenas uma pergunta:

"O projeto evoluiu ou regrediu neste período?"

Explicar os motivos.

---

## 5. Recomendações

Listar apenas ações práticas.

Priorizar.

Exemplo:

Alta prioridade

- corrigir erros críticos
- recuperar páginas estratégicas
- otimizar clusters prioritários

Média prioridade

- ampliar backlinks
- revisar conteúdos
- melhorar links internos

Baixa prioridade

- pequenos ajustes técnicos
- melhorias futuras

---

# Papel dos PDFs

Os PDFs deixam de ser relatórios de leitura.

Passam a ser documentos de auditoria.

Eles servem para:

- rastreabilidade
- comprovação técnica
- consultas futuras
- validação das conclusões do resumo executivo

---

# Dashboard Looker Studio

O Dashboard continuará sendo a principal ferramenta de consulta operacional.

O cliente poderá acessar:

- métricas em tempo real
- filtros
- comparativos
- evolução histórica
- indicadores

O resumo executivo deverá complementar o Dashboard, jamais repetir seus números.

---

# Histórico do Projeto

Será criada uma base histórica para preservar a evolução do projeto.

Cada mês deverá gerar um registro resumido contendo:

- principais ganhos
- principais perdas
- hipóteses
- ações executadas
- pendências
- recomendações

Esse histórico permitirá análises comparativas entre meses, sem necessidade de reler todos os PDFs.

---

# Fluxo de Trabalho

```text
Exportação dos PDFs
        │
        ▼
Criação da Competência
        │
        ▼
source/
        │
        ▼
Validação do manifest.json
        │
        ▼
Leitura dos PDFs
        │
        ▼
analysis/
        │
        ▼
Correlação dos Dados
        │
        ▼
output/
        │
        ▼
Resumo Executivo
        │
        ▼
Versão Word
        │
        ▼
Entrega
```

# Entregáveis Mensais

- PDFs originais preservados em `source/`.
- Análise individual do Google Analytics 4 em `analysis/`.
- Análise individual do Google Search Console em `analysis/`.
- Resumo executivo em Markdown em `output/`.
- Versão Word do resumo executivo em `output/`.
- Dashboard Looker Studio atualizado.
- Histórico mensal atualizado.

O resumo executivo é o principal entregável analítico do projeto.

---

# Benefícios Esperados

- Redução significativa do volume de leitura para o cliente.
- Maior foco em tomada de decisão.
- Manutenção de toda a documentação técnica para auditoria.
- Padronização das entregas mensais.
- Construção de histórico consistente do projeto.
- Facilidade para comparações de longo prazo.
- Processo escalável para vários anos de acompanhamento.
- Possibilidade futura de automatização completa da geração do resumo executivo utilizando IA.
- Eliminação da renomeação manual dos arquivos exportados.
- Maior robustez na identificação automática dos relatórios.
- Redução do tempo operacional de preparação das competências.

# Evoluções Futuras

O projeto visa a automação completa dos processos, incluindo:

- leitura automática dos PDFs exportados
- organização automática dos arquivos nas pastas corretas
- consolidação e análise integrada dos dados
- comparação automática com o histórico acumulado
- geração automática do resumo executivo consolidado
- exportação automática da versão Word do relatório
- integração com SEMrush, Google Analytics 4 e Google Search Console para coleta direta de dados
- atualização automática dos indicadores históricos
- implementação de análises preditivas para antecipar tendências e problemas

Essas evoluções permitirão maior eficiência, precisão e escalabilidade na geração dos relatórios executivos.

# Nova lógica de processamento

- Exportar todos os PDFs do período.
- Criar a pasta da competência (AAAA-MM).
- Armazenar todos os PDFs em `source/` mantendo seus nomes originais.
- Gerar automaticamente ou validar o `manifest.json`.
- Confirmar que todos os relatórios obrigatórios estão presentes.
- Ler todos os PDFs da competência.

# Ordem Obrigatória de Carregamento do Contexto

Toda execução deverá seguir obrigatoriamente esta sequência:

1. Ler `START_HERE.md`.
2. Ler `README.md`.
3. Ler este documento (`00_MASTER_SPECIFICATION.md`).
4. Ler todos os arquivos da pasta `prompts/`.
5. Ler todos os arquivos da pasta `knowledge/`.
6. Ler todos os arquivos disponíveis em `history/`.
7. Identificar automaticamente a competência mensal mais recente.
8. Gerar ou validar o `manifest.json`.
9. Ler exclusivamente os PDFs da pasta `source/`.
10. Gerar as análises individuais.
11. Gerar o resumo executivo.

Nenhuma análise poderá ser iniciada antes da conclusão dessa sequência.
# 00 MASTER SPECIFICATION

# Projeto SFTL Reporting

## Objetivo

Este documento é a especificação mestre do projeto SFTL Reporting.

Ele funciona como a fonte principal de arquitetura, escopo, responsabilidades e regras estruturais do processo de geração dos Relatórios Executivos Mensais do projeto Solve for Tomorrow Latam.

A partir desta fase, o projeto deixa de ter como foco a produção de várias análises individuais de todos os relatórios técnicos exportados e passa a priorizar a construção de um único Relatório Executivo Mensal, com foco em tomada de decisão.

Os relatórios técnicos exportados do Google Analytics 4, Google Search Console e SEMrush continuam sendo preservados como documentação de apoio, evidência técnica e base de consulta futura.

As únicas análises individuais obrigatórias são:

- Google Analytics 4
- Google Search Console

Essas duas análises permanecem porque representam as principais fontes de comportamento do usuário e desempenho orgânico. Elas funcionam como documentação complementar ao resumo executivo, caso seja necessário aprofundar algum ponto apresentado ao cliente.

---

# Papel deste Documento

Este arquivo deve ser tratado como Single Source of Truth estrutural do projeto.

Ele define:

- arquitetura do repositório;
- responsabilidades de cada diretório;
- responsabilidades dos prompts;
- fluxo de trabalho mensal;
- regras de processamento;
- entregáveis obrigatórios;
- separação entre Codex e ChatGPT;
- critérios de qualidade;
- critérios de conclusão da competência.

Toda alteração estrutural relevante deve ser refletida primeiro neste documento e, depois, propagada para `README.md`, `START_HERE.md` e demais arquivos relacionados.

---

# Princípio Central da Arquitetura

O fluxo do projeto é dividido em duas responsabilidades complementares.

## 1. Pipeline operacional no Codex

Responsável por:

- preparar a competência mensal;
- validar a estrutura de pastas;
- validar os PDFs originais;
- gerar ou atualizar o `manifest.json`;
- carregar o contexto metodológico;
- gerar as análises individuais de GA4 e GSC;
- consolidar o resumo executivo em Markdown;
- aguardar revisão humana;
- atualizar histórico e changelog após aprovação.

## 2. Finalização editorial no ChatGPT

Responsável por:

- revisar o resumo executivo aprovado;
- ajustar clareza, fluidez e apresentação editorial;
- preservar o conteúdo aprovado;
- gerar os arquivos finais em DOCX e PDF.

O Codex não deve gerar DOCX ou PDF durante o pipeline operacional. Esses formatos pertencem à etapa final de entrega, conduzida no ChatGPT após revisão humana.

---

# Estrutura do Repositório

```text
sftl-reporting/
├── START_HERE.md
├── README.md
├── reports/
│   └── AAAA-MM/
│       ├── source/
│       ├── analysis/
│       ├── output/
│       └── manifest.json
├── history/
│   ├── monthly/
│   ├── indicadores_historicos.csv
│   └── evolucao_mensal.md
├── knowledge/
│   ├── 01_PROJETO.md
│   ├── 02_GRUPOS_SEMRUSH.md
│   ├── 03_PAISES.md
│   ├── 04_RELATORIOS.md
│   ├── 05_INDICADORES.md
│   ├── 06_OBJETIVOS.md
│   ├── 07_TIMELINE.md
│   ├── 08_DECISOES_ARQUITETURAIS.md
│   ├── 09_BOAS_PRATICAS_SEO.md
│   ├── 10_LICOES_APRENDIDAS.md
│   └── 11_CHANGELOG.md
├── prompts/
│   ├── 00_MASTER_SPECIFICATION.md
│   ├── 01_PROMPT_RELATORIO_EXECUTIVO.md
│   ├── 02_ESTILO_DE_ESCRITA.md
│   ├── 03_REGRAS_DE_ANALISE.md
│   ├── 04_GLOSSARIO.md
│   ├── 05_HISTORICO_DO_PROJETO.md
│   ├── 06_HIPOTESES_E_CONFIANCA.md
│   ├── 07_ESTILO_CONSULTIVO.md
│   └── 08_RELATORIO_EXECUTIVO.md
├── templates/
└── scripts/
```

---

# Responsabilidade dos Diretórios

## START_HERE.md

Documento de entrada operacional.

Toda competência deve iniciar por ele.

Define a ordem de execução, validação, carregamento de contexto, interrupções obrigatórias e critérios de conclusão.

## README.md

Documento de visão geral do repositório.

Apresenta arquitetura, escopo, organização das competências, fluxo de trabalho e regras de qualidade para leitura humana rápida.

## reports/

Contém uma pasta para cada competência mensal.

Cada competência deve ser autocontida.

Estrutura padrão:

```text
reports/AAAA-MM/
├── source/
├── analysis/
├── output/
└── manifest.json
```

### source/

Armazena os PDFs originais exportados das ferramentas.

Regras:

- preservar os nomes originais dos arquivos;
- não renomear PDFs manualmente;
- não misturar arquivos de competências diferentes;
- usar os PDFs como evidência técnica e base de leitura do período.

### analysis/

Armazena somente análises intermediárias.

Arquivos obrigatórios:

```text
ga4_analise.md
gsc_analise.md
```

Não devem ser armazenados entregáveis finais nesta pasta.

### output/

Armazena os entregáveis da competência.

Arquivos esperados:

```text
resumo_executivo.md
resumo_executivo.docx
resumo_executivo.pdf
```

O arquivo `resumo_executivo.md` é gerado pelo Codex.

Os arquivos `resumo_executivo.docx` e `resumo_executivo.pdf` são gerados posteriormente no ChatGPT, após revisão humana.

### manifest.json

Inventário da competência.

Deve registrar:

- competência analisada;
- arquivos encontrados em `source/`;
- tipo identificado de cada relatório;
- relatórios obrigatórios presentes ou ausentes;
- status da validação;
- status da revisão;
- status de conclusão operacional.

Nenhuma análise deve ser iniciada antes da validação do `manifest.json`.

## history/

Armazena o histórico consolidado do projeto.

Inclui:

- registros mensais;
- indicadores históricos;
- evolução acumulada;
- ganhos e perdas por período;
- hipóteses validadas ou descartadas;
- ações executadas;
- pendências e recomendações recorrentes.

A atualização do histórico deve ocorrer somente após aprovação humana do resumo executivo.

## knowledge/

Memória permanente do projeto.

Deve ser carregada integralmente antes de qualquer análise técnica.

Contém informações estruturais sobre:

- projeto;
- países;
- grupos de análise;
- relatórios;
- indicadores;
- objetivos;
- timeline;
- decisões arquiteturais;
- boas práticas de SEO;
- lições aprendidas;
- changelog.

O baseline não deve ser sobrescrito mensalmente. Caso seja necessária uma nova referência histórica, ela deve ser criada como nova versão documentada.

## prompts/

Contém os prompts e regras metodológicas do projeto.

Todos os prompts devem ser carregados em todas as execuções, respeitando suas responsabilidades específicas.

## templates/

Armazena modelos e estruturas auxiliares para geração das entregas.

## scripts/

Contém scripts e ferramentas de automação, validação e suporte operacional.

---

# Responsabilidade dos Prompts

## 00_MASTER_SPECIFICATION.md

Define arquitetura, escopo, responsabilidades, fluxo de trabalho, regras estruturais e critérios de conclusão.

## 01_PROMPT_RELATORIO_EXECUTIVO.md

Define o processo de geração do resumo executivo consolidado da competência.

## 02_ESTILO_DE_ESCRITA.md

Define o padrão de escrita, clareza, objetividade, linguagem consultiva e tom executivo dos relatórios.

## 03_REGRAS_DE_ANALISE.md

Define regras de interpretação, cruzamento de fontes, uso de hipóteses, leitura de variações e limites de causalidade.

## 04_GLOSSARIO.md

Padroniza termos técnicos, indicadores, conceitos e nomenclaturas utilizadas nos relatórios.

## 05_HISTORICO_DO_PROJETO.md

Fornece contexto histórico permanente sobre evolução, decisões e mudanças relevantes do projeto.

## 06_HIPOTESES_E_CONFIANCA.md

Define como declarar hipóteses, níveis de confiança, limitações dos dados e evidências necessárias para sustentar conclusões.


## 07_ESTILO_CONSULTIVO.md

Define a abordagem consultiva das análises, priorizando impacto, decisão, risco, oportunidade e próximos passos.


## 08_RELATORIO_EXECUTIVO.md

Define o padrão do conteúdo consolidado do `resumo_executivo.md`, incluindo estrutura, critérios de seleção dos achados, uso de evidências numéricas, linguagem executiva e regras para transformar os dados da competência em decisão.

---

# Fontes de Dados

O processo considera três grupos principais de fontes.

## Google Analytics 4

Responsável por analisar:

- sessões;
- usuários;
- novos usuários;
- canais de tráfego;
- páginas acessadas;
- países;
- dispositivos;
- engajamento;
- eventos;
- conversões ou key events.
- variações frente ao mês anterior;
- principais páginas com ganho ou queda;
- principais países ou grupos com ganho ou queda.

Entrega obrigatória:

```text
reports/AAAA-MM/analysis/ga4_analise.md
```

A análise deve incluir camada mínima de evidência numérica, com valor atual, valor anterior, variação absoluta e variação percentual para os indicadores principais quando os dados estiverem disponíveis.

## Google Search Console

Responsável por analisar:

- cliques;
- impressões;
- CTR;
- posição média;
- páginas;
- consultas;
- países;
- oportunidades orgânicas.
- variações frente ao mês anterior;
- principais páginas com ganho ou queda;
- principais consultas com ganho ou queda;
- principais países com ganho ou queda.

Entrega obrigatória:

```text
reports/AAAA-MM/analysis/gsc_analise.md
```

A análise deve incluir camada mínima de evidência numérica, com valor atual, valor anterior, variação absoluta e variação percentual para os indicadores principais quando os dados estiverem disponíveis.

## SEMrush

Responsável por fornecer apoio estratégico e evidências complementares sobre:

- backlinks;
- domínios de referência;
- autoridade;
- toxicidade;
- monitoramento de posição;
- keywords;
- auditoria técnica;
- visibilidade por país.

Na arquitetura atual, relatórios do SEMrush não geram análises individuais obrigatórias, salvo se o usuário solicitar explicitamente. Eles devem ser utilizados como fonte de apoio para o resumo executivo, histórico, baseline e leitura estratégica.

Quando utilizado no resumo executivo, o SEMrush também deve trazer evidência numérica suficiente para sustentar o achado, como posições, visibilidade, tráfego estimado, backlinks, domínios de referência, authority score, volume de problemas técnicos ou URLs afetadas.

---

# Convenção dos Arquivos Originais

Os arquivos exportados pelas ferramentas devem permanecer exatamente com os nomes originais.

Regras:

- não renomear PDFs manualmente;
- não padronizar nomes fora do pipeline;
- não mover PDFs para fora da competência após validação;
- não substituir PDFs históricos sem justificativa explícita;
- registrar todos os arquivos no `manifest.json`.

A identificação dos relatórios deve ser realizada automaticamente por meio de padrões conhecidos nos nomes dos arquivos e, quando necessário, pelo conteúdo validado durante o processamento.

---

# Fluxo de Trabalho Mensal

## Fase 1. Preparação da competência

O Codex deve:

- iniciar a execução pelo `START_HERE.md`;
- ler o `README.md`;
- validar a estrutura do repositório;
- localizar ou criar a competência solicitada;
- criar ou validar `source/`, `analysis/` e `output/`;
- gerar ou validar o `manifest.json` inicial;
- solicitar ao usuário a cópia dos PDFs para `source/`;
- interromper a execução até o usuário responder `CONTINUAR`.

## Fase 2. Importação dos relatórios

O usuário deve copiar os PDFs originais para:

```text
reports/AAAA-MM/source/
```

Os arquivos devem permanecer com seus nomes originais.

## Fase 3. Validação dos arquivos

Após o usuário responder `CONTINUAR`, o Codex deve:

- listar os PDFs presentes em `source/`;
- identificar o tipo de cada relatório;
- validar relatórios obrigatórios;
- atualizar o `manifest.json`;
- interromper a execução em caso de inconsistência crítica.

Nenhuma análise deve ser gerada antes dessa validação.

## Fase 4. Carregamento do contexto

Antes da análise técnica, o Codex deve carregar:

1. `START_HERE.md`
2. `README.md`
3. `prompts/00_MASTER_SPECIFICATION.md`
4. todos os demais arquivos de `prompts/`
5. todos os arquivos de `knowledge/`
6. todos os arquivos disponíveis em `history/`
7. exclusivamente os PDFs da competência ativa

Nenhuma análise deve ser iniciada antes da conclusão dessa sequência.

## Fase 5. Análises individuais obrigatórias

Gerar:

```text
reports/AAAA-MM/analysis/ga4_analise.md
reports/AAAA-MM/analysis/gsc_analise.md
```

Essas análises devem:

- interpretar os dados do período;
- comparar com o mês anterior;
- informar valor atual, valor anterior, variação absoluta e variação percentual para os principais indicadores quando disponíveis;
- identificar tendências;
- apontar impactos estratégicos;
- destacar riscos e oportunidades;
- apoiar a geração do resumo executivo.

## Fase 6. Resumo executivo

Gerar:

```text
reports/AAAA-MM/output/resumo_executivo.md
```

O resumo executivo deve:

- ter foco em decisão executiva;
- evitar repetição operacional de métricas já disponíveis no Looker Studio;
- incluir camada mínima de evidência numérica para sustentar a tese central do período;
- consolidar os achados de GA4, GSC e SEMrush quando aplicável;
- apresentar evolução, regressão ou estabilidade;
- evidenciar impactos no projeto;
- listar recomendações priorizadas;
- funcionar como principal entregável analítico do mês.

Após gerar esse arquivo, o Codex deve interromper a execução para revisão humana.

## Fase 7. Revisão humana

O usuário revisa o `resumo_executivo.md`.

Se houver ajustes, o Codex deve alterar apenas os arquivos Markdown correspondentes dentro da competência ativa.

O histórico e o changelog não devem ser atualizados antes da aprovação explícita.

## Fase 8. Encerramento operacional

Após aprovação explícita do usuário, o Codex deve:

- atualizar `history/`;
- atualizar `knowledge/11_CHANGELOG.md`;
- registrar a competência como concluída no `manifest.json`;
- encerrar o pipeline operacional.

## Fase 9. Finalização editorial

No ChatGPT, utilizar:

```text
reports/AAAA-MM/output/resumo_executivo.md
```

Para gerar:

```text
reports/AAAA-MM/output/resumo_executivo.docx
reports/AAAA-MM/output/resumo_executivo.pdf
```

Essa etapa deve preservar o conteúdo aprovado e ajustar apenas apresentação, clareza editorial e formatação final.

---

# Estrutura do Resumo Executivo

O resumo executivo deve ter no máximo duas páginas em sua versão final.

Deve ser objetivo, consultivo e orientado à tomada de decisão.

Estrutura recomendada:

## 1. Resumo Geral

Responder:

- o que aconteceu no período em comparação ao período anterior;
- se houve evolução, regressão ou estabilidade;
- quais números sustentam essa leitura;
- quais fatores explicam o comportamento observado;
- qual é o impacto geral para o projeto.

O Resumo Geral deve conter um bloco curto de evidências numéricas, incluindo os principais dados de GA4 e Google Search Console quando disponíveis.

## 2. Principais Pontos Positivos

Destacar somente os fatos mais relevantes.

Exemplos:

- crescimento de tráfego qualificado;
- melhora de visibilidade orgânica;
- evolução de rankings;
- fortalecimento de backlinks;
- aumento de presença regional;
- melhora de engajamento.

Quando pertinente, separar por país ou grupo regional.

## 3. Principais Pontos de Atenção

Apontar os riscos ou problemas mais relevantes.

Exemplos:

- queda de tráfego;
- perda de posições;
- redução de CTR;
- queda de impressões;
- problemas técnicos;
- aumento de dependência de poucos canais;
- perda de presença em países estratégicos.

Quando pertinente, separar por país ou grupo regional.

## 4. Impacto Geral no Projeto

Responder objetivamente:

```text
O projeto evoluiu, regrediu ou permaneceu estável neste período?
```

A resposta deve explicar os motivos e indicar o nível de confiança da leitura quando necessário.

## 5. Recomendações Priorizadas

Listar ações práticas, separadas por prioridade.

### Alta prioridade

Ações com impacto direto em tráfego, SEO, indexação, autoridade ou estabilidade do projeto.

### Média prioridade

Ações de otimização, expansão de conteúdo, melhoria de CTR, links internos, backlinks e ajustes estruturais.

### Baixa prioridade

Ações complementares, melhorias futuras e refinamentos que não bloqueiam o desempenho atual.

---

# Papel dos PDFs

Os PDFs deixam de ser relatórios de leitura direta para o cliente.

Eles passam a funcionar como documentos de auditoria.

Servem para:

- rastreabilidade;
- comprovação técnica;
- consulta futura;
- validação das conclusões;
- preservação histórica da competência.

O relatório executivo não deve apenas resumir os PDFs. Ele deve interpretar, correlacionar e priorizar as informações.

---

# Papel do Looker Studio

O dashboard no Looker Studio continua sendo a principal ferramenta de consulta operacional.

Ele concentra:

- métricas detalhadas;
- filtros;
- comparativos;
- evolução histórica;
- indicadores operacionais.

O resumo executivo deve complementar o dashboard, não repetir seus números de forma excessiva.

Evitar repetição excessiva não significa omitir números essenciais. O resumo executivo deve trazer os dados mínimos necessários para que a conclusão seja auditável, especialmente quando afirmar crescimento, queda, avanço, regressão, estabilidade, ganho ou perda de eficiência.

---

# Regras Obrigatórias de Análise

- Nunca analisar PDFs fora da competência ativa.
- Nunca misturar competências diferentes.
- Nunca gerar análise antes da validação do `manifest.json`.
- Nunca depender de renomeação manual dos PDFs.
- Nunca repetir métricas operacionais em excesso quando já disponíveis no Looker Studio.
- Nunca omitir números essenciais necessários para sustentar conclusões executivas.
- Nunca afirmar crescimento, queda, avanço, regressão, estabilidade ou perda de eficiência sem evidência numérica quando os dados estiverem disponíveis.
- Nunca transformar hipótese em fato.
- Nunca apresentar causalidade sem evidência suficiente.
- Nunca gerar DOCX ou PDF antes da aprovação humana.
- Sempre carregar `prompts/`, `knowledge/` e `history/` antes da análise.
- Sempre correlacionar dados entre GA4, GSC e SEMrush quando aplicável.
- Sempre diferenciar fato, hipótese e recomendação.
- Sempre priorizar impacto estratégico.
- Sempre registrar limitações dos dados quando existirem.
- Sempre aplicar a camada mínima de evidência numérica nas análises individuais e no resumo executivo.
- Sempre salvar arquivos dentro da competência ativa.
- Sempre interromper após gerar `resumo_executivo.md`.
- Sempre atualizar histórico e changelog somente após aprovação explícita do usuário.

---

# Entregáveis Mensais

Entregáveis técnicos e operacionais:

```text
reports/AAAA-MM/source/
reports/AAAA-MM/analysis/ga4_analise.md
reports/AAAA-MM/analysis/gsc_analise.md
reports/AAAA-MM/output/resumo_executivo.md
reports/AAAA-MM/manifest.json
```

Entregáveis finais, gerados após revisão editorial:

```text
reports/AAAA-MM/output/resumo_executivo.docx
reports/AAAA-MM/output/resumo_executivo.pdf
```

Entregáveis complementares:

- Dashboard Looker Studio atualizado;
- histórico mensal atualizado;
- changelog atualizado;
- PDFs originais preservados como evidência.

---

# Critérios de Qualidade

O relatório mensal deve atender aos seguintes critérios:

- ser objetivo;
- ter foco executivo;
- evitar excesso de métrica operacional;
- incluir camada mínima de evidência numérica, com valor atual, valor anterior, variação absoluta e variação percentual para os principais indicadores quando disponíveis;
- indicar o que mudou no período;
- explicar por que a mudança é relevante;
- indicar os números que sustentam as principais conclusões;
- indicar impacto para o projeto;
- separar fato de hipótese;
- apresentar recomendações práticas;
- ser comparável mês a mês;
- manter rastreabilidade técnica via PDFs e manifest;
- preservar consistência com o histórico e baseline.

---

# Critério de Conclusão da Competência

Uma competência estará pronta para revisão humana quando:

- a arquitetura tiver sido validada;
- os PDFs obrigatórios tiverem sido copiados para `source/`;
- o `manifest.json` tiver sido validado;
- o contexto completo tiver sido carregado;
- `ga4_analise.md` tiver sido gerado com camada mínima de evidência numérica;
- `gsc_analise.md` tiver sido gerado com camada mínima de evidência numérica;
- `resumo_executivo.md` tiver sido gerado com sustentação numérica para as conclusões principais.

Uma competência estará operacionalmente concluída somente quando:

- o usuário aprovar explicitamente o resumo executivo;
- o histórico for atualizado;
- o changelog for atualizado;
- o `manifest.json` registrar a conclusão.

Uma competência estará pronta para entrega ao cliente somente quando:

- o DOCX tiver sido gerado;
- o PDF tiver sido gerado;
- os arquivos finais estiverem armazenados em `output/`.

---

# Benefícios Esperados

- Redução do volume de leitura para o cliente.
- Maior foco em tomada de decisão.
- Preservação da documentação técnica para auditoria.
- Padronização das entregas mensais.
- Construção de histórico consistente.
- Facilidade para comparações de longo prazo.
- Processo escalável para vários anos de acompanhamento.
- Eliminação da renomeação manual dos arquivos exportados.
- Maior robustez na identificação automática dos relatórios.
- Redução do tempo operacional de preparação das competências.

---

# Evoluções Futuras

Possíveis evoluções do projeto:

- leitura automática dos PDFs exportados;
- organização automática dos arquivos nas pastas corretas;
- consolidação integrada dos dados;
- comparação automática com histórico acumulado;
- geração automática do resumo executivo;
- exportação automatizada de DOCX e PDF após aprovação;
- integração direta com SEMrush, GA4 e Google Search Console;
- atualização automática dos indicadores históricos;
- implementação de análises preditivas para antecipar tendências e riscos.

Essas evoluções devem preservar a arquitetura central: competência autocontida, validação antes de análise, revisão humana antes de encerramento e separação entre evidência técnica, análise intermediária e entrega final.