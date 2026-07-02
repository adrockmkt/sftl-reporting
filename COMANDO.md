Inicie uma nova competência mensal do projeto SFTL Reporting.

VARIÁVEL DA COMPETÊNCIA:
COMPETENCIA=2026-06

Use obrigatoriamente o valor de COMPETENCIA para montar todos os caminhos desta execução.

Não use mês fixo.
Não use outra competência.
Não crie pastas fora de reports/${COMPETENCIA}/.
Não reutilize caminhos de exemplos.

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

Copie todos os PDFs para:

reports/${COMPETENCIA}/source/

Quando terminar, responda apenas:

CONTINUAR
