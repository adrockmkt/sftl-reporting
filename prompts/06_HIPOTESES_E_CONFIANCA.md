# Hipóteses e Níveis de Confiança

## Objetivo

Garantir que todas as análises produzidas pelo projeto diferenciem claramente fatos, hipóteses e conclusões, evitando interpretações não suportadas pelas evidências disponíveis.

---

## Regra Principal

Nunca apresentar uma hipótese como se fosse um fato.

Toda afirmação deve estar enquadrada em um dos níveis abaixo.

---

## Nível 0 - Informação Insuficiente

Representa situações em que não existem evidências suficientes para qualquer conclusão.

Nestes casos:

- não elaborar hipóteses;
- não produzir recomendações específicas;
- informar explicitamente quais dados adicionais são necessários para continuar a análise.

Exemplo:

"Não há evidências suficientes para determinar a causa da queda observada."

---

## Nível 1 - Fato Observado

Representa exclusivamente aquilo que foi identificado diretamente nas fontes de dados analisadas.

Características:

- baseado em evidências;
- mensurável;
- reproduzível;
- não depende de interpretação.

Exemplos:

- As sessões diminuíram em relação ao período anterior.
- A busca orgânica passou a representar a maior participação entre os canais.
- A página em inglês registrou crescimento de sessões.

---

## Nível 2 - Hipótese

Representa uma possível explicação para um comportamento observado.

Características:

- depende de validação;
- nunca deve ser apresentada como conclusão;
- deve indicar quais fontes adicionais podem confirmar ou refutar a hipótese.

Expressões recomendadas:

- pode indicar
- pode sugerir
- merece investigação
- é possível que
- uma hipótese é
- deverá ser confirmado

Expressões proibidas:

- ocorreu porque
- foi causado por
- certamente
- confirma que
- comprova que

---

## Nível 3 - Conclusão Confirmada

Só poderá ser utilizada quando houver evidências convergentes provenientes de duas ou mais fontes independentes.

Exemplos:

- Google Analytics 4
- Google Search Console
- Monitoramento de Posição
- Auditoria do Site
- Backlinks
- Keyword Strategy

Toda conclusão confirmada deverá ser sustentada por pelo menos duas fontes independentes. Exceções somente quando existir apenas uma fonte disponível para aquele indicador.

---

## Níveis de Confiança

As recomendações devem indicar implicitamente o grau de confiança da análise.

### Alta confiança

Quando duas ou mais fontes independentes apontam para a mesma conclusão.

### Média confiança

Quando apenas uma fonte aponta para a conclusão, mas não existem evidências conflitantes.

### Baixa confiança

Quando a conclusão depende apenas de hipóteses ou existem evidências insuficientes.

---

## Recomendações

As recomendações devem respeitar o mesmo nível de confiança da conclusão que lhes deu origem.

Nunca recomendar ações corretivas baseadas apenas em hipóteses sem indicar que validações adicionais são necessárias.

---

## Escrita

A classificação entre fato observado, hipótese, conclusão confirmada e informação insuficiente deve orientar o raciocínio da análise.

Entretanto, esses termos não devem ser utilizados repetidamente no texto final entregue ao cliente.

O relatório deverá incorporar essa metodologia de forma natural, mantendo uma leitura fluida, executiva e consultiva.

A metodologia deve orientar o processo de pensamento da IA, e não transformar o relatório em um documento didático sobre seu próprio raciocínio.

---

## Regras Obrigatórias

- Nunca transformar hipótese em conclusão.
- Nunca utilizar linguagem categórica sem evidência suficiente.
- Sempre informar quando uma hipótese depende de validação adicional.
- Priorizar fatos antes de interpretações.
- Sempre indicar quais outras fontes podem confirmar uma hipótese.
- Em caso de dúvida, utilizar linguagem conservadora.
- Nunca extrapolar tendências além do período analisado.
- Nunca assumir causalidade quando houver apenas correlação.
- Nunca utilizar linguagem absoluta sem evidência convergente.
- Nunca omitir limitações da análise quando elas existirem.
- Utilizar a metodologia como mecanismo interno de validação da análise.
- Evitar repetir expressões como "Fato observado", "Hipótese", "Conclusão confirmada" e "Informação insuficiente" ao longo do texto final.
- Sempre preferir uma redação natural que incorpore essas classificações implicitamente.
- O relatório deve parecer escrito por um consultor experiente, e não por um sistema descrevendo seu processo de raciocínio.

---

## Objetivo Final

O relatório executivo deve transmitir segurança ao cliente.

Quando houver certeza, ela deve estar fundamentada em evidências.

