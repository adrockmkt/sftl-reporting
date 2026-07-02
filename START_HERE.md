# START HERE

## Objetivo

Este documento é o ponto de entrada oficial do projeto SFTL Reporting.

Toda execução de uma nova competência mensal deve iniciar obrigatoriamente por este arquivo.

Seu objetivo é orientar o Codex na execução padronizada do pipeline mensal, garantindo consistência metodológica, rastreabilidade dos arquivos originais, validação da competência e geração das análises intermediárias antes da revisão humana.

Este documento não substitui o `README.md`. O `README.md` descreve a arquitetura geral do repositório. Este arquivo define a ordem operacional que deve ser seguida em cada competência.

---

# Princípio Central

O fluxo do projeto é dividido em duas responsabilidades complementares:

1. Codex: preparação da competência, validação dos arquivos, geração das análises técnicas e consolidação do resumo executivo em Markdown.
2. ChatGPT: revisão editorial final e geração dos arquivos DOCX e PDF para entrega ao cliente.

O Codex não deve gerar DOCX ou PDF durante o pipeline operacional. A geração desses formatos deve ocorrer somente após revisão humana e finalização editorial no ChatGPT.

---

# Fluxo Operacional

Toda competência deve seguir obrigatoriamente as fases abaixo.

---

# FASE 1 • Preparação da Competência

Executar quando uma nova competência mensal for iniciada.

O Codex deve:

- ler o `README.md`;
- validar a arquitetura do projeto;
- validar a estrutura de pastas;
- localizar a competência solicitada;
- criar a estrutura da competência caso ainda não exista;
- criar ou validar os diretórios `source/`, `analysis/` e `output/`;
- gerar ou validar o `manifest.json` inicial;
- interromper a execução caso existam problemas estruturais críticos.

Nesta fase ainda não devem existir análises.

Ao final da fase, o Codex deve solicitar ao usuário:

```text
Copie todos os PDFs para:

reports/AAAA-MM/source/

Quando terminar, responda apenas:

CONTINUAR
```

---

# FASE 2 • Importação dos Relatórios

Após a preparação da competência, o usuário deve:

1. Exportar todos os relatórios das ferramentas utilizadas.
2. Copiar todos os PDFs para:

```text
reports/AAAA-MM/source/
```

Regras obrigatórias:

- manter exatamente os nomes originais exportados pelas ferramentas;
- nunca renomear PDFs manualmente;
- nunca alterar a estrutura das pastas;
- não copiar arquivos de outras competências;
- não substituir arquivos históricos sem necessidade explícita.

A identificação dos relatórios deve ocorrer automaticamente a partir dos nomes dos arquivos e do conteúdo validado pelo pipeline.

---

# FASE 3 • Validação dos Arquivos

Somente após o usuário responder `CONTINUAR`, o Codex deve:

- validar a existência da pasta da competência;
- listar todos os PDFs presentes em `source/`;
- identificar o tipo de cada relatório encontrado;
- validar a presença dos relatórios obrigatórios;
- atualizar o `manifest.json` com os arquivos encontrados;
- registrar inconsistências, ausências ou duplicidades;
- interromper imediatamente a execução caso exista inconsistência crítica.

Nenhuma análise deve ser produzida antes desta validação.

Não produzir análises parciais quando houver ausência de relatório obrigatório.

---

# FASE 4 • Análise Técnica

Após a validação da competência e dos PDFs, o Codex deve executar:

- leitura dos documentos obrigatórios de contexto;
- leitura dos PDFs da competência ativa;
- geração da análise individual de Google Analytics 4;
- geração da análise individual de Google Search Console;
- consolidação do resumo executivo mensal em Markdown.

Arquivos obrigatórios gerados nesta fase:

```text
reports/AAAA-MM/analysis/ga4_analise.md
reports/AAAA-MM/analysis/gsc_analise.md
reports/AAAA-MM/output/resumo_executivo.md
```

Após gerar esses arquivos, a execução deve ser interrompida para revisão humana.

Nenhum arquivo DOCX ou PDF deve ser gerado nesta fase.

---

# FASE 5 • Revisão Humana

Após a geração do `resumo_executivo.md`, o usuário deve revisar o conteúdo.

Caso sejam solicitados ajustes, o Codex deve alterar apenas os arquivos Markdown correspondentes dentro da competência ativa.

O Codex não deve atualizar histórico, changelog ou status final enquanto o relatório não estiver aprovado.

---

# FASE 6 • Encerramento Operacional

Após aprovação explícita do usuário, o Codex deve:

- atualizar o histórico do projeto em `history/`;
- atualizar o changelog em `knowledge/11_CHANGELOG.md`;
- registrar a competência como concluída no `manifest.json`;
- encerrar o pipeline operacional da competência.

A geração de DOCX e PDF permanece como etapa posterior de finalização editorial no ChatGPT.

---

# FASE 7 • Finalização Editorial no ChatGPT

Após o encerramento operacional, o ChatGPT deve utilizar como base:

```text
reports/AAAA-MM/output/resumo_executivo.md
```

A partir desse arquivo aprovado, devem ser gerados os documentos finais:

```text
reports/AAAA-MM/output/resumo_executivo.docx
reports/AAAA-MM/output/resumo_executivo.pdf
```

Essa etapa deve preservar o conteúdo aprovado, ajustando apenas formatação, clareza editorial e adequação ao padrão de entrega ao cliente.

