

# Regras de Análise

## Objetivo
Este documento define a metodologia analítica utilizada para correlacionar todas as fontes de dados antes da produção de conclusões e recomendações.


## Princípios Gerais
- Nunca analisar um relatório isoladamente.
- Sempre correlacionar fontes.
- Priorizar tendências sobre eventos pontuais.
- Priorizar impacto no projeto sobre métricas isoladas.
- Procurar causa antes de descrever efeito.

## Validação da Competência

Antes de iniciar qualquer análise, validar a competência selecionada.

Confirmar obrigatoriamente:

- existência do `manifest.json`;
- presença de todos os PDFs obrigatórios;
- organização correta dos arquivos em `source/`;
- inexistência de arquivos de outras competências.

Caso qualquer validação falhe, interromper a execução e informar os itens pendentes.

## Ordem de Correlação

A análise deverá seguir obrigatoriamente a seguinte sequência:

1. Google Analytics 4
2. Google Search Console
3. Monitoramento de Posição
4. Auditoria do Site
5. On Page SEO Checker
6. Backlinks
7. Keyword Strategy

Somente após correlacionar todas as fontes será permitido elaborar conclusões.

## Regras de Correlação
Exemplos de correlação:
- Queda de usuários + queda de impressões = possível perda de visibilidade.
- Queda de posições + estabilidade técnica = possível aumento de concorrência.
- Crescimento de backlinks + estabilidade de ranking = autoridade ainda não refletida.
- Crescimento de impressões + queda de CTR = problema de snippet/intenção.
- Crescimento de erros técnicos + queda de indexação = prioridade alta.

- Nunca utilizar uma única métrica para justificar uma conclusão.
- Confirmar tendências em pelo menos duas fontes quando possível.
- Considerar fatores sazonais antes de concluir perda ou crescimento.
- Diferenciar problemas técnicos, editoriais e de concorrência.

## Priorização
- **Alta**: Impacto direto e relevante no negócio ou risco iminente.
- **Média**: Impacto relevante, mas sem risco imediato.
- **Baixa**: Impacto pontual ou de baixa relevância.

A priorização deve considerar o impacto potencial para o projeto como um todo, e não apenas a magnitude da variação observada.

## Critérios para Pontos Fortes
Exemplos:
- Crescimento consistente.
- Recuperação de posições.
- Melhoria técnica.
- Expansão internacional.
- Redução de erros.

## Critérios para Pontos de Atenção
Exemplos:
- Perda contínua.
- Queda de CTR.
- Aumento de erros.
- Perda de backlinks.
- Regressão em países estratégicos.

## Critérios para Recomendações
Toda recomendação deve ser:
- Executável (actionable).
- Priorizada.
- Justificada.
- Relacionada à causa detectada.

## Regras de Ouro
- Nunca repetir números do dashboard.
- Nunca gerar conclusões sem evidências correlacionadas.
- Nunca tratar sintomas como causa.
- Sempre pensar como consultor executivo.

- Nunca iniciar a análise sem validar a competência.
- Nunca misturar dados de competências diferentes.
- Sempre fundamentar recomendações em evidências correlacionadas.
- Sempre priorizar causas antes de ações corretivas.
# 03 REGRAS DE ANÁLISE

# Regras de Análise dos Relatórios SFTL

## Objetivo

Este documento define a metodologia analítica utilizada no projeto Solve for Tomorrow Latam para interpretar dados, correlacionar fontes, classificar hipóteses, priorizar recomendações e evitar conclusões frágeis.

Ele deve ser utilizado em conjunto com:

- `00_MASTER_SPECIFICATION.md`
- `01_PROMPT_RELATORIO_EXECUTIVO.md`
- `02_ESTILO_DE_ESCRITA.md`
- `06_HIPOTESES_E_CONFIANCA.md`
- `07_ESTILO_CONSULTIVO.md`

Este documento regula o raciocínio analítico. Ele não define estrutura editorial nem fluxo operacional completo.

---

# Princípios Gerais

Toda análise deve seguir estes princípios:

- Nunca analisar uma métrica isoladamente quando houver outras fontes disponíveis.
- Sempre correlacionar GA4 e Google Search Console como fontes obrigatórias.
- Utilizar SEMrush, histórico e baseline como fontes complementares quando disponíveis.
- Priorizar tendências sobre eventos pontuais.
- Priorizar impacto no projeto sobre variações isoladas.
- Diferenciar fato observado, hipótese interpretativa e recomendação prática.
- Procurar causas prováveis antes de propor ações corretivas.
- Evitar conclusões categóricas quando a evidência for limitada.
- Registrar limitações dos dados quando existirem.

