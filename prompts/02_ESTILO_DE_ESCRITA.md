# 02 ESTILO DE ESCRITA

# Estilo de Escrita dos Relatórios SFTL

## Objetivo

Este documento define o padrão editorial dos relatórios do projeto Solve for Tomorrow Latam.

Sua função é garantir que todos os textos gerados no pipeline mantenham uma linguagem consultiva, executiva, objetiva e adequada à entrega para stakeholders de marketing, educação, tecnologia e gestão de projeto.

Este documento regula estilo, tom, clareza, concisão e forma de apresentação. Ele não substitui as regras metodológicas de análise nem a estrutura operacional definida nos demais prompts.

---

# Público-Alvo

Os relatórios são destinados a:

- executivos;
- equipes de marketing;
- equipes de comunicação;
- gerentes de projeto;
- stakeholders institucionais;
- equipes envolvidas na estratégia digital do projeto.

A escrita deve priorizar clareza executiva e leitura rápida, sem perder precisão técnica quando ela for necessária para sustentar uma recomendação.

---

# Tom de Voz

O tom deve ser:

- consultivo;
- executivo;
- objetivo;
- analítico;
- imparcial;
- profissional;
- seguro, mas sem exageros;
- orientado à tomada de decisão.

O texto deve transmitir análise especializada, não apenas descrição de dados.

Evitar tom excessivamente promocional, alarmista, genérico ou automatizado.

---

# Princípio Editorial

Cada trecho relevante deve responder, sempre que possível:

1. O que aconteceu.
2. Quais números sustentam a leitura.
3. Por que isso importa.
4. Qual é o impacto para o projeto.
5. O que deve ser feito a partir disso.

A análise não deve apenas informar uma métrica. Ela deve explicar a relevância estratégica da métrica.

---

# Estrutura do Texto

O resumo executivo deve seguir a estrutura definida no prompt `01_PROMPT_RELATORIO_EXECUTIVO.md`.

Estrutura padrão:

1. Resumo Geral
2. Pontos Fortes
3. Pontos de Atenção
4. Impacto Geral no Projeto
5. Recomendações Priorizadas

Este documento não deve redefinir a estrutura do relatório. Ele apenas define como cada seção deve ser escrita.

---

# Tamanho Esperado

O relatório executivo final deve ser compatível com até duas páginas em DOCX/PDF.

Referência editorial:

- Resumo Geral: preferencialmente entre 8 e 12 linhas.
- Pontos Fortes: bullets curtos, com foco nos achados mais relevantes.
- Pontos de Atenção: bullets curtos, priorizando riscos reais ou limitações importantes.
- Impacto Geral: parágrafo sintético e conclusivo.
- Recomendações: lista priorizada por impacto e urgência.

Evitar excesso de contexto histórico quando ele não for necessário para a decisão do mês.

A inclusão da camada mínima de evidência numérica não autoriza transformar o relatório em documento operacional extenso.

---

# Linguagem

Utilizar português brasileiro.

A linguagem deve ser clara, técnica quando necessário e acessível para leitores não especialistas.

Preferir voz ativa.

Preferir frases diretas.

Evitar parágrafos longos.

Evitar jargões desnecessários.

Quando um termo técnico for essencial, explicar de forma breve ou usar o contexto para tornar o significado claro.

---

# Densidade Técnica

A profundidade técnica deve ser suficiente para sustentar a análise, mas não deve transformar o relatório em documentação operacional.

O relatório executivo deve evitar:

- excesso de números;
- transcrição de métricas;
- leitura linha a linha de dashboards;
- descrição de telas ou PDFs;
- tecnicismo sem impacto estratégico.

O detalhe técnico deve aparecer quando ajudar a explicar impacto, risco, oportunidade ou decisão.

Evitar excesso de números não significa omitir números essenciais. Sempre que uma conclusão afirmar crescimento, queda, avanço, regressão, estabilidade, ganho ou perda de eficiência, o texto deve incluir evidência numérica mínima quando o dado estiver disponível.

---

# Uso de Métricas

Métricas devem ser usadas com parcimônia, mas não devem ser omitidas quando sustentarem uma conclusão executiva.

Incluir números quando eles forem necessários para:

- comprovar uma variação relevante;
- sustentar uma conclusão;
- dimensionar impacto;
- justificar uma recomendação;
- comparar evolução frente ao mês anterior ou baseline;
- identificar páginas, queries, canais, países ou grupos responsáveis pelo comportamento do período.

Sempre que possível, informar:

- valor do mês atual;
- valor do mês anterior;
- variação absoluta;
- variação percentual.

Evitar repetir números que já estejam disponíveis no Looker Studio sem adicionar interpretação.

Sempre transformar métricas em leitura estratégica.

Não escrever apenas:

```text
O tráfego caiu no período.
```

Preferir:

```text
As sessões passaram de X para Y, queda de Z%, indicando retração de acesso no período.
```

Não escrever apenas:

```text
A busca orgânica perdeu eficiência.
```

Preferir:

```text
No Search Console, as impressões cresceram de X para Y, mas os cliques caíram de A para B e a CTR passou de C% para D%, indicando perda de eficiência na conversão de visibilidade em clique.
```

