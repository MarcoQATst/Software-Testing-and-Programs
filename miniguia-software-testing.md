# 📖 Miniguia — Software Testing & Test Automation

Este miniguia consolida o conteúdo estudado no NotebookLM a partir das fontes selecionadas para o projeto.

## 1. Fundamentos de Software Testing

O material estudado apresenta Software Testing como uma disciplina voltada à identificação de defeitos e avaliação do comportamento do software. A atuação de QA também aparece ligada ao refinamento, à comunicação estruturada de falhas e à distinção entre prioridade e severidade.

A terminologia do ISTQB foi utilizada como uma das referências para organização conceitual do estudo.

Outro ponto recorrente foi a evolução para práticas de **shift-left**, **quality assistance** e **whole-team collaboration**, aproximando qualidade das etapas iniciais e distribuindo responsabilidade pelo produto.

## 2. Objetivos dos testes

Entre os objetivos destacados no material:

- reduzir riscos associados a defeitos;
- detectar problemas antes da produção;
- fornecer confiança para entregas e pipelines de CI/CD;
- aumentar a visibilidade sobre cobertura;
- reduzir tempo desperdiçado em diagnóstico e manutenção;
- apoiar acessibilidade e outras características de qualidade.

## 3. Áreas e especializações abordadas

As fontes relacionadas ao ISTQB apresentam diferentes trilhas de conhecimento e certificação, incluindo:

- Foundation Level;
- Test Analyst;
- Technical Test Analyst;
- Test Automation Engineering;
- Agile Technical Testing;
- Test Management;
- IA aplicada a testes;
- performance;
- segurança;
- usabilidade;
- mobile;
- acceptance testing;
- DevOps;
- outras especializações de domínio.

> Esses itens representam trilhas/áreas de conhecimento e certificação apresentadas pelas fontes e não devem ser confundidos com os níveis de teste do software.

## 4. Testes manuais vs. automatizados

| Aspecto | Manual | Automatizado |
|---|---|---|
| Execução | Humana | Scripts/frameworks |
| Exploração | Alta adaptabilidade | Limitada ao comportamento implementado |
| Repetibilidade | Custo cresce com repetição | Forte candidato para repetição |
| UX/usabilidade | Importante para julgamento humano | Pode apoiar verificações objetivas |
| Regressão | Pode se tornar custosa | Forte aplicação |
| Manutenção | Casos/procedimentos precisam ser atualizados | Código e infraestrutura precisam ser mantidos |

As duas abordagens são complementares. Automação não elimina a necessidade de investigação, julgamento e validação humana.

## 5. Quando automatizar

### Bons candidatos

- regressões executadas frequentemente;
- fluxos críticos e repetitivos;
- testes de APIs REST;
- testes de componentes;
- verificações executadas continuamente;
- cenários que precisam rodar em CI/CD;
- suítes que se beneficiam de paralelismo.

### Quando ter cautela

- avaliações subjetivas de UX/usabilidade;
- UAT e validações fortemente dependentes de pessoas/negócio;
- aspectos subjetivos de produtos específicos;
- testes altamente instáveis;
- cenários cujo custo de manutenção não compensa o benefício.

Automação deve ser tratada como investimento e decisão de engenharia.

## 6. Testes de regressão

Testes de regressão verificam se mudanças recentes introduziram problemas em comportamentos que anteriormente funcionavam.

Por serem repetidos ao longo do desenvolvimento, são candidatos frequentes à automação e à integração em pipelines.

O material também aborda regressão visual e Visual AI como mecanismos complementares para identificar alterações de interface.

## 7. Integração e APIs REST

Os conteúdos estudados abordam testes diretos de APIs para validar:

- requisições e respostas;
- métodos HTTP;
- headers;
- payloads;
- códigos de status;
- contratos/especificações.

A principal vantagem é validar comportamentos abaixo da UI e obter feedback mais direto sobre integrações e regras expostas por serviços.

## 8. End-to-End (E2E)

Testes E2E simulam jornadas de usuário através da aplicação.

São valiosos para validar integrações entre partes do sistema do ponto de vista externo, mas precisam ser planejados considerando custo de execução, estabilidade e manutenção.

## 9. Boas práticas de automação

### Evitar flaky tests

Testes inconsistentes reduzem a confiança na suíte.

Recursos de espera automática ajudam a evitar sincronizações frágeis baseadas apenas em tempos fixos.

### Reutilizar autenticação quando apropriado

O Cypress disponibiliza recursos como `cy.session()` para armazenar/restaurar contexto de autenticação e `cy.origin()` para cenários envolvendo diferentes origens.

### Paralelismo e sharding

