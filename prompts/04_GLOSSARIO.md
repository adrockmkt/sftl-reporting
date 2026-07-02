
# 04 GLOSSÁRIO

# Glossário do Projeto SFTL Reporting

## Objetivo

Este documento centraliza os principais termos utilizados no projeto SFTL Reporting.

Seu objetivo é garantir consistência terminológica entre análises, prompts, documentação operacional, relatórios executivos e entregas finais do projeto Solve for Tomorrow Latam.

O glossário deve ser usado como referência por qualquer IA, consultor ou profissional envolvido no fluxo de análise mensal.

---

# Plataformas e Fontes de Dados

## Google Analytics 4 (GA4)

Ferramenta utilizada para analisar comportamento dos usuários no site.

No projeto SFTL, o GA4 é fonte obrigatória para avaliar:

- sessões;
- usuários;
- novos usuários;
- canais de aquisição;
- páginas acessadas;
- países;
- dispositivos;
- engajamento;
- eventos;
- key events.

## Google Search Console (GSC)

Ferramenta utilizada para monitorar o desempenho orgânico do site na busca do Google.

No projeto SFTL, o GSC é fonte obrigatória para avaliar:

- cliques orgânicos;
- impressões;
- CTR;
- posição média;
- páginas orgânicas;
- consultas;
- países;
- evolução da visibilidade nas SERPs.

## SEMrush

Plataforma utilizada como fonte complementar para SEO.

Pode apoiar análises de:

- backlinks;
- domínios de referência;
- autoridade;
- toxicidade;
- monitoramento de posição;
- auditoria técnica;
- palavras-chave;
- visibilidade orgânica estimada.

Na arquitetura atual do projeto, SEMrush não gera análise individual obrigatória, salvo solicitação explícita do usuário. Deve ser utilizado como apoio estratégico quando houver evidência relevante.

## Looker Studio

Dashboard operacional utilizado para consulta detalhada de métricas.

O relatório executivo não deve repetir excessivamente os dados disponíveis no Looker Studio. Ele deve interpretar os dados e destacar impactos, riscos e recomendações.

---

# Estrutura Operacional do Projeto

## Competência

Período mensal analisado pelo projeto.

Cada competência possui uma pasta própria em:

```text
reports/AAAA-MM/
```

Exemplo:

```text
reports/2026-06/
```

Cada competência deve ser autocontida, preservando arquivos originais, análises intermediárias, entregáveis finais e inventário do período.

## Pasta source

Diretório da competência onde ficam os PDFs originais exportados das ferramentas.

Caminho padrão:

```text
reports/AAAA-MM/source/
```

Os arquivos devem permanecer com os nomes originais exportados.

## Pasta analysis

Diretório da competência onde ficam as análises intermediárias em Markdown.

Caminho padrão:

```text
reports/AAAA-MM/analysis/
```

Arquivos obrigatórios:

```text
ga4_analise.md
gsc_analise.md
```

## Pasta output

Diretório da competência onde ficam os entregáveis consolidados.

Caminho padrão:

```text
reports/AAAA-MM/output/
```

Arquivos esperados:

```text
resumo_executivo.md
resumo_executivo.docx
resumo_executivo.pdf
```

## manifest.json

Arquivo de inventário da competência.

Registra:

- competência analisada;
- arquivos encontrados em `source/`;
- tipo identificado de cada relatório;
- relatórios obrigatórios presentes ou ausentes;
- status de validação;
- status de revisão;
- status de conclusão operacional.

Nenhuma análise deve ser iniciada antes da validação do `manifest.json`.

## Baseline

Referência histórica inicial do projeto.

Serve como ponto de comparação para avaliar evolução de tráfego, SEO, backlinks, visibilidade e desempenho estrutural ao longo do tempo.

O baseline não deve ser sobrescrito mensalmente. Caso uma nova referência seja necessária, ela deve ser criada como nova versão documentada.

## Histórico

Conjunto de registros acumulados sobre desempenho, decisões, hipóteses, recomendações e evolução mensal do projeto.

