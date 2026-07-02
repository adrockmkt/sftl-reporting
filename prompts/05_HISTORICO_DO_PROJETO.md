# 05 HISTÓRICO DO PROJETO

# Histórico Permanente do Projeto SFTL Reporting

## Objetivo

Este documento registra o contexto permanente do projeto SFTL Reporting.

Sua função é preservar decisões estruturais, premissas de longo prazo, objetivos permanentes e diretrizes históricas que devem orientar todas as competências mensais do projeto Solve for Tomorrow Latam.

Este arquivo não deve ser usado para registrar ocorrências operacionais de cada mês. Eventos mensais, variações de desempenho, hipóteses específicas e conclusões por competência devem ser registrados na pasta `history/`.

---

# Papel deste Documento

Este documento deve ser utilizado para:

- manter continuidade analítica entre competências;
- evitar perda de contexto metodológico;
- preservar decisões estruturais do projeto;
- orientar a leitura estratégica de longo prazo;
- impedir mudanças frequentes na filosofia de reporting;
- diferenciar decisões permanentes de ajustes operacionais.

Este documento complementa:

- `00_MASTER_SPECIFICATION.md`;
- `01_PROMPT_RELATORIO_EXECUTIVO.md`;
- `03_REGRAS_DE_ANALISE.md`;
- documentos da pasta `knowledge/`;
- registros acumulados em `history/`.

---

# Contexto Geral do Projeto

O Solve for Tomorrow Latam é um projeto educacional da Samsung voltado à inovação, educação STEM e desenvolvimento de projetos escolares na América Latina.

O acompanhamento digital do projeto considera o site:

```text
https://solvefortomorrowlatam.com/
```

O trabalho de reporting acompanha a evolução do projeto a partir de dados de tráfego, desempenho orgânico, posicionamento, autoridade digital e comportamento regional.

O projeto tem caráter internacional e envolve múltiplos países da América Latina, com análise segmentada por grupos regionais.

---

# Natureza do Projeto de Reporting

O SFTL Reporting é um projeto de SEO, Digital Analytics e documentação executiva de longo prazo.

Ele não tem como objetivo apenas produzir relatórios mensais. Seu objetivo central é construir uma base histórica confiável para avaliar:

- evolução do tráfego;
- crescimento da visibilidade orgânica;
- comportamento regional;
- desempenho dos conteúdos educacionais;
- fortalecimento da autoridade digital;
- oportunidades de expansão de SEO;
- riscos técnicos ou estratégicos;
- impacto das ações executadas ao longo do tempo.

---

# Fontes Históricas do Projeto

O monitoramento considera principalmente:

- Google Analytics 4;
- Google Search Console;
- SEMrush;
- Looker Studio;
- baseline histórico;
- registros acumulados em `history/`;
- documentos permanentes em `knowledge/`.

Na arquitetura atual, GA4 e Google Search Console são as fontes obrigatórias para análises individuais mensais.

SEMrush funciona como fonte complementar de apoio estratégico, especialmente para backlinks, monitoramento de posição, auditoria técnica e autoridade orgânica.

Looker Studio funciona como camada operacional de consulta e visualização de métricas.

---

# Objetivos Permanentes

Os objetivos permanentes do projeto são:

- aumentar a visibilidade orgânica qualificada nos países-alvo;
- fortalecer a descoberta de conteúdos educacionais;
- ampliar a presença do projeto em temas relacionados a STEM, inovação educacional e aprendizagem baseada em projetos;
- melhorar continuamente a leitura de tráfego e desempenho orgânico;
- monitorar a performance internacional por país e grupo regional;
- identificar riscos técnicos, editoriais e estratégicos com antecedência;
- apoiar decisões executivas com dados confiáveis;
- preservar histórico analítico para comparação de longo prazo;
- reduzir dependência de leitura manual dos PDFs técnicos;
- transformar dados operacionais em recomendações estratégicas.

---

# Premissas Permanentes

As premissas do projeto são:

- cada competência mensal deve ser autocontida;
- os PDFs técnicos são evidências, não entregáveis finais principais;
- o relatório executivo é o principal produto analítico entregue ao cliente;
- o dashboard Looker Studio é a camada operacional de consulta;
- a evolução histórica é mais relevante que flutuações isoladas;
- hipóteses devem ser identificadas como hipóteses;
- causalidade só deve ser afirmada com evidência suficiente;
- variações pontuais não devem ser tratadas automaticamente como tendências estruturais;
- decisões mensais devem considerar histórico, baseline e contexto regional;
- o processo deve preservar rastreabilidade entre PDFs, análises intermediárias e resumo executivo.

---

# Decisões Arquiteturais Permanentes

As principais decisões estruturais do projeto são:

- o repositório deve ser organizado por competências mensais em `reports/AAAA-MM/`;
- cada competência deve conter `source/`, `analysis/`, `output/` e `manifest.json`;
- os PDFs originais devem ser preservados com os nomes exportados pelas ferramentas;
- não deve haver renomeação manual dos PDFs;
- nenhuma análise deve ser iniciada antes da validação do `manifest.json`;
- apenas GA4 e Google Search Console geram análises individuais obrigatórias;
- SEMrush deve ser utilizado como fonte complementar, salvo solicitação explícita de análise individual;
- o resumo executivo em Markdown é gerado pelo Codex;
- DOCX e PDF são gerados posteriormente no ChatGPT após revisão humana;
- histórico e changelog só devem ser atualizados após aprovação explícita do usuário;
- o baseline não deve ser sobrescrito mensalmente.

---

# Filosofia de Reporting

A filosofia de reporting do projeto é consultiva e executiva.

O relatório mensal deve responder:

- o que mudou no período;
- por que a mudança é relevante;
- qual é o impacto para o projeto;
- qual é o nível de confiança da leitura;
- quais ações devem ser priorizadas.

O relatório não deve funcionar como transcrição de ferramenta, leitura operacional de dashboard ou resumo sequencial de PDFs.

A leitura estratégica deve prevalecer sobre a listagem exaustiva de métricas.

---

# Evolução Histórica como Critério Analítico

A evolução histórica é um dos critérios centrais de análise do projeto.

Sempre que possível, a competência atual deve ser comparada com:

- mês anterior;
- histórico acumulado;
- baseline do projeto;
- padrões regionais já identificados;
- decisões e aprendizados registrados anteriormente.

Isso evita conclusões frágeis baseadas apenas em variações de curto prazo.

---

# Interpretação Regional

A análise do projeto deve considerar sua dimensão latino-americana.

Os países são organizados em grupos regionais:

- Grupo 1: Argentina, Uruguai e Chile.
- Grupo 2: Brasil, Paraguai e Bolívia.
- Grupo 3: Peru, Equador e Colômbia.
- Grupo 4: Venezuela, Panamá e Costa Rica.
- Grupo 5: Nicarágua, El Salvador e Honduras.
- Grupo 6: República Dominicana, Belize e Guatemala.
- Grupo 7: México.

A análise regional deve priorizar países com peso estratégico, crescimento relevante, queda significativa ou impacto direto no desempenho geral do projeto.

Não é necessário listar todos os países em todo relatório se apenas alguns forem relevantes na competência analisada.

---

# Papel dos Conteúdos Educacionais

O site possui papel educacional e institucional.

Conteúdos relacionados a STEM, inovação, aprendizagem baseada em projetos, módulos educacionais e práticas formativas devem ser tratados como ativos estratégicos de SEO.

Quando conteúdos educacionais apresentarem crescimento, queda ou oportunidade orgânica, a leitura deve considerar:

- impacto na descoberta orgânica;
- potencial de tráfego qualificado;
- relação com clusters de conteúdo;
- oportunidade de links internos;
- potencial de expansão regional;
- aderência ao posicionamento institucional do projeto.

---

# O que Não Deve Mudar com Frequência

Não devem mudar com frequência:

- filosofia de reporting;
- estrutura executiva do relatório;
- arquitetura principal do repositório;
- separação entre evidência, análise e entrega final;
- papel do `manifest.json`;
- regra de validação antes da análise;
- uso de GA4 e GSC como fontes obrigatórias;
- uso de SEMrush como fonte complementar;
- necessidade de revisão humana antes do encerramento;
- distinção entre Codex e ChatGPT no pipeline.

Mudanças nesses pontos devem ser tratadas como decisões estruturais e registradas neste documento e no changelog.

---

# O que Pode Evoluir

Podem evoluir ao longo do projeto:

- prompts de análise;
- templates de entrega;
- scripts de automação;
- regras de validação do `manifest.json`;
- integração com ferramentas externas;
- base de conhecimento;
- histórico acumulado;
- indicadores acompanhados;
- critérios de priorização;
- capacidade de geração editorial;
- automação de DOCX e PDF após aprovação;
- modelos de análise preditiva.

Essas evoluções devem preservar a arquitetura central do projeto.

---

# Separação entre Histórico Permanente e Histórico Mensal

Este documento registra histórico permanente.

Devem ser registrados aqui:

- mudanças estruturais do projeto;
- decisões metodológicas permanentes;
- mudanças na arquitetura do repositório;
- redefinições de responsabilidades entre Codex e ChatGPT;
- alterações no papel das fontes de dados;
- mudanças na filosofia de reporting.

Não devem ser registrados aqui:

- resultados mensais;
- variações de tráfego de uma competência;
- conclusões específicas de um mês;
- hipóteses pontuais;
- ajustes editoriais menores;
- correções operacionais sem impacto estrutural.

Esses itens devem ser registrados em `history/` ou no changelog, conforme o caso.

---

# Atualização deste Documento

Este documento deve ser atualizado apenas quando houver mudanças estruturais no projeto.

Mudanças operacionais mensais não justificam alteração neste arquivo.

Quando este documento for atualizado, verificar consistência com:

- `00_MASTER_SPECIFICATION.md`;
- `01_PROMPT_RELATORIO_EXECUTIVO.md`;
- `03_REGRAS_DE_ANALISE.md`;
- `04_GLOSSARIO.md`;
- `README.md`;
- `START_HERE.md`;
- `knowledge/11_CHANGELOG.md`.