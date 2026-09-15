# 🧪 Software Testing & Test Automation — AI-Assisted Study Guide

> Projeto de aprendizagem ativa desenvolvido com **NotebookLM**, combinando curadoria de fontes, engenharia de prompts e pensamento crítico para consolidar conhecimentos de **Software Testing** e **Test Automation**.

## 📌 Sobre o projeto

Este repositório documenta um caderno temático criado para um Desafio de Projeto da **DIO**.

O tema escolhido foi **Software Testing & Test Automation**, com foco em fundamentos de qualidade, estratégias de teste, automação, Playwright, Cypress e uso de Inteligência Artificial como apoio ao estudo.

A proposta não foi apenas pedir respostas à IA. O processo envolveu:

- seleção e curadoria de fontes;
- elaboração de perguntas estratégicas;
- comparação entre prompts amplos e prompts mais específicos;
- análise das limitações das respostas;
- refinamento dos prompts;
- consolidação do conhecimento em um miniguia.

## 🎯 Objetivos

- Revisar fundamentos de Software Testing e Quality Assurance;
- compreender o papel de testes manuais e automatizados;
- identificar cenários adequados ou inadequados para automação;
- revisar testes E2E, API, componentes, regressão e testes não funcionais;
- estudar características de Playwright e Cypress;
- exercitar engenharia de prompts aplicada ao aprendizado técnico;
- utilizar IA como ferramenta de síntese, comparação, questionamento e revisão;
- manter pensamento crítico sobre as respostas geradas.

## 📚 Curadoria de fontes

O NotebookLM foi alimentado com **5 fontes**, selecionadas para combinar fundamentos, referências profissionais e documentação de ferramentas.

| Fonte | Papel no estudo |
|---|---|
| **ISTQB® — Official Software Testing Certifications** | Terminologia, fundamentos, áreas de especialização e visão estruturada da disciplina de testes. |
| **Playwright — Installation / Documentation** | Referência técnica para instalação, execução e recursos do Playwright. |
| **Cypress — Why Cypress? Documentation** | Arquitetura, recursos, execução e capacidades do Cypress. |
| **Julio de Lima — conteúdos sobre QA e automação** | Perspectiva prática sobre rotina de QA, refinamento, APIs e automação. |
| **Tricentis / Applitools — conteúdos relacionados a qualidade e Visual AI** | Material complementar sobre automação, regressão visual, IA e práticas modernas de qualidade. |

> **Nota:** os endereços individuais das fontes não foram reconstruídos por inferência. No projeto foram preservadas apenas as referências efetivamente utilizadas no caderno.

## 🧠 Engenharia de Prompts

Um dos objetivos do projeto foi observar como a qualidade da pergunta modifica a utilidade da resposta.

### Experimento 1 — Fundamentos

**Prompt**

> Com base exclusivamente nas fontes deste notebook, explique os principais fundamentos de Software Testing e Test Automation. Organize a resposta em conceitos, objetivos, tipos de testes e boas práticas. Cite as fontes utilizadas em cada parte.

**Objetivo:** criar uma visão geral estruturada e rastreável do tema.

**Resultado:** o NotebookLM organizou conceitos de QA, automação, tipos de testes, objetivos e boas práticas, mantendo referências às fontes.

---

### Experimento 2 — Manual vs. automatizado

**Prompt**

> Compare testes manuais e testes automatizados com base nas fontes deste notebook. Explique vantagens, limitações, quando utilizar cada abordagem e dê exemplos práticos. Apresente o resultado em uma tabela e cite as fontes.

**Objetivo:** evitar a simplificação de que automação substitui testes manuais.

**Resultado:** a comparação evidenciou funções complementares das duas abordagens e destacou fatores como repetibilidade, exploração, UX, regressão e manutenção.

---

### Experimento 3 — Decisão de automação

**Prompt**

> Com base exclusivamente nas fontes deste notebook, explique quais tipos de testes são bons candidatos à automação e quais normalmente não deveriam ser priorizados. Considere repetibilidade, regressão, criticidade, estabilidade, custo de manutenção e retorno sobre o investimento.

**Objetivo:** estudar automação como decisão de engenharia, não como objetivo isolado.

**Resultado:** regressões frequentes, APIs, componentes e cenários repetitivos apareceram como candidatos relevantes, enquanto avaliações subjetivas e cenários altamente instáveis exigem cautela.