Deve ser usado para contextualizar os resultados da competência atual.

---

# Entregáveis

## Relatório Executivo

Principal documento analítico entregue ao cliente.

Consolida os achados mais relevantes da competência, com foco em:

- decisão executiva;
- impacto estratégico;
- riscos;
- oportunidades;
- recomendações priorizadas.

O relatório executivo não deve ser uma transcrição dos PDFs nem uma repetição do Looker Studio.

## Relatórios Técnicos

PDFs exportados das ferramentas.

Funcionam como evidência técnica, documentação de apoio e fonte de consulta futura.

Não são o principal material de leitura para o cliente.

## Análises Intermediárias

Arquivos Markdown gerados para documentar a leitura específica de GA4 e GSC.

Servem como base para o resumo executivo.

## DOCX

Versão editável do relatório executivo final.

Deve ser gerada apenas após revisão humana e finalização editorial.

## PDF

Versão final fechada do relatório executivo para envio ou arquivamento.

Deve ser gerada apenas após revisão humana e finalização editorial.

---

# Indicadores de GA4

## Sessões

Quantidade de visitas iniciadas no site durante o período analisado.

Uma sessão pode incluir múltiplas páginas, eventos e interações.

## Usuários

Quantidade de usuários distintos identificados pelo GA4 no período.

## Novos Usuários

Usuários que acessaram o site pela primeira vez no período analisado.

## Usuários Recorrentes

Usuários que retornaram ao site após uma visita anterior.

Indicam potencial de retenção e recorrência de acesso.

## Visualizações de Página

Quantidade total de carregamentos ou visualizações de páginas.

Pode ser maior que o número de sessões e usuários.

## Taxa de Engajamento

Percentual de sessões consideradas engajadas pelo GA4.

Pode indicar qualidade da visita, mas deve ser interpretada em conjunto com tempo de engajamento, páginas e eventos.

## Tempo Médio de Engajamento

Tempo médio em que o site permaneceu efetivamente em foco para o usuário.

Não deve ser confundido com tempo total de permanência em uma aba aberta.

## Eventos

Interações registradas no GA4.

Podem incluir cliques, visualizações, rolagem, downloads, formulários, interações com componentes e eventos personalizados.

## Key Events

Eventos marcados como estratégicos no GA4.

Podem representar conversões ou interações relevantes para o projeto.

---

# Indicadores de Google Search Console

## Impressões

Quantidade de vezes que uma página do site apareceu nos resultados de busca do Google.

Impressões indicam presença e cobertura nas SERPs, mas não necessariamente tráfego.

## Cliques

Quantidade de acessos originados a partir dos resultados orgânicos do Google.

Cliques representam tráfego orgânico efetivo vindo da busca.

## CTR

Click Through Rate.

Percentual de cliques em relação às impressões.

Fórmula:

```text
CTR = cliques / impressões
```

CTR baixa em páginas com muitas impressões pode indicar necessidade de revisar título, descrição, intenção de busca ou atratividade do resultado.

## Posição Média

Média das posições ocupadas pelo site nas pesquisas do Google.

Número menor indica melhor posicionamento.

Número maior indica pior posicionamento.

A posição média deve ser interpretada com cautela, pois pode variar conforme consulta, país, dispositivo e volume de impressões.

## Consultas

Termos de busca usados pelos usuários no Google que geraram impressões ou cliques para o site.

## Páginas Orgânicas

URLs do site que apareceram ou receberam cliques nos resultados orgânicos do Google.

---

# Indicadores de SEMrush

## Visibilidade

Indicador utilizado pelo SEMrush para estimar a presença orgânica do domínio nas palavras-chave monitoradas.

Maior visibilidade geralmente indica melhor presença nas SERPs monitoradas.

## Tráfego Estimado

Estimativa de visitas orgânicas calculada pelo SEMrush a partir das posições monitoradas e do volume de busca das palavras-chave.

Deve ser tratado como estimativa, não como tráfego real.

## Posição Média no SEMrush

Média das posições das palavras-chave monitoradas no Position Tracking.

