

# Prompt Mestre - Relatório Executivo Mensal

## Objetivo
Este prompt é responsável por gerar o relatório executivo mensal a partir de todos os PDFs do período de competência, correlacionando informações entre as fontes, em vez de apenas resumir arquivos individualmente.

## Entradas
- `START_HERE.md`
- `README.md`
- `prompts/00_MASTER_SPECIFICATION.md`
- Todos os arquivos da pasta `prompts/`
- Todos os arquivos da pasta `knowledge/`
- Arquivos da pasta `history/`
- Competência mensal mais recente em `reports/AAAA-MM/`
- Arquivo `reports/AAAA-MM/manifest.json`
- PDFs localizados exclusivamente em `reports/AAAA-MM/source/`

## Fluxo Obrigatório
1. Ler `START_HERE.md`.
2. Ler `README.md`.
3. Ler `prompts/00_MASTER_SPECIFICATION.md`.
4. Ler todos os demais arquivos da pasta `prompts/`.
5. Ler todos os arquivos da pasta `knowledge/`.
6. Ler o histórico disponível em `history/`.
7. Identificar automaticamente a competência mensal mais recente em `reports/`.
8. Validar a existência e o conteúdo do `manifest.json` da competência.
9. Confirmar que todos os relatórios obrigatórios estão presentes em `source/`.
10. Ler os PDFs da competência exclusivamente a partir de `source/`.
11. Gerar as análises individuais de GA4 e Google Search Console em `analysis/`.
12. Correlacionar informações entre GA4, GSC, Auditoria, SEO Checker, Backlinks, Keyword Strategy e Monitoramento de Posição.
13. Comparar as conclusões com o histórico disponível.
14. Priorizar os fatos mais relevantes.
15. Gerar o resumo executivo em `output/`.

## Validação da Competência
Antes de qualquer leitura analítica, validar a competência selecionada.

A execução deve ser interrompida se:

- `manifest.json` não existir.
- Houver relatório obrigatório ausente.
- Os PDFs estiverem fora da pasta `source/`.
- A competência estiver ambígua.
- Houver mistura de arquivos de competências diferentes.

Não gerar relatório parcial quando a competência estiver incompleta.

## Hierarquia das Fontes
- **Muito alta:** Google Analytics 4, Google Search Console.
- **Alta:** Monitoramento de Posição, Auditoria do Site.
- **Média:** Backlinks, On Page SEO Checker.
- **Baixa:** Keyword Strategy Tool.

## Regras Obrigatórias
- Nunca resumir PDF individualmente.
- Produzir visão consolidada.
- Não repetir métricas já existentes no Dashboard.
- Explicar causas, impactos e recomendações.
- Priorizar tendências sobre eventos isolados.
- Destacar riscos e oportunidades.
- Limite máximo aproximado de duas páginas.
- Validar `manifest.json` antes da leitura dos PDFs.
- Ler PDFs apenas em `reports/AAAA-MM/source/`.
- Gravar análises individuais apenas em `reports/AAAA-MM/analysis/`.
- Gravar o resumo executivo apenas em `reports/AAAA-MM/output/`.
- Nunca misturar dados de competências diferentes.
- Interromper a execução se arquivos obrigatórios estiverem ausentes.

## Estrutura Obrigatória da Saída
1. Resumo Geral.
2. Pontos Fortes.
3. Pontos de Atenção.
4. Impacto Geral no Projeto.
5. Recomendações Priorizadas.

## Saídas Obrigatórias
A execução deve produzir:

- `reports/AAAA-MM/analysis/ga4_analise.md`
- `reports/AAAA-MM/analysis/gsc_analise.md`
- `reports/AAAA-MM/output/resumo_executivo.md`

A versão `.docx` poderá ser produzida posteriormente a partir do Markdown final.

## Estilo de Escrita
O relatório deve ser redigido como um documento executivo de consultoria, nunca mencionando PDFs, relatórios ou nomes de arquivos, e nunca utilizando expressões como "o relatório mostra" ou "segundo o PDF". Utilizar linguagem analítica e direta.

