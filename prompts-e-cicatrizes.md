# 🧠 Engenharia de Prompts e Cicatrizes

Este documento registra como os prompts foram utilizados para transformar um conjunto de fontes sobre Software Testing em material de estudo estruturado.

O objetivo não foi apenas obter respostas, mas observar como **escopo, contexto, restrições e critérios** alteram a qualidade da saída.

## Experimento 1 — Fundamentos

### Prompt
> Com base exclusivamente nas fontes deste notebook, explique os principais fundamentos de Software Testing e Test Automation. Organize a resposta em conceitos, objetivos, tipos de testes e boas práticas. Cite as fontes utilizadas em cada parte.

### Objetivo
Obter uma visão geral estruturada, evitando uma resposta sem organização.

### Resultado observado
A resposta separou conceitos, objetivos, tipos de testes e boas práticas, abordando QA, automação, E2E, APIs, testes não funcionais, CI/CD, flaky tests e shift-left.

### Aprendizado
Indicar previamente a estrutura desejada reduz a necessidade de reorganizar a resposta posteriormente.

---

## Experimento 2 — Manual vs. automatizado

### Prompt
> Compare testes manuais e testes automatizados com base nas fontes deste notebook. Explique vantagens, limitações, quando utilizar cada abordagem e dê exemplos práticos. Apresente o resultado em uma tabela e cite as fontes.

### Objetivo
Analisar as duas abordagens de forma complementar.

### Resultado observado
A resposta apresentou vantagens, limitações, contextos e exemplos, destacando o papel humano em exploração/UX e o ganho da automação em repetibilidade e regressão.

### Aprendizado
Pedir explicitamente vantagens **e limitações** reduz respostas excessivamente favoráveis a uma única abordagem.

---

## Experimento 3 — Quando automatizar

### Prompt
> Com base exclusivamente nas fontes deste notebook, explique quais tipos de testes são bons candidatos à automação e quais normalmente não deveriam ser priorizados. Considere repetibilidade, regressão, criticidade, estabilidade, custo de manutenção e retorno sobre o investimento.

### Objetivo
Tratar automação como uma decisão técnica baseada em critérios.

### Resultado observado
A resposta destacou regressões, APIs, componentes e verificações contínuas como bons candidatos e apontou avaliações subjetivas e cenários instáveis como situações que exigem cautela.

### Aprendizado
Incluir critérios de decisão no prompt produz uma análise de trade-offs mais útil.

---

## Experimento 4 — Comparação de ferramentas

### Prompt
> Compare Playwright e Cypress utilizando apenas informações sustentadas pelas fontes deste notebook. Crie uma tabela comparativa e explique em quais contextos cada ferramenta pode ser adequada. Não declare um vencedor absoluto e não invente informações ausentes nas fontes.

### Objetivo
Entender diferenças relevantes sem transformar a comparação em ranking.

### Resultado observado
Foram comparadas arquitetura, navegadores, linguagens, debugging, gerenciamento de sessão/contexto e CI/CD.

### Aprendizado
Definir que não existe um vencedor obrigatório ajuda a produzir uma comparação contextual.

---

# 🩹 Cicatrizes / Troubleshooting

## Cicatriz 1 — “Me explique testes de software”

### Prompt inicial
> Me explique testes de software.

### Problema
A pergunta é ampla. Embora a resposta tenha abordado objetivos, formas de execução, tipos de testes e papel do QA, o modelo tinha liberdade excessiva para escolher profundidade e organização.

### Ajuste
Foi solicitado uso exclusivo das fontes, estrutura definida e identificação das referências.

### Prompt refinado
> Refatore a explicação utilizando exclusivamente as fontes deste notebook. Organize em fundamentos, níveis/áreas de conhecimento, tipos de teste, testes manuais, automação e exemplos práticos. Para cada seção, indique as fontes utilizadas.

### Resultado
A nova resposta passou a relacionar explicitamente o conteúdo às fontes e trouxe exemplos técnicos de Cypress e Playwright.

### Aprendizado
**Prompt específico > prompt apenas amplo**, principalmente em estudos baseados em fontes.

---

## Cicatriz 2 — Comparação sem critérios

### Problema
Perguntas como “Playwright ou Cypress?” deixam o modelo decidir sozinho o que significa “melhor”.

### Ajuste
Foram definidos critérios técnicos e solicitado que nenhuma ferramenta fosse declarada vencedora absoluta.

### Aprendizado
Uma comparação precisa de **critérios**, não apenas de duas alternativas.

---

## Cicatriz 3 — Resposta plausível não significa resposta comprovada

### Problema
LLMs conseguem produzir explicações convincentes mesmo quando determinado detalhe não aparece no material fornecido.

### Ajuste
Os prompts passaram a incluir:
> “Utilize exclusivamente informações sustentadas pelas fontes deste notebook.”

Também foram solicitadas referências.

### Aprendizado
Ao estudar com IA, **rastreabilidade e verificabilidade** precisam fazer parte do prompt.

---

## Cicatriz 4 — Automação sem trade-offs

### Problema
Perguntar apenas sobre benefícios da automação pode ocultar manutenção, instabilidade e custo.

### Ajuste
A pergunta foi reformulada para considerar:
- repetibilidade;
- regressão;
- criticidade;
- estabilidade;
- custo de manutenção;
- ROI.

### Aprendizado
Adicionar fatores de decisão faz a IA raciocinar sobre o problema de forma mais próxima de uma decisão real de engenharia.

---

# ♻️ Prompts reutilizáveis

## 1. Revisão em níveis
> Utilizando exclusivamente as fontes deste notebook, explique `[CONCEITO]` em três níveis: iniciante, intermediário e avançado. Para cada nível, forneça um exemplo e indique as referências utilizadas.

## 2. Comparação técnica
> Compare `[TECNOLOGIA A]` e `[TECNOLOGIA B]` considerando `[CRITÉRIOS]`. Use somente as fontes disponíveis, apresente evidências e não declare um vencedor absoluto sem suporte das referências.

## 3. Simulação de entrevista
> Com base nas fontes, crie 10 perguntas de entrevista técnica sobre `[TEMA]`, aumentando gradualmente a dificuldade. Faça uma pergunta por vez e espere minha resposta antes de avaliar.

## 4. Quiz
> Crie um quiz com 10 questões sobre `[TEMA]`. Não mostre o gabarito inicialmente. Depois das minhas respostas, corrija cada questão, explique o conceito e indique a fonte.

## 5. Flashcards
> Identifique os conceitos essenciais de `[TEMA]` nas fontes e transforme-os em flashcards curtos no formato `Pergunta | Resposta`.

## 6. Identificação de lacunas
> Analise as fontes e liste perguntas importantes sobre `[TEMA]` que não podem ser respondidas adequadamente com o material atual. Não tente preencher as lacunas com conhecimento externo.

## 7. Cenário prático
> Crie um cenário realista de QA envolvendo `[TEMA]`. Primeiro apresente somente o problema e espere minha solução. Depois avalie minha resposta com base nas fontes.

## 8. Decisão de automação
> Analise o seguinte cenário de teste: `[CENÁRIO]`. Considere frequência, repetibilidade, criticidade, estabilidade, custo inicial, custo de manutenção e ROI. Explique se a automação é indicada, parcialmente indicada ou não indicada e justifique com as fontes.
