# Comando Mensal para Codex - SFTL Reporting

Inicie uma nova competência mensal do projeto SFTL Reporting.

Antes de qualquer ação, verifique se a competência mensal foi informada pelo usuário.

A competência deve estar no formato:

```text
AAAA-MM
```

Exemplo:

```text
2026-06
```

Se a competência não tiver sido informada, interrompa a execução e pergunte exatamente:

```text
Qual competência mensal devo processar? Responda no formato AAAA-MM, por exemplo 2026-06.
```

Depois que o usuário informar a competência, defina internamente:

```text
COMPETENCIA=<valor informado pelo usuário>
```

Use obrigatoriamente o valor de COMPETENCIA para montar todos os caminhos desta execução.

Não use mês fixo.
Não use outra competência.
Não crie pastas fora de reports/${COMPETENCIA}/.
Não reutilize caminhos de exemplos.
Não continue se a competência não estiver no formato AAAA-MM.

---

# Etapa 1 - Preparação da Competência

Esta etapa só pode começar depois que `COMPETENCIA` estiver definida com o valor informado pelo usuário.

Siga obrigatoriamente o arquivo START_HERE.md como orquestrador principal.

Antes de qualquer análise, leia e aplique integralmente:

1. README.md
2. prompts/00_MASTER_SPECIFICATION.md
3. todos os arquivos da pasta prompts/
4. todos os arquivos da pasta knowledge/
5. todos os arquivos disponíveis em history/, incluindo:
   - history/evolucao_mensal.md
   - history/indicadores_historicos.csv

Depois, usando o valor de COMPETENCIA:

1. Localize ou crie a competência em:

   reports/${COMPETENCIA}/

2. Crie ou valide as pastas:

   reports/${COMPETENCIA}/source/
   reports/${COMPETENCIA}/analysis/
   reports/${COMPETENCIA}/output/

3. Crie ou valide o arquivo:

   reports/${COMPETENCIA}/manifest.json

Nesta primeira etapa, não gere nenhuma análise.

Após preparar a estrutura, interrompa a execução e me solicite exatamente:

```text
Copie todos os PDFs para:

reports/${COMPETENCIA}/source/

Quando terminar, responda apenas:

CONTINUAR
```

---

# Etapa 2 - Análise da Competência após CONTINUAR

Quando eu responder `CONTINUAR`, use a mesma competência definida na Etapa 1 e valide `reports/${COMPETENCIA}/` seguindo START_HERE.md.

Antes de gerar qualquer análise:

1. Valide o `manifest.json`.
2. Liste os PDFs presentes em `source/`.
3. Identifique os relatórios obrigatórios.
4. Confirme a presença de Google Analytics 4 e Google Search Console.
5. Interrompa se houver ausência de fonte obrigatória ou inconsistência crítica.

Se a competência estiver válida, gere obrigatoriamente:

```text
reports/${COMPETENCIA}/analysis/ga4_analise.md
reports/${COMPETENCIA}/analysis/gsc_analise.md
reports/${COMPETENCIA}/output/resumo_executivo.md
```

Regras obrigatórias para esta etapa:

- Use GA4 e Google Search Console como fontes obrigatórias.
- Use SEMrush apenas como fonte complementar quando houver evidência relevante.
- Aplique a camada mínima de evidência numérica.
- Inclua valor atual, valor anterior, variação absoluta e variação percentual para os principais indicadores quando disponíveis.
- Inclua principais páginas, consultas, países, canais e eventos quando eles sustentarem a leitura executiva.
- Não transforme o relatório em tabela.
- Não repita o Looker Studio sem interpretação.
- Não gere DOCX.
- Não gere PDF.
- Não atualize `history/`.
- Não atualize `knowledge/`.
- Não atualize `knowledge/11_CHANGELOG.md`.

Após gerar os três arquivos Markdown, interrompa a execução e me solicite exatamente:

```text
Revise os arquivos gerados:

reports/${COMPETENCIA}/analysis/ga4_analise.md
reports/${COMPETENCIA}/analysis/gsc_analise.md
reports/${COMPETENCIA}/output/resumo_executivo.md

Faça a revisão humana, gere os arquivos finais no ChatGPT se necessário e, quando a competência estiver aprovada, responda apenas:

APROVADO PARA ENCERRAMENTO
```

---

# Etapa 3 - Encerramento após Aprovação Humana

Execute esta etapa somente quando eu responder exatamente:

```text
APROVADO PARA ENCERRAMENTO
```

Use a mesma competência definida na Etapa 1. Não solicite nova competência no encerramento, salvo se o contexto tiver sido perdido.

Antes disso, não atualize `history/`, `knowledge/` nem `knowledge/11_CHANGELOG.md`.

Após a aprovação humana, atualize apenas os arquivos permitidos:

```text
history/evolucao_mensal.md
history/indicadores_historicos.csv
knowledge/10_LICOES_APRENDIDAS.md
knowledge/11_CHANGELOG.md
reports/${COMPETENCIA}/manifest.json
```

Função dos arquivos de histórico:

- `history/evolucao_mensal.md` deve guardar a leitura narrativa aprovada da competência, com evolução, regressão ou estabilidade, principais conclusões e recomendações.
- `history/indicadores_historicos.csv` deve guardar os indicadores principais consolidados mês a mês, permitindo comparação histórica nas próximas competências.

Regras para atualização:

1. Em `history/evolucao_mensal.md`, registre de forma sintética:
   - competência analisada;
   - principais números aprovados;
   - principais conclusões;
   - principais recomendações;
   - leitura de evolução, regressão ou estabilidade.

2. Em `history/indicadores_historicos.csv`, registre os principais indicadores mensais aprovados para formar a série histórica do projeto.

   Inclua, quando disponíveis:

   - competência;
   - sessões;
   - usuários;
   - novos usuários;
   - sessões engajadas;
   - taxa de engajamento;
   - tempo médio de engajamento;
   - eventos principais ou key events;
   - sessões de Organic Search;
   - sessões de Direct;
   - cliques orgânicos;
   - impressões;
   - CTR;
   - posição média;
   - principal página com ganho;
   - principal página com queda;
   - principal query com ganho;
   - principal query com queda;
   - principal país ou grupo com ganho;
   - principal país ou grupo com queda;
   - observação executiva curta.

   Não incluir todos os indicadores disponíveis. Registrar apenas os principais números que permitam comparar a competência atual com os próximos meses.

3. Em `knowledge/10_LICOES_APRENDIDAS.md`, registre apenas aprendizados reutilizáveis para competências futuras.

   Não copie conclusões mensais comuns para este arquivo.

   Use este arquivo somente para aprendizados metodológicos, padrões recorrentes ou decisões que devem orientar análises futuras.

4. Em `knowledge/11_CHANGELOG.md`, registre:
   - data do encerramento;
   - competência encerrada;
   - arquivos gerados;
   - arquivos atualizados;
   - observações metodológicas relevantes.

5. Em `reports/${COMPETENCIA}/manifest.json`, atualize o status da competência para indicar que ela foi aprovada e encerrada operacionalmente.

Não altere os PDFs.
Não altere os arquivos em `source/`.
Não regenere `ga4_analise.md`, `gsc_analise.md` ou `resumo_executivo.md`, salvo se eu solicitar explicitamente.
Não gere DOCX.
Não gere PDF.

Ao concluir o encerramento, responda com um resumo curto dos arquivos atualizados.