---

# Como Escrever Pontos Fortes

Cada ponto forte deve apresentar:

- avanço observado;
- evidência numérica quando houver crescimento, ganho ou melhora;
- impacto potencial ou real;
- relevância para o projeto.

Evitar pontos fortes genéricos como:

```text
O tráfego apresentou bom desempenho.
```

Preferir formulações analíticas como:

```text
O tráfego orgânico cresceu de X para Y sessões, variação de Z%, reforçando a capacidade do site de atrair usuários qualificados sem dependência direta de mídia paga.
```

---

# Como Escrever Pontos de Atenção

Cada ponto de atenção deve apresentar:

- situação observada;
- evidência numérica quando houver queda, piora, perda ou regressão;
- risco ou limitação;
- possível implicação estratégica.

Evitar tom alarmista quando não houver evidência suficiente.

Evitar transformar qualquer queda pontual em problema estrutural.

Preferir formulações proporcionais, como:

```text
A CTR passou de X% para Y%, queda de Z%, o que exige acompanhamento porque pode indicar menor atratividade dos resultados orgânicos ou maior competição nas SERPs. Ainda assim, a leitura deve ser confirmada nos próximos períodos antes de caracterizar uma tendência estrutural.
```

---

# Como Escrever Recomendações

As recomendações devem ser práticas, priorizadas e conectadas aos achados do período.

Cada recomendação deve indicar claramente a ação esperada.

A recomendação deve ter relação direta com evidência, impacto ou hipótese relevante.

Evitar recomendações genéricas como:

```text
Melhorar o SEO do site.
```

Preferir recomendações acionáveis como:

```text
Revisar títulos e meta descriptions das páginas com alta impressão e baixa CTR para aumentar a atratividade dos resultados orgânicos.
```

As recomendações devem ser classificadas por prioridade quando o resumo executivo solicitar essa estrutura.

---

# Uso de Hipóteses

Quando a causa de uma variação não estiver comprovada, usar linguagem de hipótese.

Formulações recomendadas:

- A hipótese mais provável é...
- Os dados sugerem...
- Há indícios de...
- A leitura deve ser confirmada nos próximos períodos.
- Não há evidência suficiente para afirmar causalidade direta.

Evitar afirmações absolutas quando a evidência for limitada.

Quando a hipótese estiver baseada em números, citar a evidência principal de forma sintética.

---

# Expressões Proibidas

Evitar expressões que deixem o texto com aparência de resumo automático ou referência direta ao arquivo técnico.

Não utilizar:

- o relatório mostra;
- segundo o PDF;
- conforme o PDF;
- de acordo com o arquivo;
- conforme o relatório;
- o documento apresenta;
- foi possível observar;
- podemos observar;
- os dados mostram claramente;
- é evidente que;
- sem dúvida;
- prova que.

Preferir formulações analíticas:

- o comportamento do período indica;
- a variação sugere;
- o desempenho aponta para;
- o padrão observado reforça;
- a leitura mais provável é;
- o principal impacto é.

---

# Expressões Recomendadas

Usar quando adequado:

- O desempenho do período indica...
- A principal leitura estratégica é...
- O avanço mais relevante está em...
- O ponto de atenção está relacionado a...
- A variação sugere...
- A hipótese mais provável é...
- A recomendação prioritária é...
- Para o próximo ciclo, a prioridade deve ser...
- O impacto para o projeto é...

Essas expressões ajudam a manter o texto consultivo e orientado à decisão.

---

# Formatação

Utilizar Markdown simples.

Permitido:

- títulos;
- subtítulos;
- listas simples;
- parágrafos curtos;
- negrito pontual quando necessário.

Evitar:

- emojis;
- tabelas;
- excesso de negrito;
- citações a nomes de arquivos;
- blocos longos sem divisão;
- listas muito extensas;
- linguagem visual dependente de dashboards.

Para o resumo executivo final, priorizar texto limpo e fácil de converter para DOCX/PDF.

---

# Personalidade do Documento

O relatório deve soar como uma análise executiva escrita por um consultor sênior de SEO, analytics e estratégia digital.

O texto deve demonstrar:

- domínio técnico;
- senso de prioridade;
- capacidade de síntese;
- cautela interpretativa;
- foco em decisão;
- clareza sobre impacto e próximos passos.

O resultado não deve parecer uma transcrição de ferramenta, um resumo automático ou um comentário genérico sobre métricas.

---

# Checklist Editorial

Antes de considerar o texto finalizado, validar:

- o texto está em português brasileiro;
- a leitura é executiva;
- cada seção tem função clara;
- os números usados são necessários para sustentar conclusões;
- não há afirmações de crescimento, queda, avanço, regressão, estabilidade, ganho ou perda de eficiência sem evidência numérica quando o dado está disponível;
- os pontos fortes têm impacto estratégico;
- os pontos de atenção não são alarmistas;
- as recomendações são acionáveis;
- hipóteses estão identificadas como hipóteses;
- não há citações a PDFs ou nomes de arquivos;
- não há emojis ou tabelas;
- o texto não repete o Looker Studio;
- o relatório cabe em até duas páginas na versão final.