---

### Experimento 4 — Playwright vs. Cypress

**Prompt**

> Compare Playwright e Cypress utilizando apenas informações sustentadas pelas fontes deste notebook. Crie uma tabela comparativa e explique em quais contextos cada ferramenta pode ser adequada. Não declare um vencedor absoluto e não invente informações ausentes nas fontes.

**Objetivo:** comparar ferramentas sem transformar a análise em uma disputa de “melhor framework”.

**Resultado:** foram identificadas diferenças de arquitetura, navegadores, linguagens, debugging, sessão/contexto e execução em CI/CD.

## 🩹 Cicatrizes: o que não funcionou de primeira

Uma parte importante do exercício foi registrar as limitações do uso da IA.

### Cicatriz 1 — Prompt amplo demais

**Prompt inicial**

> Me explique testes de software.

**Problema:** apesar de produzir uma resposta válida, a pergunta deixava escopo, profundidade, estrutura e critérios de evidência abertos demais.

**Ajuste:** restringir a resposta às fontes e definir explicitamente os tópicos desejados.

**Prompt refinado**

> Refatore a explicação utilizando exclusivamente as fontes deste notebook. Organize em fundamentos, níveis/áreas de conhecimento, tipos de teste, testes manuais, automação e exemplos práticos. Para cada seção, indique as fontes utilizadas.

**Aprendizado:** especificar contexto, formato e evidências torna a resposta mais útil e auditável.

### Cicatriz 2 — Comparações podem virar opinião

**Problema:** perguntar apenas “Playwright ou Cypress?” favoreceria uma resposta simplificada ou um vencedor arbitrário.

**Ajuste:** definir critérios de comparação e proibir um vencedor absoluto.

**Aprendizado:** prompts comparativos funcionam melhor quando os critérios são explícitos.

### Cicatriz 3 — IA pode extrapolar as fontes

**Problema:** uma resposta tecnicamente plausível não significa que ela esteja sustentada pelo material estudado.

**Ajuste:** utilizar expressões como **“exclusivamente nas fontes deste notebook”** e solicitar referências.

**Aprendizado:** rastreabilidade é tão importante quanto fluência na resposta.

### Cicatriz 4 — Automação não significa automatizar tudo

**Problema:** uma pergunta genérica sobre automação pode enfatizar benefícios sem discutir custo e manutenção.

**Ajuste:** incluir repetibilidade, estabilidade, criticidade, custo de manutenção e ROI como critérios.

**Aprendizado:** um bom prompt pode forçar a análise de trade-offs, em vez de buscar somente vantagens.

➡️ [Veja a documentação detalhada dos prompts e cicatrizes](docs/prompts-e-cicatrizes.md)

## 📖 Miniguia

O estudo consolidado aborda:

- fundamentos de Software Testing;
- objetivos dos testes;
- testes manuais e automatizados;
- decisão sobre quando automatizar;
- regressão;
- integração e APIs REST;
- End-to-End;
- boas práticas de automação;
- flaky tests;
- Playwright;
- Cypress;
- comparação contextual entre as ferramentas;
- IA e práticas modernas de qualidade;
- glossário técnico.

➡️ [Acesse o Miniguia de Software Testing & Test Automation](docs/miniguia-software-testing.md)

## ⚡ Resumo rápido

### Manual x Automação

| Teste manual | Teste automatizado |
|---|---|
| Forte em exploração e avaliações humanas/contextuais | Forte em verificações repetíveis e frequentes |
| Útil em UX, usabilidade e validações de negócio | Útil em regressão, API, componentes e E2E |
| Adaptável durante a execução | Escalável em pipelines |
| Não exige script prévio | Exige desenvolvimento e manutenção |

### Quando automatizar?

**Bons candidatos**
- regressões frequentes;
- fluxos repetitivos;
- APIs;
- componentes;
- verificações contínuas;
- cenários executados frequentemente no CI/CD.

**Exigem cautela**
- avaliações subjetivas de UX/usabilidade;
- validações que dependem diretamente de julgamento humano;
- cenários extremamente instáveis;
- automações cujo custo de manutenção supera o benefício.

### Playwright x Cypress

