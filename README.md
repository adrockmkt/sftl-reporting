# SFTL Reporting

## Objetivo

Este repositório centraliza o processo de geração dos Relatórios Executivos Mensais do projeto Solve for Tomorrow Latam (SFTL).

O objetivo é transformar relatórios técnicos exportados do Google Analytics 4, Google Search Console e SEMrush em um fluxo estruturado de análise, com rastreabilidade dos arquivos originais, geração de análises intermediárias e produção de um relatório executivo final orientado à tomada de decisão.

O repositório foi desenhado para funcionar em duas etapas complementares:

1. Pipeline operacional no Codex, responsável por organizar a competência mensal, validar os arquivos, gerar análises técnicas e consolidar o resumo executivo em Markdown.
2. Finalização editorial no ChatGPT, responsável por revisar o resumo executivo aprovado e gerar os documentos finais em DOCX e PDF para entrega ao cliente.

---

## Escopo do Repositório

Este repositório cobre:

- organização mensal dos relatórios exportados;
- validação da estrutura de arquivos;
- geração do inventário da competência;
- análise individual de Google Analytics 4;
- análise individual de Google Search Console;
- consolidação do relatório executivo mensal;
- manutenção do histórico analítico do projeto;
- atualização da base de conhecimento metodológica;
- preparação da base para geração final em DOCX e PDF.

Este repositório não substitui o dashboard operacional no Looker Studio. Ele funciona como camada de análise executiva, documentação e fechamento mensal.

---

## Estrutura do Projeto

```text
START_HERE.md            -> Ponto de entrada operacional do projeto
README.md                -> Visão geral da arquitetura e do fluxo de trabalho

knowledge/               -> Base permanente de conhecimento do projeto
prompts/                 -> Prompts, regras e metodologia de análise
history/                 -> Histórico consolidado e evolução mensal
reports/                 -> Competências mensais
│
├── AAAA-MM/
│   ├── source/          -> PDFs originais exportados
│   ├── analysis/        -> Análises individuais de GA4 e GSC
│   ├── output/          -> Resumo executivo e documentos finais
│   └── manifest.json    -> Inventário e validação da competência
templates/               -> Modelos utilizados nas entregas
scripts/                 -> Scripts de automação e validação
```

---

## Organização das Competências

Cada competência mensal deve possuir uma pasta própria dentro de `reports/`.

Exemplo:

```text
reports/
└── 2026-06/
    ├── source/
    ├── analysis/
    ├── output/
    └── manifest.json
```

Cada competência deve ser autocontida. Isso significa que os arquivos originais, análises intermediárias, entregáveis finais e inventário da competência devem permanecer dentro da própria pasta mensal.

Essa estrutura evita perda de contexto, facilita auditoria futura e permite comparar a evolução mês a mês com maior segurança.

---

## Estrutura Interna de Cada Competência

Estrutura padrão:

```text
reports/
└── AAAA-MM/
    ├── source/
    │   └── PDFs originais exportados
    │
    ├── analysis/
    │   ├── ga4_analise.md
    │   └── gsc_analise.md
    │
    ├── output/
    │   ├── resumo_executivo.md
    │   ├── resumo_executivo.docx
    │   └── resumo_executivo.pdf
    │
    └── manifest.json
```

Responsabilidade de cada diretório:

- `source/`: preserva os PDFs técnicos originais exportados das ferramentas.
- `analysis/`: armazena apenas as análises individuais de Google Analytics 4 e Google Search Console.
- `output/`: armazena exclusivamente os entregáveis finais da competência.
- `manifest.json`: registra os arquivos esperados, os arquivos encontrados, o tipo de cada relatório e o status de validação da competência.

Não deve existir mistura entre evidências, análises intermediárias e entregáveis finais.

---

## Convenção dos Arquivos Originais

Os relatórios exportados do Google Analytics 4, Google Search Console e SEMrush devem ser armazenados em `source/` exatamente com os nomes gerados pelas ferramentas.

Não deve haver renomeação manual dos PDFs.

A identificação de cada relatório deve ser realizada pelo processo de análise, utilizando padrões conhecidos nos nomes dos arquivos exportados.

O arquivo `manifest.json` é responsável por registrar o mapeamento entre os nomes físicos dos PDFs e os tipos de relatório esperados.

Essa abordagem reduz trabalho manual, preserva a rastreabilidade dos arquivos originais e mantém compatibilidade com futuras exportações das ferramentas.

---

## Fontes de Dados

O fluxo considera os seguintes tipos de relatório:

- Google Analytics 4, para análise de tráfego, canais, páginas, países, eventos e engajamento.
- Google Search Console, para análise de cliques, impressões, CTR, posição média, páginas e consultas orgânicas.
- SEMrush, para suporte estratégico com backlinks, monitoramento de posição e indicadores complementares de SEO.

Na versão operacional atual, o pipeline do Codex gera análises individuais obrigatórias para GA4 e Google Search Console. Os dados de SEMrush podem ser utilizados como apoio estratégico, baseline ou complemento metodológico, conforme a competência.

---

## Fluxo de Trabalho Operacional

### 1. Preparação da competência

O usuário inicia o processo a partir do `START_HERE.md`, informando a competência mensal que será analisada.