Número menor indica melhora de ranking.

Número maior indica piora de ranking.

## Backlinks

Links externos apontando para o domínio analisado.

Podem contribuir para autoridade, descoberta e relevância, mas não devem ser tratados isoladamente como causa direta de ranking.

## Domínios Referenciadores

Quantidade de domínios únicos que possuem links apontando para o site.

Em geral, a diversidade de domínios é mais relevante do que apenas o volume total de backlinks.

## Authority Score

Métrica proprietária do SEMrush que estima a autoridade geral de um domínio.

Deve ser usada como indicador comparativo, não como métrica oficial do Google.

## Toxicidade

Classificação do SEMrush para risco potencial de backlinks.

Deve ser interpretada com cautela e revisada manualmente antes de qualquer ação de desautorização.

---

# Conceitos de SEO

## SEO Técnico

Conjunto de otimizações relacionadas à infraestrutura, rastreamento, indexação, performance, arquitetura e saúde técnica do site.

## SEO On Page

Otimizações realizadas diretamente no conteúdo e na estrutura das páginas.

Inclui títulos, headings, meta descriptions, conteúdo, links internos, dados estruturados e experiência de leitura.

## SEO Off Page

Conjunto de fatores externos ao site que contribuem para autoridade e reputação.

Inclui backlinks, menções, parcerias e citações institucionais.

## SERP

Search Engine Results Page.

Página de resultados exibida pelo Google ou por outro mecanismo de busca.

## CTR Orgânico

Taxa de clique dos resultados orgânicos.

Indica a capacidade de um resultado atrair cliques quando aparece nas buscas.

## Indexação

Processo pelo qual páginas são adicionadas ao índice do Google e passam a poder aparecer nos resultados de busca.

## Rastreamento

Processo pelo qual mecanismos de busca acessam páginas do site para descobrir, atualizar ou avaliar conteúdo.

## Long Tail

Consultas específicas e normalmente menos concorridas.

Geralmente apresentam intenção de busca mais clara e podem gerar tráfego qualificado.

## Head Term

Palavra-chave ampla, de alto volume e geralmente alta concorrência.

## Cluster de Conteúdo

Conjunto de páginas relacionadas a um mesmo tema, conectadas por interligação interna e arquitetura editorial.

## Link Interno

Link entre páginas do próprio site.

Ajuda na navegação, distribuição de autoridade interna e descoberta de conteúdos.

## Link Building

Estratégia de aquisição ou estímulo à conquista de backlinks relevantes.

No projeto SFTL, deve priorizar fontes educacionais, institucionais, jornalísticas e parceiros relevantes.

## Snippet

Trecho exibido nos resultados de busca, geralmente formado por título, URL e descrição.

Pode influenciar diretamente a CTR.

## Meta Description

Descrição HTML de uma página.

Não é fator direto de ranking, mas pode influenciar a taxa de clique nos resultados orgânicos.

## Title Tag

Título HTML da página exibido geralmente como título clicável nos resultados de busca.

Tem impacto importante em SEO e CTR.

---


# Conceitos Analíticos

## Evidência Numérica

Dado quantitativo usado para sustentar uma conclusão analítica.

Deve ser utilizado sempre que o texto afirmar crescimento, queda, avanço, regressão, estabilidade, ganho de eficiência ou perda de eficiência.

Exemplo:

```text
As sessões passaram de X para Y, variação de Z%.
```

A evidência numérica não deve ser usada como transcrição do dashboard. Deve aparecer apenas quando ajudar a comprovar uma leitura executiva.

## Camada Mínima de Evidência

Conjunto mínimo de números que deve aparecer nas análises individuais e no resumo executivo para sustentar conclusões sem transformar o documento em relatório operacional.

Deve incluir, quando disponível:

- valor do mês atual;
- valor do mês anterior;
- variação absoluta;
- variação percentual.

A camada mínima de evidência deve ser aplicada principalmente a GA4 e Google Search Console, e também a SEMrush quando houver dado relevante para explicar impacto, risco ou recomendação.