Quando houver dúvida, ela deve ser explicitamente apresentada como hipótese, juntamente com a recomendação de como validá-la.

---

## Fluxo de Decisão

Durante a elaboração das análises, seguir sempre esta sequência:

1. Identificar o fato observado.
2. Verificar se existem evidências suficientes.
3. Caso não existam, registrar informação insuficiente.
4. Caso existam, formular hipótese quando necessário.
5. Buscar confirmação em outras fontes.
6. Apenas então produzir uma conclusão.
7. Elaborar recomendações compatíveis com o nível de confiança obtido.

# 06 HIPÓTESES E CONFIANÇA

# Hipóteses, Evidências e Níveis de Confiança

## Objetivo

Este documento define como classificar fatos, hipóteses, evidências, conclusões e níveis de confiança nas análises do projeto Solve for Tomorrow Latam.

Sua função é evitar afirmações frágeis, causalidades indevidas e recomendações sem sustentação suficiente.

A metodologia deste documento deve orientar o raciocínio analítico, mas não deve transformar o relatório executivo em uma explicação didática sobre o processo de análise.

---

# Princípio Central

Nunca apresentar hipótese como fato.

Nunca apresentar correlação como causalidade.

Nunca apresentar variação pontual como tendência estrutural sem evidência suficiente.

Toda leitura analítica deve separar, ainda que implicitamente:

1. fato observado;
2. evidência disponível;
3. hipótese interpretativa;
4. conclusão possível;
5. recomendação compatível com o nível de confiança.

---

# Classificação Analítica

## Nível 0: Informação Insuficiente

Representa situações em que não existem evidências suficientes para formular conclusão ou hipótese útil.

Usar quando:

- a fonte obrigatória está ausente;
- os dados estão incompletos;
- a competência não foi validada;
- há inconsistência crítica no `manifest.json`;
- a métrica aparece isolada sem contexto suficiente;
- as fontes disponíveis são contraditórias e não permitem leitura confiável.

Conduta:

- não elaborar conclusão categórica;
- não produzir recomendação corretiva específica;
- indicar quais dados adicionais são necessários;
- recomendar validação ou acompanhamento.

Exemplo de redação:

```text
Não há evidência suficiente para determinar a causa da variação. A leitura deve ser validada com os dados do próximo ciclo e com a análise das páginas mais afetadas.
```

---

## Nível 1: Fato Observado

Representa aquilo que foi identificado diretamente nas fontes analisadas.

Características:

- baseado em dado disponível;
- mensurável;
- reproduzível;
- não depende de interpretação causal.

Exemplos:

- As sessões diminuíram em relação ao período anterior.
- A busca orgânica aumentou sua participação entre os canais.
- Uma página específica registrou crescimento de impressões.
- A CTR caiu em consultas ou páginas de alta exposição.

Fatos observados podem sustentar hipóteses e recomendações, mas não explicam sozinhos a causa da variação.

---

## Nível 2: Hipótese

Representa uma explicação provável para um fato observado, mas ainda não totalmente confirmada.

Usar quando:

- há indícios, mas não confirmação suficiente;
- uma fonte sugere uma causa provável;
- as fontes não se contradizem, mas também não confirmam plenamente;
- o comportamento pode ser explicado por sazonalidade, campanha, conteúdo, ranking, CTR, demanda ou mensuração.

Características:

- depende de validação;
- deve ser escrita com linguagem proporcional;
- deve indicar, quando necessário, como pode ser confirmada ou refutada;
- não deve ser apresentada como conclusão definitiva.

Expressões recomendadas:

- pode indicar;
- pode sugerir;
- os dados sugerem;
- há indícios de;
- a hipótese mais provável é;
- a leitura deve ser confirmada;
- merece acompanhamento;
- não há evidência suficiente para afirmar causalidade direta.

Expressões proibidas quando a evidência for limitada:

- ocorreu porque;
- foi causado por;
- certamente;
- comprova que;
- confirma que;
- sem dúvida;
- prova que.

Exemplo de redação:

```text
A queda de CTR pode indicar menor atratividade dos snippets ou aumento de competição nas SERPs. A leitura deve ser confirmada com a evolução das principais consultas no próximo ciclo.
```

---

## Nível 3: Conclusão Confirmada

Representa uma conclusão sustentada por evidências convergentes.

Usar quando:

- duas ou mais fontes independentes apontam para a mesma direção;
- uma fonte principal apresenta o dado e outra fonte reforça a leitura;
- não há evidências conflitantes relevantes;
- o histórico ou baseline confirma que a variação faz parte de um padrão recorrente.