A escrita deve ser sintética, executiva e voltada para tomada de decisão. O texto final não deve parecer um resumo automatizado, mas uma análise consultiva consolidada.
# 01 PROMPT RELATÓRIO EXECUTIVO

# Relatório Executivo Mensal SFTL

## Objetivo

Este prompt define como gerar o Relatório Executivo Mensal do projeto Solve for Tomorrow Latam a partir da competência ativa em `reports/AAAA-MM/`.

O objetivo não é resumir PDFs individualmente. O objetivo é consolidar os principais achados do período, cruzando as fontes disponíveis, identificando tendências, impactos, riscos e recomendações estratégicas para o projeto.

O relatório executivo deve funcionar como o principal entregável analítico mensal, complementar ao dashboard operacional no Looker Studio.

---

# Responsabilidade deste Prompt

Este prompt é responsável por orientar:

- a geração das análises individuais obrigatórias de GA4 e Google Search Console;
- a consolidação do `resumo_executivo.md`;
- a priorização dos achados mais relevantes;
- a diferenciação entre fato, hipótese e recomendação;
- a escrita executiva orientada à tomada de decisão.

Este prompt não é responsável por gerar DOCX ou PDF.

Os arquivos DOCX e PDF devem ser gerados posteriormente no ChatGPT, após revisão humana e aprovação do Markdown final.

---

# Entradas Obrigatórias

Antes de gerar qualquer análise, devem estar disponíveis:

- `START_HERE.md`
- `README.md`
- `prompts/00_MASTER_SPECIFICATION.md`
- todos os demais arquivos da pasta `prompts/`
- todos os arquivos da pasta `knowledge/`
- arquivos disponíveis na pasta `history/`
- competência ativa em `reports/AAAA-MM/`
- arquivo `reports/AAAA-MM/manifest.json`
- PDFs localizados exclusivamente em `reports/AAAA-MM/source/`

A competência ativa deve ser validada antes de qualquer leitura analítica.

---

# Fontes de Dados

## Fontes obrigatórias

As fontes obrigatórias para a competência são:

- Google Analytics 4
- Google Search Console

Essas fontes devem gerar análises individuais obrigatórias em Markdown.

## Fontes complementares

As fontes complementares podem incluir, quando disponíveis:

- SEMrush Backlinks
- SEMrush Monitoramento de Posição
- SEMrush Auditoria do Site
- SEMrush On Page SEO Checker
- SEMrush Keyword Strategy
- baseline histórico
- histórico mensal do projeto

Fontes complementares não geram análises individuais obrigatórias, salvo solicitação explícita do usuário.

Elas devem ser utilizadas para enriquecer o resumo executivo quando houver evidência relevante.

---

# Fluxo Obrigatório

Executar o processo nesta ordem:

1. Ler `START_HERE.md`.
2. Ler `README.md`.
3. Ler `prompts/00_MASTER_SPECIFICATION.md`.
4. Ler todos os demais arquivos da pasta `prompts/`.
5. Ler todos os arquivos da pasta `knowledge/`.
6. Ler o histórico disponível em `history/`.
7. Identificar a competência ativa em `reports/AAAA-MM/`.
8. Validar a existência e o conteúdo do `manifest.json` da competência.
9. Confirmar que os relatórios obrigatórios estão presentes em `source/`.
10. Ler exclusivamente os PDFs da competência ativa em `source/`.
11. Gerar a análise individual de GA4 em `analysis/ga4_analise.md`.
12. Gerar a análise individual de Google Search Console em `analysis/gsc_analise.md`.
13. Correlacionar GA4, GSC, histórico, baseline e fontes complementares disponíveis.
14. Priorizar os achados mais relevantes do período.
15. Gerar o resumo executivo em `output/resumo_executivo.md`.
16. Interromper a execução para revisão humana.

Nenhuma etapa de geração de DOCX ou PDF deve ocorrer neste fluxo.

---

# Validação da Competência

Antes de qualquer leitura analítica, validar a competência selecionada.

A execução deve ser interrompida se:

