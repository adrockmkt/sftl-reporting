# 08 RELATÓRIO EXECUTIVO

# Relatório Executivo Consolidado SFTL

## Objetivo

Este documento define como o `resumo_executivo.md` deve ser produzido dentro de cada competência mensal do projeto Solve for Tomorrow Latam.

O objetivo não é resumir relatórios individuais, PDFs técnicos ou dashboards.

O objetivo é produzir uma visão estratégica única do período, utilizando as evidências disponíveis para explicar:

- o que aconteceu;
- quais números sustentam a leitura;
- por que aconteceu ou qual é a hipótese mais provável;
- qual foi o impacto para o projeto;
- quais riscos e oportunidades devem ser considerados;
- quais ações devem ser priorizadas no próximo ciclo.

O público deste documento é formado por gestores, equipes de marketing, comunicação, educação, tecnologia e tomadores de decisão.

---

# Papel deste Documento

Este arquivo complementa o `01_PROMPT_RELATORIO_EXECUTIVO.md`.

Enquanto o prompt 01 define o processo de geração do relatório executivo, este documento define o padrão específico do conteúdo consolidado que será entregue no arquivo:

```text
reports/AAAA-MM/output/resumo_executivo.md
```

Este documento não orienta a geração de DOCX ou PDF. Esses formatos devem ser produzidos posteriormente no ChatGPT, após revisão humana e aprovação do Markdown final.

---

# Princípio Central

O relatório executivo deve contar uma única história sobre o período.

Ele não deve parecer uma soma de análises separadas.

O leitor deve perceber uma análise integrada, com conexão entre tráfego, busca orgânica, conteúdo, países, histórico e oportunidades estratégicas.

A função do relatório é transformar dados em decisão.

A síntese executiva deve ser objetiva, mas precisa ter evidência numérica suficiente para sustentar as conclusões principais.

---

# Fontes de Dados

## Fontes obrigatórias

As fontes obrigatórias são:

- Google Analytics 4;
- Google Search Console;
- histórico disponível;
- baseline e documentos da base `knowledge/`, quando disponíveis.

GA4 e Google Search Console devem sempre ser correlacionados.

## Fontes complementares

As fontes complementares podem incluir, quando disponíveis e relevantes:

- SEMrush Site Audit;
- SEMrush On Page SEO Checker;
- SEMrush Keyword Strategy;
- SEMrush Backlinks;
- SEMrush Position Tracking;
- outros relatórios técnicos anexados à competência.

Essas fontes não precisam aparecer em todas as seções e não devem ser tratadas como obrigatórias, salvo solicitação explícita do usuário.

Elas devem ser usadas apenas quando ajudarem a explicar impacto, risco, oportunidade ou recomendação.

---

# Regras de Seleção dos Achados

Nem todo dado deve entrar no relatório executivo.

Selecionar apenas achados que tenham impacto em pelo menos um dos pontos abaixo:

- tráfego qualificado;
- visibilidade orgânica;
- CTR ou conversão de visibilidade em clique;
- páginas estratégicas;
- conteúdos educacionais;
- países prioritários;
- idiomas relevantes;
- autoridade digital;
- risco técnico;
- recorrência histórica;
- oportunidade clara de otimização;
- decisão de próximo ciclo.

Dados operacionais sem impacto estratégico devem permanecer nas análises intermediárias ou no Looker Studio.

Entretanto, achados selecionados para o resumo executivo devem trazer evidência mínima quando indicarem crescimento, queda, avanço, regressão, estabilidade, ganho ou perda de eficiência.

---

# Camada Mínima de Evidência Numérica

O relatório executivo não deve repetir o Looker Studio, mas precisa conter números suficientes para sustentar a tese central do período.

Sempre que os dados estiverem disponíveis, as principais conclusões devem incluir:

- valor do mês atual;
- valor do mês anterior;
- variação absoluta;
- variação percentual.

A camada mínima de evidência deve aparecer principalmente no `Resumo Geral`, nos `Pontos Fortes`, nos `Pontos de Atenção` e no `Impacto Geral no Projeto`.

Não criar tabelas, salvo solicitação explícita do usuário.

Não listar todas as métricas disponíveis.

Selecionar apenas os números necessários para comprovar a leitura executiva.

---

# Indicadores Numéricos Mínimos no Resumo Executivo

Quando disponíveis, o resumo executivo deve citar de forma sintética:

## GA4

- sessões;
- usuários;
- novos usuários;
- sessões engajadas;
- eventos principais ou key events;
- canal Organic Search;
- canal Direct;
- principais páginas com ganho ou queda;
- principais países ou grupos com ganho ou queda.

## Google Search Console

- cliques;
- impressões;
- CTR;
- posição média;
- principais páginas com ganho ou queda;
- principais queries com ganho ou queda;
- principais países com ganho ou queda.

## SEMrush, quando relevante

- variação de visibilidade;
- posição média;
- tráfego estimado;
- backlinks;
- domínios de referência;
- autoridade;
- principais problemas técnicos.