A análise deve responder sempre:

1. O que mudou.
2. Onde mudou.
3. Qual é a evidência.
4. Qual é a causa provável.
5. Qual é o impacto.
6. Qual ação deve ser priorizada.

---

# Validação da Competência

Antes de iniciar qualquer análise, validar a competência ativa.

Confirmar obrigatoriamente:

- existência do `manifest.json`;
- consistência entre `manifest.json` e a pasta `source/`;
- presença dos relatórios obrigatórios de GA4 e Google Search Console;
- organização correta dos arquivos em `reports/AAAA-MM/source/`;
- inexistência de arquivos de outras competências;
- inexistência de duplicidades críticas;
- identificação clara da competência analisada.

Caso qualquer validação crítica falhe, interromper a execução e informar os itens pendentes.

Não gerar análise parcial quando faltar fonte obrigatória.

---

# Hierarquia Analítica das Fontes

A análise deve respeitar a seguinte hierarquia.

## Fontes obrigatórias

1. Google Analytics 4
2. Google Search Console

Essas fontes devem sempre ser analisadas e correlacionadas.

GA4 responde principalmente sobre:

- tráfego;
- usuários;
- canais;
- páginas;
- países;
- comportamento;
- engajamento;
- eventos.

Google Search Console responde principalmente sobre:

- cliques orgânicos;
- impressões;
- CTR;
- posição média;
- páginas orgânicas;
- consultas;
- presença nas buscas.

## Fontes complementares

Utilizar quando estiverem disponíveis e forem relevantes para a conclusão:

1. SEMrush Monitoramento de Posição
2. SEMrush Auditoria do Site
3. SEMrush Backlinks
4. SEMrush On Page SEO Checker
5. SEMrush Keyword Strategy
6. histórico mensal do projeto
7. baseline histórico
8. changelog e decisões anteriores

Essas fontes não precisam gerar análises individuais obrigatórias, salvo solicitação explícita do usuário.

Elas devem apoiar, contextualizar ou qualificar conclusões do resumo executivo.

---

# Ordem Recomendada de Leitura Analítica

A análise deve seguir esta sequência lógica:

1. Validar a competência e o `manifest.json`.
2. Ler GA4 para entender comportamento de tráfego e audiência.
3. Ler Google Search Console para entender desempenho orgânico.
4. Cruzar GA4 e GSC para identificar coerência ou divergência.
5. Consultar histórico e baseline para entender tendência de longo prazo.
6. Consultar SEMrush quando houver dados disponíveis e relevantes.
7. Classificar achados por impacto estratégico.
8. Diferenciar fatos, hipóteses e recomendações.
9. Priorizar ações.
10. Consolidar apenas o que for relevante para o resumo executivo.

Não é obrigatório correlacionar todas as fontes SEMrush em toda competência. A correlação deve ser proporcional à disponibilidade dos dados e à relevância estratégica do mês.

---

# Regras de Correlação

A correlação deve buscar coerência entre fontes.

Exemplos:

- Crescimento de sessões orgânicas no GA4 junto com aumento de cliques no GSC indica avanço orgânico mais consistente.
- Crescimento de impressões no GSC com queda de CTR sugere necessidade de revisar títulos, descrições e aderência à intenção de busca.
- Queda de tráfego orgânico no GA4 sem queda proporcional no GSC pode indicar mudança de comportamento pós clique, páginas específicas ou diferença de mensuração.
- Queda de cliques no GSC com estabilidade de posição média pode indicar redução de demanda, sazonalidade ou perda de atratividade dos snippets.
- Piora de posição média no GSC acompanhada de perda de rankings no SEMrush reforça hipótese de pressão competitiva ou perda de relevância orgânica.
- Crescimento de tráfego em país específico no GA4 com aumento de impressões orgânicas no GSC para o mesmo mercado sugere expansão regional mais consistente.
- Crescimento de backlinks ou domínios de referência pode indicar fortalecimento de autoridade, mas não deve ser tratado como causa direta de melhoria de ranking sem evidência adicional.
- Aumento de erros técnicos em auditoria pode ser ponto de atenção quando houver impacto simultâneo em indexação, tráfego orgânico ou desempenho de páginas relevantes.

---

# Regras de Interpretação

Nunca utilizar uma única métrica para justificar uma conclusão estrutural.

Confirmar tendências em mais de uma fonte quando possível.