---

# Carregamento Obrigatório do Contexto

Toda execução deve seguir exatamente esta sequência de leitura antes da análise técnica.

---

## Etapa 1

Ler completamente:

```text
README.md
```

Objetivo:

Compreender a arquitetura geral do projeto, a separação entre pipeline operacional e finalização editorial, e a estrutura de competências mensais.

---

## Etapa 2

Ler completamente:

```text
prompts/00_MASTER_SPECIFICATION.md
```

Objetivo:

Compreender a arquitetura metodológica, as regras gerais e o padrão de execução do projeto.

---

## Etapa 3

Ler todos os documentos da pasta:

```text
prompts/
```

Na ordem:

1. `01_PROMPT_RELATORIO_EXECUTIVO.md`
2. `02_ESTILO_DE_ESCRITA.md`
3. `03_REGRAS_DE_ANALISE.md`
4. `04_GLOSSARIO.md`
5. `05_HISTORICO_DO_PROJETO.md`
6. `06_HIPOTESES_E_CONFIANCA.md`
7. `07_ESTILO_CONSULTIVO.md`

Todos devem permanecer ativos simultaneamente durante a execução.

---

## Etapa 4

Ler todos os documentos da pasta:

```text
knowledge/
```

Os arquivos devem ser carregados integralmente.

A leitura deve seguir a ordem numérica quando existir prefixo numérico no nome dos arquivos.

Nenhum arquivo obrigatório deve ser ignorado.

---

## Etapa 5

Ler todos os documentos disponíveis em:

```text
history/
```

Priorizar:

- `monthly/`
- `indicadores_historicos.csv`
- `evolucao_mensal.md`

Objetivo:

Compreender tendências históricas antes de analisar a competência atual.

---

## Etapa 6

Localizar automaticamente a competência ativa.

Validar:

- `manifest.json`;
- estrutura da competência;
- relatórios obrigatórios;
- integridade da pasta `source/`.

Caso o `manifest.json` não exista, ele deve ser gerado automaticamente.

Caso qualquer relatório obrigatório esteja ausente, a execução deve ser interrompida imediatamente.

---

## Etapa 7

Ler exclusivamente os PDFs presentes em:

```text
reports/AAAA-MM/source/
```

Os PDFs representam evidências técnicas da competência ativa.

Os PDFs não devem ser citados nominalmente no relatório executivo final, exceto quando isso for necessário para rastreabilidade interna.

---

## Etapa 8

Correlacionar todas as informações utilizando:

- regras de análise;
- metodologia consultiva;
- hipóteses e níveis de confiança;
- histórico;
- baseline;
- conhecimento permanente do projeto.

Sempre priorizar:

- causas prováveis;
- impactos estratégicos;
- tendências;
- riscos;
- recomendações acionáveis.

Nunca apenas resumir os PDFs.

---

# Regras Obrigatórias

- Nunca analisar PDFs fora da competência ativa.
- Nunca misturar competências diferentes.
- Nunca depender de renomeação manual.
- Nunca repetir números operacionais em excesso quando eles já estiverem disponíveis no Looker Studio.
- Nunca transformar hipótese em fato.
- Nunca apresentar causalidade sem evidência suficiente.
- Nunca gerar DOCX ou PDF antes da revisão humana.
- Sempre correlacionar diferentes fontes.
- Sempre utilizar o histórico quando disponível.
- Sempre utilizar a base da pasta `knowledge/`.
- Sempre validar o `manifest.json` antes da leitura analítica dos PDFs.
- Sempre gravar os arquivos dentro da competência analisada.
- Sempre produzir análises consultivas e orientadas à decisão.
- Sempre interromper a execução após gerar o `resumo_executivo.md`.
- Sempre atualizar histórico e changelog somente após aprovação explícita do usuário.

---

# Critério de Sucesso

Uma competência estará pronta para revisão humana quando:

- a arquitetura do projeto tiver sido validada;
- todos os documentos obrigatórios tiverem sido carregados;
- todos os PDFs obrigatórios tiverem sido validados;
- o `manifest.json` estiver atualizado;
- a análise de GA4 tiver sido gerada;
- a análise de Google Search Console tiver sido gerada;
- o resumo executivo em Markdown tiver sido gerado;
- todos os arquivos estiverem salvos dentro da competência ativa.

Uma competência somente poderá ser considerada concluída quando:

- o usuário aprovar explicitamente o resumo executivo;
- o histórico do projeto for atualizado;
- o changelog for atualizado;
- o `manifest.json` registrar a conclusão operacional.

Somente depois disso o relatório poderá seguir para finalização editorial em DOCX e PDF no ChatGPT.

---

# Resultado Esperado

Ao final do fluxo completo, a competência mensal deve conter:

```text
reports/AAAA-MM/source/
reports/AAAA-MM/analysis/ga4_analise.md
reports/AAAA-MM/analysis/gsc_analise.md
reports/AAAA-MM/output/resumo_executivo.md
reports/AAAA-MM/output/resumo_executivo.docx
reports/AAAA-MM/output/resumo_executivo.pdf
reports/AAAA-MM/manifest.json
```

Os arquivos DOCX e PDF só devem existir após a etapa de finalização editorial.

---

Este documento é o orquestrador oficial do projeto.

Toda competência deve iniciar obrigatoriamente por ele.