SEMrush só deve entrar quando a evidência for relevante para explicar impacto, risco ou recomendação.

---

# Regra de Equilíbrio entre Síntese e Evidência

Evitar excesso de números não significa omitir números essenciais.

O relatório deve ser sintético, mas auditável.

Não escrever apenas:

```text
O projeto teve queda de tráfego.
```

Escrever:

```text
As sessões passaram de X para Y, queda de Z%, enquanto os usuários recuaram de A para B. Esse movimento sustenta a leitura de retração de alcance no período.
```

Não escrever apenas:

```text
A busca orgânica perdeu eficiência.
```

Escrever:

```text
No Search Console, as impressões cresceram de X para Y, mas os cliques caíram de A para B e a CTR passou de C% para D%. Esse comportamento indica perda de eficiência na conversão de visibilidade em clique.
```

---

# Estrutura Obrigatória

O relatório executivo deve seguir esta estrutura.

## 1. Resumo Geral

Apresentar a leitura executiva do período.

Responder, de forma sintética:

- o projeto evoluiu, regrediu ou permaneceu estável;
- quais números sustentam essa leitura;
- qual foi o principal comportamento do período;
- quais fatores explicam a leitura;
- qual foi o maior risco identificado;
- qual foi a maior oportunidade identificada;
- qual é o impacto geral para o projeto.

O `Resumo Geral` deve incluir um bloco curto de evidências numéricas, com os principais dados de GA4 e GSC.

Evitar repetir números em excesso.

Usar métricas apenas quando forem necessárias para sustentar a conclusão.

---

## 2. Impacto Geral no Projeto

Explicar como os indicadores se relacionam.

Exemplos de relações que devem ser avaliadas quando existirem:

- crescimento de impressões sem crescimento proporcional de cliques;
- aumento de cliques orgânicos sem avanço equivalente em sessões orgânicas;
- aumento de tráfego sem melhora de engajamento;
- melhora de rankings sem reflexo imediato em tráfego;
- crescimento regional concentrado em poucos países;
- evolução técnica ainda sem impacto mensurável em SEO;
- crescimento de autoridade sem evidência direta de ganho de ranking.

Sempre explicar o impacto para o projeto.

Nunca apenas listar métricas.

Quando a seção afirmar evolução, regressão, perda de eficiência ou ganho de eficiência, incluir evidência numérica de sustentação.

---

## 3. Evolução Histórica

Sempre que houver histórico disponível, explicar:

- se o comportamento representa tendência ou variação pontual;
- se há continuidade em relação aos meses anteriores;
- quais iniciativas parecem começar a produzir resultado;
- quais problemas continuam recorrentes;
- quais recomendações anteriores permanecem relevantes;
- como o período se posiciona frente ao baseline.

Caso não exista histórico suficiente, indicar a limitação de forma natural.

Não transformar variação pontual em tendência estrutural sem evidência suficiente.

---

## 4. Países e Grupos Regionais

Destacar apenas países ou grupos que realmente impactaram o período.

Priorizar:

- principais evoluções regionais;
- principais quedas;
- países que merecem prioridade;
- países com maior oportunidade orgânica;
- países com comportamento divergente entre tráfego e busca;
- mercados com impacto relevante para o projeto.

Não listar todos os países.

Utilizar os grupos regionais oficiais quando isso ajudar a leitura estratégica.

Quando houver dados disponíveis, citar os principais números de sessões, cliques, impressões, eventos, CTR ou posição média que sustentam a leitura regional.

---

## 5. Idiomas

Avaliar idiomas quando houver dados disponíveis e impacto estratégico.

Idiomas principais:

- Português;
- Espanhol;
- Inglês.

A análise deve explicar:

- qual idioma evoluiu;
- qual idioma perdeu desempenho;
- se há concentração excessiva em um idioma;
- se há oportunidade editorial ou regional associada ao idioma;
- qual o impacto para alcance latino-americano do projeto.

Se os dados de idioma não estiverem disponíveis ou não forem relevantes na competência, não forçar uma seção extensa.

Quando a análise afirmar ganho ou perda por idioma, incluir números de páginas, sessões, cliques, impressões ou CTR que sustentem a leitura.

---

## 6. Conteúdos e Páginas Estratégicas

Destacar conteúdos com impacto real no período.

Priorizar:

- páginas com maior contribuição para tráfego ou busca orgânica;
- páginas que ganharam visibilidade;
- páginas que perderam força;
- conteúdos educacionais com potencial de expansão;
- páginas institucionais importantes;
- temas com oportunidade editorial;
- conteúdos que podem ser reforçados com links internos ou atualização.

Não transformar a seção em inventário de URLs.

A análise deve explicar por que as páginas ou temas citados são relevantes para o projeto.

Sempre que possível, citar as principais páginas ou URLs com suas variações de sessões, cliques, impressões, CTR ou posição média.

---

## 7. SEO Técnico