- `manifest.json` não existir;
- `manifest.json` estiver inconsistente com a pasta `source/`;
- houver relatório obrigatório ausente;
- os PDFs estiverem fora da pasta `source/`;
- a competência estiver ambígua;
- houver mistura de arquivos de competências diferentes;
- houver duplicidade crítica que impeça a identificação correta das fontes.

Não gerar relatório parcial quando a competência estiver incompleta.

---

# Hierarquia das Fontes

A leitura deve respeitar a seguinte hierarquia:

## Prioridade muito alta

- Google Analytics 4
- Google Search Console

Essas fontes sustentam as conclusões principais sobre tráfego, engajamento, visibilidade orgânica e performance de busca.

## Prioridade alta

- SEMrush Monitoramento de Posição
- SEMrush Auditoria do Site
- baseline histórico
- histórico mensal do projeto

Essas fontes ajudam a contextualizar evolução de ranking, estabilidade técnica e tendência de longo prazo.

## Prioridade média

- SEMrush Backlinks
- SEMrush On Page SEO Checker

Essas fontes ajudam a qualificar autoridade, oportunidades de link building e ajustes estruturais.

## Prioridade baixa

- SEMrush Keyword Strategy
- demais materiais complementares

Essas fontes devem ser utilizadas apenas quando trouxerem evidência útil para oportunidade, expansão de conteúdo ou planejamento estratégico.

---

# Análises Individuais Obrigatórias

## GA4

Gerar:

```text
reports/AAAA-MM/analysis/ga4_analise.md
```

A análise deve cobrir:

- tráfego geral;
- usuários;
- usuários novos e recorrentes;
- canais de aquisição;
- páginas mais acessadas;
- países e regiões relevantes;
- dispositivos quando houver impacto estratégico;
- engajamento;
- eventos e key events;
- variações relevantes frente ao mês anterior;
- leitura estratégica do comportamento observado.

## Google Search Console

Gerar:

```text
reports/AAAA-MM/analysis/gsc_analise.md
```

A análise deve cobrir:

- cliques;
- impressões;
- CTR;
- posição média;
- páginas com maior impacto orgânico;
- consultas mais relevantes;
- países quando aplicável;
- crescimento ou retração de visibilidade;
- oportunidades de SEO;
- leitura estratégica do desempenho orgânico.

Essas análises devem apoiar o resumo executivo, não substituir o resumo executivo.

---

# Correlação Obrigatória

O resumo executivo deve cruzar as fontes em vez de tratá-las isoladamente.

Exemplos de correlação esperada:

- se o tráfego orgânico cresceu no GA4, verificar se houve aumento de cliques ou impressões no GSC;
- se o GSC mostra queda de CTR, avaliar se houve perda de tráfego orgânico no GA4;
- se a visibilidade regional mudou, verificar se o comportamento aparece também em países ou grupos no GA4;
- se SEMrush indicar ganho ou perda de posições, usar isso como apoio para explicar variações orgânicas;
- se backlinks ou autoridade evoluíram, relacionar com crescimento estrutural de SEO, sem afirmar causalidade direta sem evidência.

A análise deve priorizar relações com impacto estratégico.

---

# Tratamento de Hipóteses

Quando a causa de uma variação não puder ser confirmada, declarar como hipótese.

Usar linguagem como:

- A hipótese mais provável é...
- Os dados sugerem...
- Há indícios de...
- Não há evidência suficiente para afirmar causalidade direta.

Nunca transformar hipótese em fato.

Sempre diferenciar:

- fato observado;
- interpretação provável;
- recomendação decorrente.

---

# Regras Obrigatórias