Suítes podem ser distribuídas para reduzir o tempo de feedback em CI.

### Debugging

Ferramentas modernas oferecem recursos ricos de diagnóstico, como:

- Trace Viewer e UI Mode no Playwright;
- Time Travel e recursos de replay/debug no ecossistema Cypress.

## 10. Playwright

De acordo com o material estudado, Playwright oferece:

- testes E2E para aplicações web;
- suporte a Chromium, Firefox e WebKit;
- execução headed/headless;
- isolamento por contextos;
- paralelismo;
- retries;
- sharding;
- UI Mode;
- Trace Viewer;
- Codegen;
- relatórios HTML;
- suporte a Node.js, Python, Java e .NET.

### Exemplo de inicialização estudado

```bash
npm init playwright@latest
```

### Execução

```bash
npx playwright test
```

### UI Mode

```bash
npx playwright test --ui
```

## 11. Cypress

O material descreve Cypress como uma plataforma de testes web com arquitetura integrada ao ambiente do navegador/aplicação.

Entre os recursos estudados:

- E2E;
- Component Testing;
- `cy.request()` para APIs;
- Automatic Waiting;
- Time Travel;
- spies/stubs/clocks;
- `cy.session()`;
- `cy.origin()`;
- Cypress Cloud e recursos associados;
- capacidades relacionadas a acessibilidade e cobertura de UI apresentadas nas fontes.

## 12. Playwright vs. Cypress

| Critério | Playwright | Cypress |
|---|---|---|
| Arquitetura | Framework E2E com contextos isolados | Execução integrada ao browser/app |
| Navegadores destacados | Chromium, Firefox, WebKit | Chrome-family e Firefox |
| Linguagens destacadas | Node.js, Python, Java, .NET | JavaScript/TypeScript |
| Debug | Trace Viewer, UI Mode, Codegen | Time Travel, DevTools e recursos de replay |
| Sessão/contexto | Browser contexts e fixtures | `cy.session()` / `cy.origin()` |
| CI | Paralelismo, retries, sharding | Paralelização e recursos Cloud |

Não existe um vencedor universal. A escolha depende do produto, stack, equipe, navegadores necessários, estratégia de CI e características da suíte.

## 13. IA aplicada ao estudo e aos testes

As fontes também apresentaram aplicações modernas de IA relacionadas a:

- apoio à criação/análise de cenários;
- Visual AI;
- assistência no desenvolvimento;
- integração de ferramentas com assistentes através de MCP.

No contexto deste projeto, a IA foi utilizada principalmente como **ferramenta de aprendizagem ativa**: sintetizar fontes, comparar conceitos, gerar perguntas e reorganizar conhecimento.

## 14. Glossário

1. **CTFL:** certificação Foundation Level apresentada pelo ISTQB.
2. **Shift-Left:** antecipação de atividades de qualidade para fases iniciais.
3. **Quality Assistance:** abordagem de apoio à qualidade distribuída pelo time.
4. **Whole-Team Collaboration:** colaboração de toda a equipe na qualidade.
5. **CTAL-TAE:** trilha avançada relacionada a Test Automation Engineering.
6. **Flaky Test:** teste que apresenta resultados inconsistentes.
7. **Time Travel:** recurso de inspeção do Cypress baseado no histórico de comandos/estados.
8. **Automatic Waiting:** espera automática por condições adequadas antes da interação.
9. **Component Testing:** teste de componentes isolados.
10. **Test Replay:** recurso associado ao ecossistema Cypress Cloud para análise de execuções.
11. **UI Coverage:** visibilidade sobre elementos/áreas exercitados pela suíte, conforme material estudado.
12. **MCP:** Model Context Protocol, usado para fornecer contexto de ferramentas a sistemas compatíveis.
13. **Visual Regression:** comparação destinada a identificar mudanças visuais inesperadas.
14. **cy.session():** recurso Cypress para cache/restauração de sessão.
15. **cy.origin():** recurso Cypress para cenários envolvendo origens diferentes.
16. **Trace Viewer:** ferramenta Playwright para análise detalhada de execução.
17. **Sharding:** divisão da suíte em partes para execução distribuída/paralela.

## 15. Principais aprendizados

1. Qualidade começa antes da execução dos testes.
2. Automação não deve se limitar à UI.
3. Testes manuais e automatizados atendem necessidades diferentes e complementares.
4. Manter testes confiáveis é tão importante quanto aumentar a quantidade de testes.
5. Playwright e Cypress possuem características diferentes e devem ser avaliados pelo contexto.
6. IA pode acelerar o estudo, mas suas respostas precisam permanecer ligadas às fontes e ser avaliadas criticamente.