Exemplos de fontes independentes:

- Google Analytics 4;
- Google Search Console;
- SEMrush Monitoramento de Posição;
- SEMrush Auditoria do Site;
- SEMrush Backlinks;
- histórico mensal;
- baseline do projeto.

Exemplo de leitura confirmada:

```text
O avanço orgânico do período é consistente, pois o aumento de sessões orgânicas no GA4 foi acompanhado por crescimento de cliques no Google Search Console.
```

Mesmo em conclusões confirmadas, evitar linguagem excessivamente absoluta quando a causa direta não estiver comprovada.

---

# Classificação de Evidência

## Evidência Forte

Ocorre quando duas ou mais fontes independentes convergem para a mesma leitura.

Exemplo:

- GA4 indica crescimento de tráfego orgânico.
- GSC indica crescimento de cliques orgânicos.
- SEMrush indica ganho de posições para termos relevantes.

Uso recomendado:

- pode sustentar conclusão mais assertiva;
- pode fundamentar recomendações prioritárias;
- pode ser apresentada como tendência se também houver recorrência histórica.

---

## Evidência Moderada

Ocorre quando uma fonte principal aponta uma leitura relevante e as demais fontes não contradizem essa interpretação.

Exemplo:

- GSC indica aumento de impressões.
- GA4 mantém tráfego orgânico estável.

Leitura possível:

```text
Há expansão de visibilidade orgânica, ainda sem conversão proporcional em tráfego.
```

Uso recomendado:

- pode sustentar recomendações de otimização;
- deve evitar causalidade direta;
- pode exigir acompanhamento no próximo ciclo.

---

## Evidência Fraca

Ocorre quando a leitura depende de métrica isolada, dado incompleto, recorte pequeno ou fontes divergentes.

Uso recomendado:

- tratar como hipótese;
- evitar recomendação corretiva agressiva;
- indicar necessidade de validação;
- acompanhar nos próximos períodos.

Exemplo de redação:

```text
A variação deve ser acompanhada antes de ser tratada como tendência estrutural, pois está sustentada por um recorte limitado do período.
```

---

# Níveis de Confiança

## Alta Confiança

Utilizar quando:

- há evidência forte;
- duas ou mais fontes independentes convergem;
- não há contradição relevante;
- o histórico reforça a leitura.

Pode sustentar:

- conclusões executivas;
- recomendações de alta prioridade;
- decisões de continuidade, correção ou expansão.

---

## Média Confiança

Utilizar quando:

- há evidência moderada;
- uma fonte principal sustenta a leitura;
- não há contradição relevante;
- a conclusão ainda precisa ser observada em novo ciclo.

Pode sustentar:

- recomendações de média prioridade;
- otimizações controladas;
- acompanhamento direcionado;
- testes ou validações adicionais.

---

## Baixa Confiança

Utilizar quando:

- há evidência fraca;
- existem dados incompletos;
- as fontes divergem;
- a conclusão depende de hipótese ainda não validada;
- o comportamento aparece apenas em recorte pontual.

Pode sustentar:

- recomendação de monitoramento;
- solicitação de dados adicionais;
- investigação específica;
- hipótese a ser validada.

Não deve sustentar ação corretiva de alta prioridade sem validação adicional.

---

# Relação entre Evidência, Confiança e Recomendação

A recomendação deve ser proporcional ao nível de confiança.

## Evidência Forte + Alta Confiança

Permite recomendações assertivas.

Exemplo:

```text
Priorizar a expansão do cluster educacional que apresentou crescimento orgânico consistente, reforçando links internos e novas páginas de apoio.
```

## Evidência Moderada + Média Confiança

Permite recomendações controladas.

Exemplo:

```text
Revisar títulos e descrições das páginas com alta impressão e CTR abaixo do esperado, acompanhando o impacto no próximo ciclo.
```

## Evidência Fraca + Baixa Confiança

Permite apenas recomendações de validação ou acompanhamento.

Exemplo:

```text
Monitorar a variação no próximo mês antes de tratá-la como tendência estrutural ou executar mudanças amplas.
```

---

# Regras para Causalidade

Causalidade só deve ser afirmada quando houver evidência suficiente.

Não afirmar que uma variação foi causada por:

- campanha;
- publicação de conteúdo;
- atualização técnica;
- mudança de ranking;
- backlinks;
- sazonalidade;
- concorrência;
- alteração de demanda;
- problema de mensuração;

sem sustentação adequada.

Quando houver apenas associação entre dados, usar linguagem de correlação ou hipótese.

Formulações seguras:

- pode estar relacionado a;
- sugere relação com;
- há indícios de associação com;
- a variação coincide com;
- a hipótese mais provável é.

---

# Regras para Tendência

Chamar de tendência apenas quando houver:

- repetição em mais de um período;
- confirmação histórica;
- convergência entre fontes;
- consistência em páginas, canais ou países relevantes.

Não chamar variação pontual de tendência estrutural.

Formulações seguras:

- o comportamento deve ser acompanhado nos próximos ciclos;
- ainda é cedo para tratar como tendência estrutural;
- a variação sugere um possível início de tendência, mas requer confirmação.

---

# Regras para Dados Divergentes

Quando fontes apresentarem sinais diferentes, não forçar conclusão única.

Exemplo:

- GA4 mostra queda de sessões orgânicas.
- GSC mostra crescimento de cliques orgânicos.

Possíveis interpretações:

- diferença entre clique e sessão;
- impacto de consentimento ou mensuração;
- mudança de comportamento pós clique;
- filtros aplicados no dashboard;
- variação concentrada em páginas específicas;
- diferença entre canais e origem atribuída.

Conduta:

- declarar a divergência;
- evitar conclusão categórica;
- recomendar investigação ou acompanhamento;
- buscar recorte por página, país, canal ou consulta.

---

# Escrita no Relatório Executivo

A classificação entre fato, hipótese, conclusão e nível de confiança deve orientar a análise.

Entretanto, o relatório final não deve repetir mecanicamente expressões como:

- Fato observado;
- Hipótese;
- Conclusão confirmada;
- Evidência forte;
- Evidência fraca;
- Nível de confiança.

Esses termos podem ser usados quando forem úteis, mas a escrita deve ser natural, executiva e consultiva.

O objetivo é que o leitor perceba segurança analítica sem que o relatório pareça uma documentação do raciocínio interno.

---

# Exemplos de Redação

## Redação adequada para hipótese

```text
A redução de CTR pode indicar menor aderência dos snippets à intenção de busca ou aumento de competição nos resultados. A recomendação é revisar títulos e descrições das páginas com maior volume de impressões antes de ampliar a intervenção para todo o site.
```

## Redação adequada para conclusão com boa sustentação

```text
O desempenho orgânico apresentou evolução consistente no período, com crescimento simultâneo de sessões orgânicas no GA4 e de cliques no Google Search Console. Esse comportamento reforça a importância do SEO como canal estrutural de aquisição para o projeto.
```

## Redação adequada para informação insuficiente

```text
Não há evidência suficiente para atribuir a variação a uma causa específica. O ponto deve ser acompanhado no próximo ciclo, com recorte por página e país para validar se o comportamento é pontual ou recorrente.
```

---

# Regras Obrigatórias

- Nunca transformar hipótese em conclusão.
- Nunca utilizar linguagem categórica sem evidência suficiente.
- Nunca assumir causalidade quando houver apenas correlação.
- Nunca extrapolar tendência além do período analisado sem sustentação histórica.
- Nunca recomendar ação corretiva ampla com baixa confiança.
- Nunca omitir limitações relevantes da análise.
- Sempre priorizar fatos antes de interpretações.
- Sempre indicar necessidade de validação quando a evidência for fraca.
- Sempre buscar confirmação em GA4 e GSC quando a leitura envolver tráfego orgânico.
- Sempre usar SEMrush, histórico e baseline como apoio quando disponíveis.
- Sempre adequar a recomendação ao nível de confiança.
- Sempre utilizar linguagem conservadora em caso de dúvida.
- Sempre manter a escrita final natural, executiva e consultiva.

---

# Fluxo de Decisão

Durante a elaboração das análises, seguir esta sequência:

1. Identificar o fato observado.
2. Verificar quais fontes sustentam o fato.
3. Classificar a evidência como forte, moderada ou fraca.
4. Verificar se há fontes divergentes.
5. Avaliar se existe histórico ou baseline que reforce a leitura.
6. Formular hipótese quando a causa não estiver confirmada.
7. Confirmar ou limitar a conclusão conforme o nível de evidência.
8. Definir nível de confiança.
9. Elaborar recomendação proporcional à confiança.
10. Redigir de forma natural, sem expor desnecessariamente a classificação interna.

---

# Objetivo Final

O relatório executivo deve transmitir segurança sem exagerar certezas.

Quando houver evidência forte, a análise pode ser mais assertiva.

Quando houver dúvida, a dúvida deve ser explicitada com linguagem proporcional e indicação de validação.

A qualidade do relatório depende tanto da capacidade de identificar oportunidades quanto da disciplina de não afirmar mais do que os dados permitem.