| Critério | Playwright | Cypress |
|---|---|---|
| Browsers destacados nas fontes | Chromium, Firefox e WebKit | Família Chrome e Firefox |
| Linguagens destacadas | Node.js, Python, Java e .NET | JavaScript / TypeScript |
| Debug | Trace Viewer, UI Mode, Codegen | Time Travel, DevTools e recursos Cloud/Studio |
| CI | Paralelismo, retries e sharding | Paralelização e recursos adicionais via Cypress Cloud |
| Abordagem | Contextos isolados e locators | Execução integrada ao browser/app |

A escolha depende do contexto técnico e das necessidades do projeto.

## 🗂️ Glossário rápido

| Termo | Definição |
|---|---|
| **Shift-Left** | Antecipação das atividades de qualidade para fases iniciais do desenvolvimento. |
| **Quality Assistance** | Abordagem em que QA ajuda o time a incorporar qualidade ao processo. |
| **Whole-Team Collaboration** | Responsabilidade compartilhada pela qualidade. |
| **Flaky Test** | Teste automatizado com resultado inconsistente sem mudança correspondente no produto. |
| **Component Testing** | Teste de componentes de UI de forma isolada. |
| **Automatic Waiting** | Espera automática por condições adequadas antes de uma interação. |
| **Trace Viewer** | Ferramenta de inspeção de execuções do Playwright. |
| **Time Travel** | Recurso de inspeção de estados/comandos do Cypress. |
| **Sharding** | Divisão da suíte para execução paralela. |
| **MCP** | Protocolo usado para disponibilizar contexto de ferramentas a sistemas/assistentes compatíveis. |

O glossário completo está no [miniguia](docs/miniguia-software-testing.md).

## ♻️ Prompts reutilizáveis

Alguns modelos que podem ser reaproveitados em estudos futuros:

1. **Revisão:** “Utilizando exclusivamente as fontes, explique `[CONCEITO]` em níveis iniciante, intermediário e avançado e indique as referências.”
2. **Comparação:** “Compare `[A]` e `[B]` usando os critérios `[X, Y, Z]`. Não declare vencedor sem evidência nas fontes.”
3. **Entrevista:** “Crie 10 perguntas de entrevista sobre `[TEMA]` fundamentadas nas fontes e só revele as respostas após as perguntas.”
4. **Quiz:** “Crie um quiz de 10 questões sobre `[TEMA]`, com justificativa da resposta correta e referência.”
5. **Flashcards:** “Transforme os conceitos essenciais de `[TEMA]` em flashcards de pergunta/resposta.”
6. **Lacunas:** “Identifique quais perguntas importantes sobre `[TEMA]` não podem ser respondidas adequadamente pelas fontes atuais.”
7. **Cenário prático:** “Apresente um problema realista de QA envolvendo `[TEMA]` e peça que eu proponha uma solução antes de apresentar sua análise.”
8. **Automação:** “Avalie este cenário de teste considerando repetibilidade, criticidade, estabilidade, frequência, custo de manutenção e ROI. Explique se deve ser automatizado.”

## 💡 Principais aprendizados

O projeto reforçou que qualidade de software não depende apenas da execução de testes. Ela envolve colaboração, prevenção de defeitos, escolha adequada das estratégias de teste e manutenção de um sinal confiável de qualidade.

Também ficou evidente que **automação é uma decisão de engenharia**. Um cenário ser automatizável não significa necessariamente que deva ser automatizado.

No uso de IA, o principal aprendizado foi semelhante: respostas mais longas não são automaticamente melhores. **Contexto, restrições, fontes e critérios de avaliação** aumentam significativamente a qualidade e a rastreabilidade do resultado.

## 🛠️ Ferramentas e tecnologias

- NotebookLM
- Inteligência Artificial / LLMs
- GitHub
- Markdown
- Playwright
- Cypress

## 📂 Estrutura

```text
software-testing-notebooklm-study-guide/
├── README.md
└── docs/
    ├── prompts-e-cicatrizes.md
    └── miniguia-software-testing.md
```

## 👨‍💻 Autor

**Marco Aurélio Gomes**

Projeto desenvolvido para fins de estudo, prática de Engenharia de Prompts e consolidação de conhecimentos em Software Quality Assurance.

---

⭐ Se este material for útil para seus estudos, fique à vontade para usar os prompts como base para suas próprias revisões.