## Valor Atual

Valor registrado para uma métrica na competência analisada.

Exemplo:

```text
Sessões em junho de 2026.
```

## Valor Anterior

Valor registrado para a mesma métrica na competência imediatamente anterior ou no período de comparação definido.

Exemplo:

```text
Sessões em maio de 2026.
```

## Variação Absoluta

Diferença numérica entre o valor atual e o valor anterior.

Fórmula:

```text
variação absoluta = valor atual - valor anterior
```

Exemplo:

```text
Se as sessões passaram de 1.000 para 850, a variação absoluta foi de -150 sessões.
```

## Variação Percentual

Percentual de aumento ou queda entre o valor atual e o valor anterior.

Fórmula:

```text
variação percentual = (valor atual - valor anterior) / valor anterior
```

Exemplo:

```text
Se as sessões passaram de 1.000 para 850, a variação percentual foi de -15%.
```

A variação percentual deve ser interpretada com cautela em bases pequenas, porque mudanças pequenas em números absolutos podem gerar percentuais altos.

## Base Pequena

Situação em que uma métrica possui volume absoluto baixo e, por isso, pode gerar variações percentuais elevadas sem impacto estratégico proporcional.

Exemplo:

```text
Uma página que passa de 1 para 4 cliques cresce 300%, mas ainda possui impacto limitado no desempenho total.
```

Quando a base for pequena, priorizar a leitura do impacto absoluto antes de destacar o percentual.

## Métrica de Sustentação

Métrica selecionada para comprovar uma conclusão específica.

Não é qualquer métrica disponível. É o número necessário para sustentar uma leitura executiva.

Exemplo:

- para sustentar queda de tráfego: sessões, usuários ou canal de aquisição;
- para sustentar perda de eficiência orgânica: cliques, impressões, CTR e posição média;
- para sustentar oportunidade regional: país, sessões, cliques, impressões, eventos ou ranking monitorado;
- para sustentar problema técnico: volume de URLs afetadas, severidade ou recorrência.

## Fato Observado

Informação diretamente sustentada pelos dados disponíveis.

Exemplo:

```text
Os cliques orgânicos cresceram no período analisado.
```

## Hipótese

Interpretação provável, mas não totalmente comprovada pelos dados disponíveis.

Deve ser identificada claramente como hipótese.

## Recomendação

Ação sugerida com base em fatos observados, hipóteses e impacto estratégico.

Deve ser prática, priorizada e conectada ao diagnóstico.

## Evidência Forte

Conclusão sustentada por duas ou mais fontes apontando para a mesma direção.

## Evidência Moderada

Conclusão sustentada por uma fonte principal e sem contradição relevante nas demais.

## Evidência Fraca

Conclusão baseada em métrica isolada, dado incompleto ou fontes divergentes.

Deve ser tratada com cautela.

## Causalidade

Relação direta de causa e efeito.

Só deve ser afirmada quando houver evidência suficiente.

Na maioria dos casos, usar linguagem de hipótese ou indicação.

## Correlação

Relação entre dois comportamentos ou indicadores que caminham juntos.

Correlação não significa causalidade.

## Tendência

Padrão observado ao longo de mais de um período ou sustentado por múltiplas evidências.

Não deve ser confundida com variação pontual.

## Variação Pontual

Mudança observada em um único período, sem confirmação histórica ou recorrência.

Deve ser acompanhada antes de ser tratada como tendência estrutural.

---

# Conceitos do Projeto SFTL

## Solve for Tomorrow Latam

Projeto educacional da Samsung voltado à inovação, educação STEM e desenvolvimento de projetos escolares na América Latina.

## Grupos Regionais

Agrupamento de países utilizado para análise regional do projeto.

Grupos oficiais:

- Grupo 1: Argentina, Uruguai e Chile.
- Grupo 2: Brasil, Paraguai e Bolívia.
- Grupo 3: Peru, Equador e Colômbia.
- Grupo 4: Venezuela, Panamá e Costa Rica.
- Grupo 5: Nicarágua, El Salvador e Honduras.
- Grupo 6: República Dominicana, Belize e Guatemala.
- Grupo 7: México.