- Nunca resumir PDFs individualmente.
- Nunca citar nomes de arquivos no texto final do resumo executivo.
- Nunca utilizar expressões como `o PDF mostra`, `o relatório aponta` ou `segundo o arquivo`.
- Nunca analisar PDFs fora da competência ativa.
- Nunca misturar dados de competências diferentes.
- Nunca gerar análise antes da validação do `manifest.json`.
- Nunca depender de renomeação manual dos PDFs.
- Nunca repetir métricas operacionais em excesso quando elas já estiverem disponíveis no Looker Studio.
- Nunca transformar hipótese em fato.
- Nunca apresentar causalidade sem evidência suficiente.
- Nunca gerar DOCX ou PDF neste fluxo.
- Sempre produzir visão consolidada.
- Sempre explicar causas prováveis, impactos e recomendações.
- Sempre priorizar tendências sobre eventos isolados.
- Sempre destacar riscos e oportunidades.
- Sempre validar `manifest.json` antes da leitura dos PDFs.
- Sempre ler PDFs apenas em `reports/AAAA-MM/source/`.
- Sempre gravar análises individuais apenas em `reports/AAAA-MM/analysis/`.
- Sempre gravar o resumo executivo apenas em `reports/AAAA-MM/output/`.
- Sempre interromper a execução após gerar `resumo_executivo.md`.

---

# Estrutura Obrigatória do Resumo Executivo

O arquivo `resumo_executivo.md` deve seguir a estrutura abaixo.

## 1. Resumo Geral

Apresentar a leitura executiva do período.

Responder:

- o desempenho geral evoluiu, regrediu ou ficou estável;
- quais fatores explicam o comportamento observado;
- quais canais, países, conteúdos ou indicadores foram decisivos;
- qual é o impacto geral para o projeto.

## 2. Pontos Fortes

Destacar os avanços mais relevantes do mês.

Priorizar:

- crescimento qualificado de tráfego;
- melhora de visibilidade orgânica;
- evolução de páginas estratégicas;
- crescimento regional relevante;
- avanço de engajamento;
- evolução estrutural de SEO;
- fortalecimento de autoridade quando houver evidência.

## 3. Pontos de Atenção

Destacar os principais riscos, quedas ou limitações do período.

Priorizar:

- perda de tráfego relevante;
- queda de cliques ou impressões orgânicas;
- redução de CTR;
- piora de posição média;
- dependência excessiva de poucos canais ou páginas;
- queda em países estratégicos;
- problemas técnicos ou estruturais com impacto potencial.

## 4. Impacto Geral no Projeto

Responder objetivamente:

```text
O projeto evoluiu, regrediu ou permaneceu estável neste período?
```

A resposta deve sintetizar o impacto para SEO, tráfego, visibilidade regional e evolução institucional do projeto.

Quando necessário, indicar nível de confiança da leitura.

## 5. Recomendações Priorizadas

Listar recomendações práticas por prioridade.

### Alta prioridade

Ações com impacto direto em tráfego, visibilidade, indexação, autoridade, estabilidade técnica ou mitigação de risco relevante.

### Média prioridade

Ações de otimização, expansão de conteúdo, melhoria de CTR, fortalecimento de links internos, atualização de páginas e ajustes estratégicos.

### Baixa prioridade

Ações complementares, refinamentos futuros e melhorias que não bloqueiam o desempenho atual.

---

# Estilo de Escrita

O relatório deve ser redigido como documento executivo de consultoria.

A escrita deve ser:

- direta;
- analítica;
- sintética;
- objetiva;
- consultiva;
- orientada à decisão.

Evitar:

- tom operacional excessivo;
- transcrição de métricas;
- linguagem de resumo automatizado;
- repetição de números sem interpretação;
- afirmações categóricas sem evidência.

O texto final deve parecer uma análise consolidada feita por consultoria, não um resumo automático de arquivos exportados.

---

# Limite de Tamanho

O resumo executivo deve ter no máximo duas páginas em sua versão final.

A versão Markdown pode ser ligeiramente mais detalhada para facilitar revisão humana, mas deve manter concisão suficiente para conversão posterior em DOCX e PDF.

---

# Saídas Obrigatórias

A execução deve produzir:

```text
reports/AAAA-MM/analysis/ga4_analise.md
reports/AAAA-MM/analysis/gsc_analise.md
reports/AAAA-MM/output/resumo_executivo.md
```

Após produzir esses arquivos, interromper para revisão humana.

Não gerar DOCX ou PDF nesta etapa.