Incluir esta seção quando houver evidência técnica relevante.

Podem ser considerados:

- rastreabilidade;
- indexação;
- canibalização;
- duplicidades;
- metadados;
- links quebrados;
- performance;
- arquitetura;
- problemas estruturais identificados em auditorias.

Priorizar apenas aquilo que tenha impacto potencial ou real em SEO, experiência ou mensuração.

Não tratar todo erro técnico como prioridade alta.

Se não houver dado técnico relevante na competência, não forçar análise técnica extensa.

Quando houver números técnicos relevantes, citar volume de URLs afetadas, variação ou prioridade relativa.

---

## 8. Autoridade e Backlinks

Incluir esta seção quando houver dados de backlinks ou autoridade relevantes.

Consolidar:

- evolução de backlinks;
- domínios de referência;
- autoridade;
- toxicidade;
- qualidade do perfil de links;
- oportunidades de link building institucional.

Explicar o impacto estratégico.

Não afirmar que backlinks causaram melhoria de ranking sem evidência adicional.

Quando houver dados disponíveis, citar números principais de backlinks, domínios de referência, authority score, toxicidade ou variação relevante.

---

## 9. Keywords e Intenção de Busca

Incluir esta seção quando houver dados relevantes de palavras-chave.

Consolidar:

- evolução das palavras-chave;
- intenção de busca;
- oportunidades editoriais;
- mercados com maior potencial;
- temas educacionais associados;
- relação entre queries e conteúdos existentes.

Relacionar keywords com páginas e oportunidades de conteúdo.

Não listar palavras-chave de forma excessiva.

Sempre que possível, citar queries específicas com cliques, impressões, CTR ou posição média quando elas sustentarem a leitura executiva.

---

# Recomendações Priorizadas

As recomendações devem ser acionáveis e conectadas aos achados do período.

Separar obrigatoriamente em três níveis.

## Alta prioridade

Ações que devem ser executadas ou encaminhadas no próximo ciclo por terem impacto direto em tráfego, SEO, visibilidade, risco técnico, páginas estratégicas ou países prioritários.

## Média prioridade

Ações de otimização e evolução que podem melhorar desempenho, mas não bloqueiam o resultado atual.

Incluem ajustes editoriais, revisão de snippets, links internos, atualização de conteúdo e expansão controlada.

## Baixa prioridade

Ações complementares, refinamentos futuros ou iniciativas estruturais de longo prazo sem urgência imediata.

---

# Regras Obrigatórias

- Nunca resumir individualmente os PDFs.
- Nunca citar nomes de arquivos no texto final.
- Nunca usar expressões como `segundo o PDF`, `o relatório mostra` ou `conforme o arquivo`.
- Nunca repetir números disponíveis no Looker Studio sem interpretação.
- Nunca omitir números essenciais necessários para sustentar conclusões executivas.
- Nunca afirmar crescimento, queda, avanço, regressão, estabilidade ou perda de eficiência sem evidência numérica quando os dados estiverem disponíveis.
- Nunca listar métricas sem explicar impacto.
- Nunca repetir recomendações de meses anteriores sem contexto.
- Nunca apresentar hipótese como fato.
- Nunca afirmar causalidade sem evidência suficiente.
- Nunca tratar toda variação pontual como tendência.
- Nunca forçar seções sem dados relevantes.
- Sempre correlacionar GA4 e Google Search Console.
- Sempre considerar histórico e base de conhecimento quando disponíveis.
- Sempre usar SEMrush como fonte complementar quando houver evidência útil.
- Sempre explicar causa provável, impacto e consequência.
- Sempre priorizar o que realmente influencia decisões.
- Sempre conectar recomendações aos achados do período.
- Sempre aplicar a camada mínima de evidência numérica.

---

# Linguagem

O relatório deve parecer escrito por um consultor sênior de SEO, analytics e estratégia digital.

A linguagem deve ser:

- objetiva;
- consultiva;
- estratégica;
- clara;
- proporcional à evidência;
- orientada à decisão.

Evitar:

- excesso de detalhes técnicos;
- listas muito longas;
- linguagem acadêmica;
- linguagem excessivamente otimista;
- linguagem excessivamente pessimista;
- tom automatizado;
- transcrição de dashboard;
- recomendações genéricas.

Buscar equilíbrio entre riscos e oportunidades.

A necessidade de incluir evidência numérica não autoriza transformar o resumo executivo em um relatório operacional extenso.

---

# Resultado Esperado

Ao terminar a leitura, o cliente deve compreender:

- como o projeto evoluiu no período;
- quais números sustentam essa leitura;
- quais fatores explicam a evolução ou retração;
- quais mercados merecem atenção;
- quais idiomas ou conteúdos tiveram relevância;
- quais problemas continuam limitando o desempenho;
- quais oportunidades devem ser priorizadas;
- quais ações devem ser executadas no próximo ciclo.

O relatório deve servir como documento executivo para tomada de decisão e complementar o Looker Studio, nunca substituí-lo.