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
- a escrita executiva orientada à tomada de decisão;
- a inclusão de evidências numéricas mínimas para sustentar conclusões.

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
15. Aplicar a camada mínima de evidência numérica.
16. Gerar o resumo executivo em `output/resumo_executivo.md`.
17. Interromper a execução para revisão humana.

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

# Camada Mínima de Evidência Numérica

O relatório não deve repetir o Looker Studio, mas também não pode omitir os números essenciais que sustentam a leitura executiva.

Toda afirmação de crescimento, queda, avanço, regressão, estabilidade, perda de eficiência ou ganho de eficiência deve estar acompanhada de pelo menos uma evidência numérica direta.

Sempre que os dados estiverem disponíveis, informar:

- valor do mês atual;
- valor do mês anterior;
- variação absoluta;
- variação percentual.

A camada mínima de evidência deve aparecer tanto nas análises individuais quanto no resumo executivo, de forma sintética e interpretativa.

Não criar tabelas, salvo solicitação explícita do usuário.

Não listar todas as métricas disponíveis.

Selecionar apenas os números necessários para comprovar a leitura executiva.

---

# Indicadores Mínimos Obrigatórios por Fonte

## GA4

A análise individual de GA4 deve incluir, quando disponíveis:

- sessões;
- usuários;
- novos usuários;
- sessões engajadas;
- taxa de engajamento;
- tempo médio de engajamento;
- eventos principais ou key events;
- canal Organic Search;
- canal Direct;
- principais páginas com ganho;
- principais páginas com queda;
- principais países ou grupos com ganho;
- principais países ou grupos com queda.

Para cada indicador principal, registrar valor atual, valor anterior, variação absoluta e variação percentual.

Para páginas, países e canais, priorizar os itens com maior impacto no período, não listas extensas.

## Google Search Console

A análise individual de GSC deve incluir, quando disponíveis:

- cliques;
- impressões;
- CTR;
- posição média;
- principais páginas com ganho;
- principais páginas com queda;
- principais queries com ganho;
- principais queries com queda;
- principais países com ganho;
- principais países com queda.

Para cada indicador principal, registrar valor atual, valor anterior, variação absoluta e variação percentual.

Para páginas, queries e países, priorizar os itens que explicam a tese central do período.

---

# Evidências Numéricas no Resumo Executivo

O `resumo_executivo.md` deve conter um bloco curto de sustentação numérica dentro do `Resumo Geral` ou logo após ele.

Esse bloco deve incluir, quando disponíveis:

- principais variações de GA4;
- principais variações de GSC;
- páginas que mais explicam ganho e queda;
- queries que mais explicam ganho e queda;
- países ou grupos com maior impacto no período.

O bloco deve ser curto e interpretativo.

Exemplo de formato esperado:

```text
Em junho, as sessões passaram de X para Y, variação de Z%, enquanto os usuários passaram de X para Y. No Search Console, as impressões cresceram de X para Y, mas os cliques caíram de X para Y e a CTR passou de A% para B%. Esse comportamento sustenta a leitura de maior exposição orgânica com menor eficiência de captura.
```

---

# Regra de Equilíbrio entre Síntese e Evidência

Evitar excesso de números não significa omitir números essenciais.

O relatório deve manter linguagem executiva, mas precisa permitir auditoria mínima da conclusão.

Não escrever apenas:

```text
O tráfego caiu no período.
```

Escrever:

```text
As sessões caíram de X para Y, variação de Z%, indicando retração de acesso no período.
```

Não escrever apenas:

```text
A CTR piorou.
```

Escrever:

```text
A CTR passou de X% para Y%, enquanto as impressões cresceram, indicando perda de eficiência na conversão de visibilidade orgânica em clique.
```

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
- leitura estratégica do comportamento observado;
- camada mínima de evidência numérica.

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
- leitura estratégica do desempenho orgânico;
- camada mínima de evidência numérica.

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
- Nunca omitir números essenciais necessários para sustentar conclusões executivas.
- Nunca afirmar crescimento, queda, avanço, regressão ou perda de eficiência sem evidência numérica quando os dados estiverem disponíveis.
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
- Sempre aplicar a camada mínima de evidência numérica.
- Sempre interromper a execução após gerar `resumo_executivo.md`.

---

# Estrutura Obrigatória do Resumo Executivo

O arquivo `resumo_executivo.md` deve seguir a estrutura abaixo.

## 1. Resumo Geral

Apresentar a leitura executiva do período.

Responder:

- o desempenho geral evoluiu, regrediu ou ficou estável;
- quais números sustentam essa leitura;
- quais fatores explicam o comportamento observado;
- quais canais, países, conteúdos ou indicadores foram decisivos;
- qual é o impacto geral para o projeto.

O Resumo Geral deve incluir um bloco curto de evidências numéricas mínimas.

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

Cada ponto forte deve incluir evidência numérica quando se referir a crescimento, avanço, ganho ou melhora.

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

Cada ponto de atenção deve incluir evidência numérica quando se referir a queda, piora, perda ou regressão.

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

A necessidade de evidência numérica não autoriza transformar o resumo executivo em relatório operacional extenso.

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