O Codex deve:

- validar a arquitetura do repositório;
- criar a pasta da competência caso ela não exista;
- criar os diretórios `source/`, `analysis/` e `output/`;
- gerar ou validar o `manifest.json` inicial.

Após essa etapa, o Codex deve interromper a execução e solicitar:

```text
Copie todos os PDFs para:

reports/AAAA-MM/source/

Quando terminar, responda apenas:

CONTINUAR
```

---

### 2. Validação dos arquivos

Somente após o usuário responder `CONTINUAR`, o Codex deve:

- validar a existência da pasta da competência;
- listar os PDFs encontrados em `source/`;
- identificar os tipos de relatório disponíveis;
- verificar se os relatórios obrigatórios estão presentes;
- atualizar o `manifest.json`;
- interromper a execução caso exista qualquer inconsistência crítica.

Nenhuma análise deve ser gerada antes da validação dos arquivos.

---

### 3. Geração das análises técnicas

Após a validação, o Codex deve gerar os seguintes arquivos:

```text
reports/AAAA-MM/analysis/ga4_analise.md
reports/AAAA-MM/analysis/gsc_analise.md
```

Cada análise deve seguir os templates e regras metodológicas definidos em `templates/`, `prompts/` e `knowledge/`.

As análises devem priorizar:

- leitura executiva dos dados;
- comparação com o mês anterior;
- identificação de tendências;
- impactos estratégicos;
- pontos de atenção;
- recomendações acionáveis.

---

### 4. Consolidação do resumo executivo

Depois das análises individuais, o Codex deve gerar:

```text
reports/AAAA-MM/output/resumo_executivo.md
```

O resumo executivo deve consolidar os principais achados das análises de GA4 e Google Search Console, evitando repetição excessiva e priorizando leitura de negócio.

O documento deve ser adequado para revisão humana antes da geração final em DOCX e PDF.

---

### 5. Revisão humana

Após gerar o `resumo_executivo.md`, o Codex deve interromper novamente a execução e solicitar validação do usuário.

O pipeline não deve atualizar histórico, changelog ou status final antes da aprovação humana.

---

### 6. Encerramento da competência

Após aprovação do usuário, o Codex deve:

- atualizar `history/`;
- atualizar `knowledge/11_CHANGELOG.md`;
- registrar a competência como concluída;
- encerrar o pipeline operacional da competência.

A partir desse ponto, a etapa do Codex é considerada finalizada.

---

## Finalização Editorial no ChatGPT

A geração dos documentos finais para entrega ao cliente deve ser feita em conjunto com o ChatGPT, utilizando como base:

```text
reports/AAAA-MM/output/resumo_executivo.md
```

Após a revisão final, o ChatGPT deve produzir:

```text
reports/AAAA-MM/output/resumo_executivo.docx
reports/AAAA-MM/output/resumo_executivo.pdf
```

Essa separação mantém o pipeline operacional limpo e reserva a etapa final para ajustes editoriais, formatação e adequação do relatório ao padrão de entrega ao cliente.

---

## Entregáveis

Os entregáveis do processo completo são:

- Dashboard operacional no Looker Studio.
- PDFs técnicos originais preservados como evidência.
- Análise individual do Google Analytics 4.
- Análise individual do Google Search Console.
- Relatório Executivo Mensal consolidado em Markdown.
- Relatório Executivo Mensal em DOCX.
- Relatório Executivo Mensal em PDF.

---

## Regras de Qualidade

O processo deve respeitar as seguintes regras:

- Cada competência deve ser autocontida.
- Os PDFs originais devem ser preservados sem renomeação manual.
- Nenhuma análise deve ser criada antes da validação dos arquivos.
- As análises individuais devem permanecer em `analysis/`.
- Os entregáveis finais devem permanecer em `output/`.
- O `manifest.json` deve refletir o estado real da competência.
- A competência só deve ser encerrada após revisão humana.
- O histórico e o changelog só devem ser atualizados após aprovação.
- A análise deve priorizar decisão executiva, não apenas transcrição de métricas.

---

## Princípios Analíticos

O relatório mensal deve seguir estes princípios:

- Uma única análise executiva por competência.
- Correlação entre fontes de dados.
- Foco em tendência, impacto e decisão.
- Preservação dos PDFs como evidência técnica.
- Consistência metodológica entre competências.
- Comparabilidade mês a mês.
- Separação clara entre dado bruto, análise intermediária e entrega final.

---

## Papel do Baseline e da Base de Conhecimento

A pasta `knowledge/` concentra documentos de referência permanente do projeto, incluindo baseline histórico, framework de monitoramento e changelog metodológico.

Esses documentos devem ser utilizados para manter consistência nas análises e preservar a evolução estratégica do projeto ao longo do tempo.

O baseline não deve ser sobrescrito mensalmente. Caso uma nova referência histórica seja necessária, deve ser criada uma nova versão documentada.

---

## Evolução do Repositório

A arquitetura foi projetada para crescer continuamente por meio da atualização da base de conhecimento, histórico do projeto, regras de análise e automações.

O objetivo é manter estabilidade metodológica, reduzir trabalho manual e garantir que cada relatório mensal possa ser auditado, revisado e comparado com períodos anteriores.