Considerar sazonalidade, campanhas, publicações recentes, mudanças técnicas e contexto regional antes de concluir perda ou crescimento estrutural.

Diferenciar os tipos de problema:

- problema de aquisição;
- problema de visibilidade orgânica;
- problema de CTR;
- problema de posicionamento;
- problema técnico;
- problema editorial;
- problema de concorrência;
- problema de engajamento;
- problema de mensuração.

A mesma variação pode ter leituras diferentes conforme a fonte.

Exemplo:

- queda de usuários no GA4 pode ser problema de aquisição;
- queda de impressões no GSC pode ser perda de cobertura orgânica;
- queda de CTR pode ser problema de snippet ou intenção de busca;
- queda de posição média pode indicar competição ou perda de relevância;
- queda de engajamento pode indicar desalinhamento entre conteúdo e intenção do usuário.

---

# Classificação de Evidência

Toda conclusão deve estar apoiada por evidência.

## Evidência forte

Ocorre quando duas ou mais fontes apontam para a mesma direção.

Exemplo:

- GA4 mostra crescimento orgânico.
- GSC mostra aumento de cliques.
- SEMrush mostra ganho de posições.

Nesse caso, é possível afirmar que houve avanço orgânico com maior segurança.

## Evidência moderada

Ocorre quando uma fonte principal aponta uma tendência e outra fonte não contradiz a leitura.

Exemplo:

- GSC mostra aumento de impressões.
- GA4 mostra estabilidade de tráfego orgânico.

Nesse caso, a leitura pode indicar expansão de visibilidade ainda não convertida proporcionalmente em tráfego.

## Evidência fraca

Ocorre quando apenas uma métrica isolada aponta mudança relevante ou quando as fontes divergem.

Nesse caso, a conclusão deve ser tratada como hipótese e acompanhada nos próximos períodos.

---

# Tratamento de Hipóteses

Quando a causa não estiver comprovada, usar linguagem de hipótese.

Formulações recomendadas:

- A hipótese mais provável é...
- Os dados sugerem...
- Há indícios de...
- A leitura deve ser confirmada nos próximos ciclos.
- Não há evidência suficiente para afirmar causalidade direta.

Nunca escrever como fato uma causa que não esteja sustentada por evidência suficiente.

---

# Priorização

A priorização deve considerar impacto potencial para o projeto, urgência e capacidade de execução.

## Alta prioridade

Classificar como alta prioridade quando houver:

- impacto direto em tráfego orgânico relevante;
- risco de perda de visibilidade;
- queda em páginas ou países estratégicos;
- problema técnico com potencial de afetar indexação;
- queda relevante de CTR em páginas com alto volume de impressões;
- perda de posições em grupos ou países prioritários;
- oportunidade clara de ganho com esforço relativamente controlado.

## Média prioridade

Classificar como média prioridade quando houver:

- oportunidade de otimização relevante, mas sem risco imediato;
- necessidade de atualizar conteúdo;
- melhoria possível de snippets;
- expansão de conteúdo educacional;
- fortalecimento de links internos;
- ganho regional ainda em fase inicial;
- necessidade de acompanhar tendência por mais um ciclo.

## Baixa prioridade

Classificar como baixa prioridade quando houver:

- ajuste complementar;
- variação pontual sem impacto estrutural;
- oportunidade de refinamento futuro;
- ação que depende de outras prioridades;
- recomendação sem urgência operacional.

A prioridade não deve ser definida apenas pelo tamanho da variação percentual. Deve considerar relevância estratégica.

---

# Critérios para Pontos Fortes

Um ponto forte deve representar avanço relevante para o projeto.

Pode ser classificado como ponto forte quando houver:

- crescimento consistente de tráfego qualificado;
- aumento de tráfego orgânico;
- crescimento de cliques no GSC;
- aumento de impressões com potencial estratégico;
- melhora de CTR em páginas relevantes;
- melhora de posição média;
- recuperação de rankings;
- expansão regional em países estratégicos;
- avanço de engajamento;
- crescimento de backlinks qualificados;
- redução de problemas técnicos relevantes;
- evolução de páginas educacionais ou institucionais prioritárias.

Evitar registrar como ponto forte uma variação positiva pequena, isolada ou sem impacto estratégico.

---

# Critérios para Pontos de Atenção

Um ponto de atenção deve representar risco, limitação ou perda relevante.

Pode ser classificado como ponto de atenção quando houver:

- queda recorrente de tráfego;
- queda de tráfego orgânico;
- queda de cliques no GSC;
- queda de impressões em páginas ou países estratégicos;
- queda de CTR em páginas com alta exposição;
- piora de posição média;
- perda de rankings;
- redução de engajamento em páginas relevantes;
- aumento de problemas técnicos;
- perda de backlinks ou domínios relevantes;
- dependência excessiva de poucos canais, países ou páginas;
- divergência relevante entre fontes de dados.

Evitar transformar variação pontual em problema estrutural sem evidência recorrente.

---

# Critérios para Recomendações

Toda recomendação deve ser:

- executável;
- priorizada;
- justificada;
- relacionada à causa provável;
- conectada a uma evidência;
- proporcional ao impacto observado;
- compatível com o estágio atual do projeto.

Evitar recomendações genéricas.

Não recomendar ações sem relação clara com o diagnóstico.

Exemplos de recomendações boas:

- Revisar títulos e meta descriptions de páginas com alta impressão e baixa CTR.
- Atualizar páginas educacionais que perderam tráfego orgânico ou posições relevantes.
- Fortalecer links internos para páginas com crescimento de impressões e baixo tráfego.
- Priorizar conteúdos em países com crescimento regional consistente.
- Monitorar páginas com divergência entre cliques no GSC e sessões orgânicas no GA4.

Exemplos de recomendações ruins:

- Melhorar o SEO.
- Fazer mais conteúdo.
- Aumentar o tráfego.
- Corrigir o site.
- Melhorar performance.

---

# Regras para Dados Divergentes

Quando as fontes divergirem, não forçar uma conclusão única.

Exemplo:

- GSC indica crescimento de cliques.
- GA4 indica queda de sessões orgânicas.

Possíveis leituras:

- diferença de atribuição entre ferramentas;
- mudança de comportamento pós clique;
- filtros, consentimento ou mensuração;
- variação concentrada em páginas específicas;
- diferença entre cliques e sessões.

Nesses casos, declarar a divergência e recomendar acompanhamento ou análise específica.

---

# Regras para Sazonalidade

Antes de concluir regressão ou avanço estrutural, considerar:

- calendário escolar;
- ciclos regionais do projeto;
- períodos de inscrição;
- publicações recentes;
- campanhas de divulgação;
- feriados nacionais ou regionais;
- sazonalidade de busca;
- eventos institucionais.

Quando a sazonalidade for uma hipótese, declarar como hipótese.

---

# Regras para Países e Grupos Regionais

Quando houver análise regional, considerar os grupos do projeto:

- Grupo 1: Argentina, Uruguai e Chile.
- Grupo 2: Brasil, Paraguai e Bolívia.
- Grupo 3: Peru, Equador e Colômbia.
- Grupo 4: Venezuela, Panamá e Costa Rica.
- Grupo 5: Nicarágua, El Salvador e Honduras.
- Grupo 6: República Dominicana, Belize e Guatemala.
- Grupo 7: México.

A análise regional deve priorizar:

- países com maior peso no tráfego;
- países com crescimento expressivo;
- países com queda relevante;
- países estratégicos para o projeto;
- coerência entre tráfego, busca orgânica e ranking quando houver dados.

Evitar listar todos os países quando apenas poucos tiverem relevância no período.

---

# Regras para Relatórios Técnicos

Problemas técnicos devem ser priorizados apenas quando houver impacto potencial ou real.

Não tratar todo erro técnico como prioridade alta.

A leitura deve considerar:

- quantidade de URLs afetadas;
- relevância das páginas afetadas;
- impacto em rastreamento;
- impacto em indexação;
- impacto em experiência do usuário;
- recorrência do problema;
- capacidade de correção.

Problemas técnicos sem impacto estratégico devem ser classificados como média ou baixa prioridade.

---

# Regras de Ouro

- Nunca iniciar análise sem validar a competência.
- Nunca misturar dados de competências diferentes.
- Nunca analisar PDFs fora de `reports/AAAA-MM/source/`.
- Nunca usar uma única métrica para sustentar conclusão estrutural.
- Nunca tratar sintoma como causa.
- Nunca transformar hipótese em fato.
- Nunca apresentar causalidade sem evidência suficiente.
- Nunca repetir métricas do Looker Studio sem interpretação.
- Sempre correlacionar GA4 e GSC.
- Sempre usar SEMrush, histórico e baseline como apoio quando disponíveis.
- Sempre fundamentar recomendações em evidências.
- Sempre priorizar causas antes de ações corretivas.
- Sempre diferenciar fato, hipótese e recomendação.
- Sempre pensar como consultor executivo.
- Sempre priorizar impacto estratégico sobre detalhe operacional.