## País Estratégico

País com relevância para tráfego, SEO, visibilidade institucional, operação regional ou expansão do projeto.

A classificação pode variar conforme o período e a estratégia do projeto.

## Conteúdo Educacional

Página, módulo ou material voltado à formação, metodologia, aprendizagem baseada em projetos, STEM, inovação ou práticas educacionais.

## Página Institucional

Página voltada à apresentação do programa, regulamentos, países participantes, inscrição, informações oficiais ou comunicação institucional.

---

# Terminologia Padronizada

Utilizar sempre:

- Resumo Geral
- Pontos Fortes
- Pontos de Atenção
- Impacto Geral no Projeto
- Recomendações Priorizadas
- Alta prioridade
- Média prioridade
- Baixa prioridade

Evitar variações como:

- Pontos positivos principais
- Alertas
- Problemas
- Insights gerais
- Próximos passos soltos
- Considerações finais

A padronização facilita consistência entre competências e conversão para DOCX/PDF.

---

# Termos que Exigem Cuidado

## Crescimento

Usar quando houver aumento mensurável em uma métrica.

Sempre que possível, informar valor atual, valor anterior, variação absoluta e variação percentual.

Evitar usar o termo quando houver apenas melhora percentual em base muito pequena sem impacto estratégico.

## Queda

Usar quando houver redução mensurável em uma métrica.

Sempre que possível, informar valor atual, valor anterior, variação absoluta e variação percentual.

Evitar tratar toda queda pontual como problema estrutural.

## Avanço

Usar quando houver melhora relevante para o projeto, sustentada por métrica, correlação entre fontes ou evolução histórica.

Não usar como sinônimo genérico de qualquer variação positiva.

## Regressão

Usar quando houver piora relevante para o projeto, sustentada por métrica, correlação entre fontes ou evolução histórica.

Não usar como sinônimo genérico de qualquer variação negativa.

## Ganho de Eficiência

Usar quando uma métrica indicar melhor aproveitamento de uma oportunidade existente.

Exemplos:

- aumento de CTR com volume relevante de impressões;
- aumento de sessões engajadas em relação às sessões totais;
- aumento de cliques sem crescimento proporcional de impressões;
- melhora de posição média acompanhada de aumento de cliques.

## Perda de Eficiência

Usar quando uma métrica indicar pior aproveitamento de uma oportunidade existente.

Exemplos:

- aumento de impressões com queda de cliques;
- queda de CTR;
- aumento de tráfego sem aumento proporcional de engajamento;
- melhora de visibilidade sem avanço em sessões ou eventos relevantes.

Sempre sustentar a leitura com números quando os dados estiverem disponíveis.

## Crescimento Consistente

Usar apenas quando houver evidência em mais de um período ou confirmação em mais de uma fonte.

## Queda Estrutural

Usar apenas quando a perda for recorrente, relevante ou sustentada por múltiplas evidências.

## Melhora de Ranking

Usar quando a posição média melhorar, ou seja, quando o número da posição diminuir.

## Piora de Ranking

Usar quando a posição média piorar, ou seja, quando o número da posição aumentar.

## Tráfego Qualificado

Usar quando houver indícios de relevância do acesso, como engajamento, origem orgânica estratégica, páginas relevantes ou eventos associados.

Não usar apenas como sinônimo de aumento de sessões.

---

# Atualização do Glossário

Este documento deve ser atualizado quando:

- novos conceitos passarem a fazer parte do projeto;
- houver mudança na arquitetura do pipeline;
- uma nova ferramenta for incorporada;
- a terminologia oficial das entregas mudar;
- algum termo estiver gerando ambiguidade nas análises.

A atualização deve preservar compatibilidade com `00_MASTER_SPECIFICATION.md`, `01_PROMPT_RELATORIO_EXECUTIVO.md`, `02_ESTILO_DE_ESCRITA.md` e `03_REGRAS_DE_ANALISE.md`.